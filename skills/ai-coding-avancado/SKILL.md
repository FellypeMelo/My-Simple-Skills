# AI Coding Avançado – Skill para LLM

## Identificação

- **Nome:** `ai-coding-avancado`
- **Descrição:** Tratado técnico sobre codificação avançada com IA. Cobre prompt engineering para código, TDD com IA, anti-padrões de vibe coding, economia de contexto, ciclo Red-Green-Refactor agêntico e orquestração multiagentes.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **codificação assistida por IA**, **vibe coding**, **engenharia de prompt para código**, **TDD com agentes**, **orquestração multiagente**, **gestão de contexto**, **anti-padrões em geração de código** ou **arquitetura de software com LLMs**.

### Como usar este conhecimento

1. **Diagnóstico do problema**  
   - Identifique se a questão envolve geração de código, refatoração, depuração, planejamento arquitetural ou governança de agentes.
   - Use a taxonomia de paradigmas (LLM simples, agente com ferramentas, ReAct, multiagente) para enquadrar a solução.

2. **Aplicação dos princípios fundamentais**  
   - **DRTD (Decodificação Restrita por Topologia de Domínio):** Estruture prompts seguindo a fórmula **C + R + K + O** (Contexto, Papel, Conhecimento/Regras, Objetivo/Saída).
   - **Akita Rules:** Priorize simplicidade, isole estado, evite abstrações prematuras, repudie overengineering.
   - **Anti-padrões:** Esteja alerta para falsa abstração, acoplamento implícito (mau DRY) e inchaço de código (LLM Bloat).

3. **Estratégias de orquestração**  
   - Escolha entre **ReAct**, **Plan-and-Execute** ou **Reflexion** conforme a complexidade da tarefa.
   - Para grandes bases de código, use **engenharia de contexto incremental** (repo maps, AST, isolamento topológico).

4. **Validação e controle**  
   - Sempre que possível, exija que o agente gere um plano (`<thinking>`) e auto-crítica (`<reflection>`) antes do código final.
   - Utilize testes arquiteturais (dependency-cruiser, ArchUnit) para barrar violações de camadas.
   - Para tarefas críticas, aplique o **checklist operacional** (seção 6.1).

5. **Escolha do modelo**  
   - Consulte a análise comparativa (capítulo 7) para decidir entre Claude, GPT ou Gemini conforme a necessidade: refatoração segura, velocidade, ou varredura de contexto massivo.

### Formato de resposta preferido

- Sempre que possível, entregue **diffs estruturados**, **código funcional** e **explicações concisas**.
- Inclua justificativas baseadas nos princípios do tratado (ex.: “evitei uma abstração prematura seguindo a Regra das Três Repetições”).
- Se a solução exigir mudanças arquiteturais profundas, peça confirmação humana com a flag `INTERVENÇÃO_HUMANA_REQUERIDA`.

---

## Visão Geral

Este documento é um tratado técnico abrangente sobre a aplicação de Modelos de Linguagem de Grande Escala (LLMs) no desenvolvimento de software. Ele aborda desde os fundamentos cognitivos dos transformers até estratégias avançadas de orquestração multiagente, passando por engenharia de prompt rigorosa, arquitetura limpa e prevenção de anti-padrões específicos da geração de código por IA.

O objetivo é fornecer um arcabouço teórico e prático para engenheiros de software e arquitetos que desejam governar o comportamento estocástico dos LLMs, transformando‑os em ferramentas previsíveis e produtivas dentro de um ecossistema de desenvolvimento profissional.

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- AI coding, vibe coding, prompt engineering para código  
- TDD com IA, TDD agêntico, ciclo red-green-refactor  
- Orquestração multiagente, agentes autônomos de codificação  
- Gestão de contexto, janela de contexto, economia de tokens  
- Anti-padrões em código gerado por IA (falsa abstração, acoplamento implícito, LLM bloat)  
- Arquitetura de software com LLMs, Akita Rules, clean code pragmático  
- Ferramentas como Cursor, Windsurf, Aider, Cline, Claude Code, GitHub Copilot  
- Comparação entre modelos (Claude, GPT, Gemini) para tarefas de código  

**Palavras‑chave:** AI coding, vibe coding, prompt engineering, TDD agêntico, multiagentes, context window, coding assistants, red-green-refactor, anti-padrões IA, Akita Rules, DRTD, ReAct, Plan-and-Execute, Reflexion.

---

## Conteúdo Completo

### Sumário Executivo

A integração de LLMs no ciclo de desenvolvimento de software exige rigor arquitetural e metodologias profundas. A prática informal do “vibe coding” leva a consequências estruturais desastrosas: aumento de falhas lógicas, problemas de segurança e ineficiências de I/O. Este tratado estabelece fundamentos teóricos e práticos para governar o caos probabilístico dos modelos generativos, transformando‑os em motores quase‑determinísticos de produtividade estruturada.

---

## Capítulo 1: Fundamentos Cognitivos de AI Coding

### 1.1 A Matemática do Raciocínio de LLMs na Geração de Código

O “raciocínio” de um LLM é uma aproximação probabilística guiada pela arquitetura Transformer. O mecanismo de auto‑atenção (self‑attention) relaciona Queries (Q), Keys (K) e Values (V):

\[
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
\]

No contexto de código, a matriz Q representa o estado atual da geração, K o contexto disponível (variáveis, imports), e o produto escalar \(QK^T\) identifica quais abstrações influenciam a predição do próximo token. Modelos como StarCoder usam Multi‑Query Attention (MQA) para inferências rápidas com janelas extensas.

**Implicação prática:** a ordem e a relevância da informação no prompt são cruciais. Fornecer um arquivo de 10 mil linhas para resolver um bug local satura a atenção com ruído, degradando o sinal semântico.

### 1.2 Limitações Estruturais: Entropia, Compressão e Alucinação

A alucinação não é um bug corrigível por depuração clássica, mas sim um subproduto da compressão com perdas (lossy compression) dos dados de treinamento. Quando um detalhe de API raramente documentado excede a capacidade paramétrica, o modelo interpola com base na proximidade semântica. Além disso, o aumento indiscriminado da janela de contexto agrava o não determinismo, diluindo o vetor de atenção e provocando a síndrome da “agulha no palheiro”.

### 1.3 Espectro de Agência e Evolução Arquitetural

| Paradigma | Arquitetura | Casos de Uso |
|-----------|-------------|--------------|
| LLM Simples (zero‑shot/few‑shot) | Stateless, transacional | Autocompletar blocos simples, funções puras |
| Agente com Ferramentas (tool use) | Interfaces declarativas (JSON‑schema) | Extração de logs, execução de testes, buscas |
| Agente com Memória e Raciocínio (ReAct) | Ciclo raciocínio‑ação‑observação | Depuração interativa, refatorações |
| Sistema Multiagente Orquestrado | Coreografia com planejador, trabalhadores, revisores | Escala corporativa, arquiteturas complexas |

A confusão entre esses níveis é a causa primária do fracasso de agentes em produção.

### 1.4 Engenharia Cognitiva Aplicada a Código

Para combater a miopia topológica dos LLMs, emprega‑se a extração de **Grafos de Sintaxe Abstrata (AST)** e a geração de **Repo Maps**. Em vez de alimentar o modelo com milhares de linhas, o orquestrador condensa a arquitetura em assinaturas e dependências, usando algoritmos de centralidade (PageRank) para selecionar os nós cruciais.

### 1.5 Casos de Falha Reais

- **Armadilha do Vibe Coding:** código aparentemente coerente que ignora ciclo de vida (memory leaks, race conditions).
- **Quebra silenciosa na refatoração:** ao atingir o limite de contexto, o modelo substitui implementações por “// resto do código permanece igual”, colapsando o build.

---

## Capítulo 2: Engenharia Suprema de Prompt para Código

### 2.1 Metodologia DRTD: Decodificação Restrita por Topologia de Domínio

A fórmula conceitual **C + R + K + O** estrutura prompts de alta precisão:

- **Contexto (C):** delimitação minimalista do estado (repo map, arquivos estritamente necessários).
- **Papel Restritivo (R):** identidade cognitiva que filtra o espaço de probabilidades (ex.: Arquiteto Focado em Baixa Latência).
- **Conhecimento e Regras Arquiteturais (K):** axiomas inegociáveis (proibir ORMs pesados, exigir fatiamento vertical).
- **Objetivo Estrito e Saída (O):** formato determinístico (diffs, JSON‑schema), suprimindo prosa redundante.

### 2.2 Estrutura Profunda das Camadas do DRTD

Um prompt mestre deve seguir esta ordem de precedência:

1. **Perfil Epistemológico** – quem o modelo é e como avalia rigor técnico.
2. **Contextualização Isolada** – grafo AST e arquivos parciais.
3. **Restrições Negativas (Anti‑Patterns)** – o que não pode fazer (ex.: “não abstrair preventivamente”).
4. **Obrigação de Raciocínio Reflexivo (Chain‑of‑Thought)** – uso de tags `<thinking>` para análise prévia.
5. **Critérios de Qualidade Verificáveis** – métricas de performance e governança.
6. **Mecânica de Resposta e Validação** – formato de saída (diff, JSON).

**Comparação entre prompt fraco e prompt fundacional (DRTD):**  
(Ver tabela no original – destaca definição identitária, estrutura de contexto, mecanismo de execução e gestão de risco.)

### 2.3 Engenharia de Meta‑Prompts e Recursividade Estrutural

O **Meta‑Prompting** transfere o foco da resolução direta para o gerenciamento do processo. Um agente orquestrador constrói o prompt instrucional mais seguro para uma tarefa, e um agente codificador subalterno executa. Tipos:

- **Meta‑Prompts de Planejamento:** geram fluxogramas em pseudocódigo antes do código final.
- **Meta‑Prompts de Auto‑Revisão:** o modelo assume papel adversário para criticar seu próprio código.
- **Meta‑Prompts de Refatoração Arquitetural:** agrupam nós da AST para propor reestruturações modulares.

---

## Capítulo 3: Arquitetura Inspirada nas Akita Rules e a Governança da Simplicidade

### 3.1 Separação Estrutural Focada e Supressão do Overengineering

Os LLMs tendem a gerar código “enterprise” inflado (factories, proxies, injeções bizantinas). Para neutralizar isso, adote **Fatias Verticais (Vertical Slices)** ou módulos de domínio fechado:

- **Camada de Domínio Puro:** entidades e regras de negócio, livres de I/O e frameworks.
- **Camada de Aplicação:** orquestra casos de uso, sem lógica de domínio.
- **Camada de Infraestrutura:** banco de dados, APIs, estado global – tratada com escrutínio paranoico.

### 3.2 Sistema de Validação Arquitetural Pós‑Geração

Use ferramentas de teste arquitetural como guardrails:

- **JavaScript/TypeScript:** dependency‑cruiser com regras de acoplamento.
- **Java/C#:** ArchUnit (ou TSArch) para escrever testes que barram violações de camada.

Exemplo de configuração dependency‑cruiser:

```javascript
module.exports = {
  forbidden: [{
    name: 'no-domain-deps',
    from: { path: '^src/domain' },
    to: { path: '^src/infrastructure' }
  }]
};
```

### 3.3 Checklist Arquitetural Estrito para Injeção no Prompt Mestre

1. **Isolamento de Estado:** funções puras, side‑effects gerenciados por injeção explícita.
2. **Repúdio à Prematuridade:** nenhuma abstração antes de três repetições (Regra das Três Repetições).
3. **Proibição de Magia Negra:** evitar reflexão, monkey‑patching, one‑liners ilegíveis.
4. **Acoplamento Físico e Topológico:** componentes que mudam juntos devem estar juntos no espaço do projeto.

---

## Capítulo 4: Estratégias Avançadas de AI Engineering e Orquestração

### 4.1 Test‑Driven Development (TDD) Sistematizado por IA

O TDD assistido por IA inverte o paradigma tradicional: os testes tornam‑se contratos formais que estancam o não‑determinismo.

1. **Code Planning First:** documento de intenção modelando a interface semântica.
2. **Geração e Validação do Contrato (Red):** agente QA desenvolve testes unitários.
3. **Implementação Iterativa Guiada (Green):** agente desenvolvedor recebe contexto dos testes falhos e itera até passar.

### 4.2 Arquiteturas de Orquestração Multiagente

- **Padrão ReAct (Reason + Act):** ciclo curto de raciocínio, ação, observação. Ideal para exploração dinâmica, mas sujeito a saturação de contexto.
- **Padrão Plan‑and‑Execute:** separa planejamento (modelo massivo) da execução (modelos rápidos paralelos). Escalável e robusto.
- **Padrão Reflexion (Self‑Critique Interno):** após gerar código, um modelo crítico o escrutina sob as Akita Rules e corrige antes de apresentar.

### 4.3 Controle Dimensional de Alucinação e Engenharia de Contexto Incremental

- **Isolamento de Caminho e Filtragem Topológica:** use AST para extrair apenas dependências diretas e reversas dos métodos afetados.
- **Gestão Direcional de Cachê:** coloque regras estáticas no início do prompt (aproveitando prompt caching) e anexe conteúdo dinâmico ao final.
- **Quando manter ou quebrar o contexto:** contextos unificados são essenciais na fase de mapeamento; descarte a janela histórica ao mudar de tarefa não correlacionada.

---

## Capítulo 5: Mapeamento e Prevenção de Anti‑Patterns em AI Coding

### 5.1 O Flagelo da Falsa Abstração (Premature Abstraction)

LLMs, treinados em tutoriais de padrões de projeto, tendem ao overengineering. Ex.: para um validador de inteiro, criam `IValidator<T>`, `BaseValidatorAbstract`, etc. **Solução:** imponha a **Regra das Três Repetições** no metaprompt: nenhuma abstração antes de três ocorrências concretas.

### 5.2 O Acoplamento Implícito e o Paradigma do “Mau DRY”

A busca por compressão de tokens leva a IA a unificar conceitos logicamente independentes (ex.: `UserModel` da infraestrutura com `UserDTO` da API). Isso cria acoplamento onde as taxas de mudança são diferentes. **Prevenção:** separe por módulo e proíba o compartilhamento de tipos entre camadas com responsabilidades distintas.

### 5.3 A Degradação Sistêmica pelo Inchaço de Código (LLM Bloat)

A IA, por cegueira topológica, insere condicionais pesados em vez de reorganizar a estrutura. Isso aumenta a complexidade ciclomática e degrada performance (especialmente em I/O assíncrono). **Mitigação:** análise estática de complexidade e rejeição de código com alta complexidade.

---

## Capítulo 6: Framework Final – O Sistema Mestre de AI Coding (FCLM)

### 6.1 Checklist Operacional de Orquestração

Antes de permitir iterações autônomas, verifique:

1. [ ] Contexto minimalista (grafo restrito, nós parciais).
2. [ ] Saída com formato rígido (JSON com logit masking).
3. [ ] Prompt exige `<plan>` e `<reflection>`.
4. [ ] Testes arquiteturais (dependency‑cruiser, ArchUnit) armados na CI.

### 6.2 O Repositório Paramétrico: Templates de Interação Fundacional

#### Template Mestre de Controle Global (Axiomas e Guardrails)

```markdown
## Papel Permanente
Você opera como um Arquiteto de Software Sênior e Engenheiro Pragmatista focado na eliminação do overengineering. Atitude base: ceticismo construtivo. “O melhor software é zero software.”

## Regras Axiomáticas Inegociáveis (Akita Rules)
- **Isolamento de Estado:** código em `src/domain` é puro e imune a infraestrutura.
- **Simplicidade Radical:** Regra das Três Repetições é lei suprema.
- **Anti‑Alucinação Operativa:** não modifique mais de 50 linhas estruturais consecutivas sem pausar com “INTERVENÇÃO HUMANA REQUERIDA”.

## Formato de Refinamento Fixo
A sua mecânica final deve restringir explicações verbais, substituindo‑as apenas por diffs contínuos.
```

#### Template Operacional: Planejamento Preemptivo Multiagente

```markdown
<repository_map_topologico>
{{INSERIR_AST_OU_REPO_MAP}}
</repository_map_topologico>

<thinking>
1. QUAIS arquivos (paths exatos) requerem intervenção?
2. A alteração transgride fronteiras do sistema fatiado?
3. Gere pseudo‑algoritmo de orquestração.
</thinking>

[PAUSE para validação humana]
```

#### Template Estrito para Reflexão e Auto‑Crítica (Reflexion)

```markdown
Atue como Analista de Qualidade Code‑Reviewer. O código gerado abaixo deve ser criticado sob os anti‑patterns:
1. Criou acoplamento implícito (mau DRY)?
2. Há inchaço processual?
3. Alucinou parâmetros inexistentes?

Retorne JSON:
{"status": "APROVADO", "motivo_congruencia": "..."}
ou
{"correcoes_necessarias_criticas": [...]}
```

---

## Capítulo 7: Análise Comparativa Profissional das Malhas Conexionistas (Claude, Gemini e GPT)

| Atributo | Claude 3.5 Sonnet | OpenAI GPT‑4o | Google Gemini 1.5 Pro |
|----------|-------------------|---------------|------------------------|
| **Arquitetura Cognitiva** | Maestria em lógica semântica, alta resiliência em bases extensas. 64% em agentic evaluation. | Velocidade e capacidade analítico‑dedutiva (76.6% MATH zero‑shot). | Mixture of Experts, memória atencional de até 2M tokens. |
| **Vantagens Pragmáticas** | Refatoração não‑destrutiva, aderência ao estilo da codebase. | TTFT até 2x mais rápido, ideal para automações paralelas. | Escala brutal: engole 30k+ linhas sem RAG. |
| **Defeitos Orgânicos** | Bloqueios por alinhamento excessivo, recusas infundadas. | Preguiça (comprime lógica com comentários “// resto da implementação”). | Latência, diluição de diretivas cruciais. |
| **Estratégia de Prompt Recomendada** | Agente Construtor Central e Revisor (Reflexion). | Trabalhador de Velocidade (automações paralelas). | Mente Coletiva Planejadora (Plan‑and‑Execute, RAG nativo). |

---

## Conclusões Arquiteturais

A introdução de LLMs na codificação não dilui o rigor da engenharia, mas o exacerba. O “vibe coding” leva ao colapso escalar. O domínio da tecnologia exige:

- Refugo metódico de falsas abstrações.
- Imposição matemática de isolamentos (logit masking).
- Dinâmicas cibernéticas de agentes restritos.
- Ancoragem em princípios tangíveis (Akita Rules) e validação automatizada (dependency‑cruiser, ArchUnit).

Sob essa ótica, a IA torna‑se uma forja de produtividade estruturada, e o desenvolvedor sênior, o verdadeiro **Orquestrador da Complexidade**.

---

## Fonte

- **PDF Original:** Tratado Técnico AI Coding Avançado.pdf
- **Skill gerada automaticamente** com preservação máxima de conteúdo.