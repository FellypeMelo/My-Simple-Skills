# XP com Agentes de IA – Skill para LLM

## Identificação

- **Nome:** `xp-agentes-ia`
- **Descrição:** Framework AI-XP (Artificially Intelligent eXtreme Programming) para pair programming com agentes de IA. Cobre orquestração multiagentes, TDD mandatório, Clean Architecture enforced, DevSecOps self-healing e métricas de qualidade.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **aplicação de Extreme Programming (XP) com agentes de IA**, incluindo tópicos como:

- Fundamentos da Engenharia de Software Agêntica (SE 3.0)
- Modelo AI-XP: loops VISION, ADAPT, LEAP
- Orquestração multiagentes (CrewAI, AutoGen, LangGraph)
- TDD agêntico (Red-Green-Refactor) e prevenção de poluição de contexto
- Engenharia de prompt para Clean Architecture e SOLID
- DevSecOps autônomo com remediação agêntica
- Anti-patterns de IA e dívida técnica induzida
- Métricas de produtividade e transição corporativa
- Pair programming humano‑IA (Driver/Navigator)

### Como usar este conhecimento

1. **Diagnóstico da necessidade**  
   - Identifique se a questão envolve metodologia ágil com IA, automação de testes, governança de código, segurança em pipelines, ou métricas de qualidade.
   - Determine se o usuário busca orientação conceitual (ex.: “como estruturar um time com agentes?”) ou prática (ex.: “como configurar um hook de TDD?”).

2. **Aplicação dos princípios**  
   - Para introdução ao paradigma, use a explicação da transição SE 2.0 → SE 3.0 e o problema do “vibe coding”.
   - Ao discutir orquestração, utilize a tabela comparativa de frameworks (CrewAI, AutoGen, LangGraph) e a topologia de esquadrão agêntico.
   - Para TDD agêntico, explique as fases RED, GREEN, REFACTOR com separação de agentes e o hook de pré‑commit que bloqueia código sem teste falho.
   - Na engenharia de prompt, apresente o padrão CRISPE, as “leis invioláveis” de Clean Architecture e o padrão de reflexão (auto‑auditoria).
   - Para DevSecOps, detalhe o fluxo de remediação autônoma: SAST/DAST → agente especialista → patch → revalidação → commit assinado.
   - Ao abordar anti‑patterns, use a tabela com cinco anomalias (Avoidance of Refactors, Bugs Déjà‑Vu, etc.) e suas estratégias de prevenção.
   - Nas métricas, refira‑se aos estudos (DORA 2025, GitClear, METR) e à tabela comparativa de abordagens (Manual XP, Vibe Coding, AI‑XP).
   - Para implementação, utilize o checklist exaustivo com 15 itens.

3. **Estrutura de resposta recomendada**  
   - Comece com um resumo do conceito ou problema (ex.: “O ‘vibe coding’ leva a dívida técnica; o AI‑XP aplica rigor do XP para domar agentes.”).
   - Se relevante, apresente tabelas comparativas (frameworks, anti‑patterns, métricas).
   - Forneça exemplos de código (YAML para hooks, JSON para configuração, TypeScript para script de validação).
   - Inclua diagramas textuais (como a topologia de esquadrão).
   - Finalize com recomendações de implementação e checklist corporativo.

4. **Validação e boas práticas**  
   - Lembre‑se de que a separação de contextos (Context Engineering) é crucial para evitar poluição de tokens.
   - O TDD deve ser mandatório e verificado por hooks; a fase RED deve ter um teste falho comprovado.
   - Em DevSecOps, o princípio de least privilege deve ser aplicado aos agentes.
   - Sempre enfatizar o papel humano como Navigator (orquestrador), mantendo o controle de decisões de negócio.

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- XP, Extreme Programming com IA
- Agentes de IA para programação em par (pair programming)
- TDD com IA, Red‑Green‑Refactor automatizado
- Orquestração multiagentes (CrewAI, AutoGen, LangGraph)
- Clean Architecture e SOLID enforced por IA
- DevSecOps autônomo, self‑healing, remediação de vulnerabilidades
- Dívida técnica induzida por IA, anti‑patterns de código gerado
- Métricas de produtividade com IA (DORA, GitClear, METR)
- Transição para SE 3.0 (Engenharia de Software Agêntica)
- Pair programming humano‑IA (Driver/Navigator)

**Palavras‑chave:** XP, extreme programming, agentes IA, pair programming, AI-XP, TDD mandatório, multiagentes, DevSecOps, orquestração, workflow agêntico, LangGraph, CrewAI, AutoGen, Clean Architecture, SOLID, contexto de engenharia, vibe coding, dívida técnica, métricas DORA.

---

## Conteúdo Completo

### 1. Fundamentos da Engenharia de Software Agêntica (SE 3.0)

A Engenharia de Software atravessa uma bifurcação evolutiva:

- **SE 1.0:** desenvolvimento puramente manual.
- **SE 2.0:** assistência por IA (copilotos reativos, autocompletar).
- **SE 3.0 (Engenharia Agêntica):** agentes autônomos que raciocinam sobre arquiteturas, orquestram ferramentas, debugam e validam implementações de forma semi‑independente.

O fenômeno do **“vibe coding”** (terceirização do julgamento técnico para a máquina sem restrições) resulta em código acoplado, inseguro e de difícil manutenção. Estudos mostram que, embora os desenvolvedores se sintam mais rápidos, a inserção descontrolada de agentes aumenta o tempo de revisão, o *code churn* e a densidade de bugs.

Para domar o determinismo estocástico dos LLMs, o **Extreme Programming (XP)** ressurge como camada de controle processual. A fusão originou o modelo **AI-XP**.

#### 1.1. O Modelo Estrutural AI-XP (Artificially Intelligent eXtreme Programming)

O AI-XP reimagina os pilares do desenvolvimento ágil através de três loops interconectados:

- **VISION:** planejamento de longo prazo e arquitetura de alto nível. Agentes analisam telemetria, documentação e conformidade para extrair épicos e ADRs (Architecture Decision Records).
- **ADAPT:** agilidade tática. IA avalia complexidade ciclomática e velocidade da equipe para distribuir tarefas preditivamente e refinar o backlog.
- **LEAP:** execução diária. Ferramentas de orquestração local (CLI de agentes) automatizam o desenvolvimento em pares com TDD, linters e validações de segurança.

**Dualidade humano‑máquina:**
- **Humano (Navigator):** detentor do contexto de negócios, tomador de decisões de risco, orquestrador.
- **Agente (Driver):** execução iterativa, digitação em alta velocidade.

---

### 2. Modelos Mentais de Orquestração e Topologias Multiagentes

O erro comum é tentar um “Super Agente Monolítico” com todo o contexto. A engenharia agêntica exige **Sistemas Multiagentes (MAS)** com fronteiras estritas de conhecimento e **Model Context Protocols (MCPs)** seletivos.

#### 2.1. Análise Comparativa de Frameworks de Orquestração

| Framework | Arquitetura | Modelo de Coordenação | Pontos Fortes no AI-XP | Limitações |
|-----------|-------------|------------------------|-------------------------|------------|
| **CrewAI** | Delegação baseada em papéis | Hierárquica (Manager/Worker) | Simula uma squad ágil; papéis e backstories restritos. | Inflexível para problemas não‑lineares; favorece sequências estritas. |
| **AutoGen (Microsoft)** | Conversacional (multi‑agent chat) | Peer‑to‑peer orgânico | Excelente para pair programming agêntico (Coder + Critic debatem refatorações). | Risco de loops infinitos e degradação de tokens se não houver restrições rígidas. |
| **LangGraph** | Máquina de estados (grafos cíclicos direcionados) | Controle determinístico com checkpoints | Controle absoluto, verificabilidade, time travel para rollbacks. Ideal para pipelines CI/CD. | Curva de aprendizado alta; exige engenharia de grafos. |

**Escolha ótima:** híbrido – LangGraph para o pipeline central (devido à recuperação determinística) e CrewAI para geração de artefatos paralelos no terminal do desenvolvedor.

#### 2.2. Diagrama Estrutural: Topologia de Esquadrão Agêntico

```
============================================================================
|                           ENGENHEIRO CHEFE (HUMANO)                      |
| - Define intenções de negócio (Spec-Driven Development)                 |
| - Aprova checkpoints de alto impacto                                    |
============================================================================
                                   |
                                   v
+----------------------------------------------------------------------------+
|                        AGENTE SUPERVISOR (ROUTER NODE)                     |
| - Analisa o StateGraph global e aloca sub‑tarefas                         |
| - LLM de inferência máxima (ex: Claude 3.7 Sonnet / GPT-4o)               |
| - Gerencia memória (sumariza eventos concluídos)                          |
+----------------------------------------------------------------------------+
                                   |
           +-----------------------+-----------------------+
           v                       v                       v
+---------------------+  +---------------------+  +---------------------+
|   ARCHITECT AGENT   |  |   TDD CODER AGENT   |  |  SEC/REVIEW AGENT   |
+---------------------+  +---------------------+  +---------------------+
| CONTEXTO ISOLADO:   |  | CONTEXTO ISOLADO:   |  | CONTEXTO ISOLADO:   |
| - Documentos C4      |  | - SOLID Rules       |  | - SAST Tools        |
| - OpenAPI Specs      |  | - AST Parser        |  | - OWASP Top 10      |
| - Bounded Contexts   |  | - Red-Green Loop    |  | - DAST Emulators    |
+---------------------+  +---------------------+  +---------------------+
         |                        |                        |
         v                        v                        v
+---------------------+  +---------------------+  +---------------------+
| Diagramas, Schemas  |  | PRs de Código       |  | Relatórios, Patches |
+---------------------+  +---------------------+  +---------------------+
```

**Princípio chave:** Separação de contexto. O TDD Coder Agent nunca enxerga os regulamentos completos de segurança; recebe apenas restrições filtradas pelo Sec/Review Agent. Isso previne fadiga do LLM e assegura controle estrutural.

---

### 3. O Ciclo TDD Agêntico (Red‑Green‑Refactor) e o Fim do “Vibe Coding”

O TDD é um protocolo fundamental de comunicação e segurança. Estudos (METR) mostram que desenvolvedores usando IA sem governança demoram até **19% mais** devido ao tempo gasto decifrando lógicas convolutas. O TDD resolve isso fornecendo um contrato executável.

#### 3.1. O Problema da Poluição de Contexto (Context Pollution)

Se um humano pede ao LLM, na mesma sessão, “crie os testes e depois a implementação”, ocorre **poluição de contexto**: o modelo concebe mentalmente o *happy path* da implementação antes de finalizar o teste, gerando testes tautológicos que apenas aprovam a implementação que ele já decidiu construir.

**Solução:** separar o ciclo Red‑Green‑Refactor em subagentes estanques e usar **pre‑commit hooks** que verificam a existência de um teste falho antes de permitir alterações no código de produção.

#### 3.2. Operacionalização do Fluxo Red‑Green‑Refactor

- **Fase RED (Write a Failing Test):**  
  O orquestrador delega especificações para o **Agente Analista de Testes**. Ele está proibido de modificar código de produção. Deve gerar testes focados em comportamento (ex.: Gherkin). A validação é a garantia de uma falha de asserção rigorosa (AssertionError).

- **Fase GREEN (Write the Minimum Code):**  
  O teste falho é passado ao **Agente Implementador**. Guiado por YAGNI, ele implementa o mínimo necessário para satisfazer o contrato. O feedback loop é mecânico: executa o motor de testes local (Pytest, Jest); se falhar, explica a falha, reverte ao último commit limpo e itera.

- **Fase REFACTOR (Improve the Design):**  
  Com a luz verde, o **Agente Refatorador** analisa complexidade ciclomática, remove duplicações, otimiza legibilidade. Se violar algum teste, ocorre reversão cibernética.

#### 3.3. Pipeline Prática: Hook de TDD para LLMs

Exemplo de configuração no Claude Code (`.claude/settings.json`) que bloqueia modificações de código sem cobertura RED:

```yaml
{
  "hooks": {
    "PreEditHook": [
      {
        "matcher": "src/domain/.*\\.(ts|py)$",
        "action": {
          "type": "command",
          "command": "npx tsx .claude/hooks/enforce-tdd-red-phase.ts",
          "timeout": 15
        }
      }
    ]
  }
}
```

O script `enforce-tdd-red-phase.ts` verifica:
- Se o arquivo solicitado (ex.: `UserService.ts`) tem um arquivo de teste correspondente (`UserService.spec.ts`).
- Se o teste falhou recentemente (timestamp e resultado do test runner).
- Se a precondição falhar, aborta a ação do agente e retorna erro no contexto:

```
<error>Protocolo XP Violado: FASE RED obrigatória. A implementação foi bloqueada.
Você deve gerar um teste falho antes de alterar a lógica de domínio.</error>
```

---

### 4. Engenharia de Prompt: Metodologia para Clean Architecture e Princípios SOLID

LLMs priorizam o caminho de menor resistência, gerando código acoplado. Para contrapor, adota‑se **Engenharia de Prompt Arquitetural** com o padrão **CRISPE** (Capacity, Role, Insight, Style, Persona, Example) e o **padrão de Reflexão** (auto‑crítica).

#### 4.1. Especificação Rigorosa de Arquitetura Limpa (System Prompt)

Exemplo de trecho de System Prompt para um Agente Implementador:

```
DOMAIN: Clean Architecture & SOLID Enforcer
Você é um Arquiteto de Sistemas Sênior. Produza código que siga irrefutavelmente a Clean Architecture.

LEIS INVIOLÁVEIS:
1. SOLID FIRST: Toda classe deve ter uma única razão para mudar (SRP). Nenhuma dependência concreta deve ser instanciada nas regras de negócio; use Injeção de Dependências por construtores vinculados a interfaces (DIP).
2. ISOLAMENTO DE DOMÍNIO: A camada de regras de negócio (Use Cases/Services) NÃO pode importar bibliotecas externas, frameworks web (Express/Axios) ou ORMs (Prisma/Hibernate). Comunicação via DTOs.
3. ALGORITHMIC ELEGANCE: Evite Hype-Driven Development. Nomes de variáveis altamente reveladores. Funções com no máximo 15 linhas lógicas. Use early returns.
4. VALUE OBJECTS: Nunca use tipos primitivos para identificadores, endereços ou cálculos monetários no Domínio. Encapsule em Value Objects com validação intrínseca.

PADRÃO DE REFLEXÃO (Auto-Auditoria Obrigatória):
Antes de consolidar a saída, rode internamente:
- [ ] Há bibliotecas de I/O vazando para o Domínio?
- [ ] O código permite fácil Mocking das interfaces?
- [ ] O nível de aninhamento (Nesting Depth) excede 2?
Se qualquer resposta for uma violação, destrua sua solução e reescreva‑a.
```

Este nível de parametrização transforma o comportamento heurístico do modelo.

---

### 5. DevSecOps, CI/CD Autônomo e Remediação Agêntica de Vulnerabilidades

Com o volume astronômico de código gerado, a revisão manual de segurança torna‑se gargalo. A solução é um pipeline **self‑healing** com remediação agêntica.

#### 5.1. Dinâmica do Pipeline Self-Healing

1. **Interceptação e Triagem:** Pull Request submetido → ferramenta SAST (SonarQube) ou SCA (Dependabot) detecta vulnerabilidade (ex.: hard‑coded secret, SQLi). Falha o fluxo.
2. **Roteamento para Agente Especialista:** Servidor CI empacota notificação de falha (JSON com CVE, árvore de execução, código fonte) e envia ao **Sec/Review Agent** (LangGraph/CrewAI).
3. **Correção em Linha (In‑line Fix):** Agente interpreta Policies as Code (OPA), reescreve a camada insegura do AST e injeta validação correta (ex.: substitui interpolação direta por parametrização).
4. **Revalidação Cruzada:** Agente despacha correção para o **Agente Testador** (TDD) que roda toda a suíte para garantir que o patch não violou funcionalidade.
5. **Audit Trail e Merge:** Após mitigação, agente consolida commit assinado com descrição rastreável (para conformidade com AI Act, SOC2). O PR é aprovado automaticamente ou sinalizado para revisão humana.

#### 5.2. Observabilidade Preditiva

Agentes monitoram telemetria (OpenTelemetry), rastreiam latências, saturação de recursos e comportamentos de falha. Em vez de alertas caóticos, criam hipóteses causais, isolam pods no Kubernetes e emitem PRs corretivos, exigindo apenas aprovação do SRE.

---

### 6. Arquitetura Evolutiva e Funções de Aptidão contra a Dívida Técnica Induzida por IA

Estudos (Ox Security, GitClear 2025) mostram que LLMs atuam como um “Exército de Juniores” em velocidade hiérsica, gerando **Dívida Técnica de IA (AITD)**. Sem supervisão, a complexidade explode.

#### 6.1. Catálogo de Anti‑Patterns Gerados por IA

| Anti‑Pattern | Causa | Detecção | Prevenção |
|--------------|-------|----------|-----------|
| **Avoidance of Refactors** | LLM adiciona if/else em vez de redesenhar | Complexidade ciclomática cresce; Manutenibilidade cai no SonarQube | Acoplar Lint ao agente; falhar task se complexidade > 15; exigir plano de extração |
| **Bugs Déjà‑Vu** | Cópia mental de código idêntico em vários módulos | Code duplication alta; AST semelhante em múltiplos locais | RAG com busca por intenção antes de implementar (DRY Enforcement) |
| **Over‑Specification** | Alucinações preventivas; código para cenários inexistentes | Code churn alto (código deletado semanas depois) | TDD estrito: gerar apenas o código necessário para passar no teste; YAGNI |
| **Return of Monoliths** | IA conecta web layer diretamente ao banco, ignorando microsserviços | Acoplamento direto de pacotes (ex.: JPA no Controller) | Injetar diagramas C4/OpenAPI no contexto para demarcar limites |
| **Comments Everywhere** | LLM insere comentários triviais para auxiliar seu próprio raciocínio | Poluição visual; densidade de legibilidade cai | Instrução de sistema: “Nunca comente o QUÊ; reserve comentários ao PORQUÊ” |

#### 6.2. Agentes de Modernização e Dívida Técnica

Usando **Funções de Aptidão (Fitness Functions)**, a equipe programa restrições corporativas. Agentes de refatoração, em horários de baixa carga, rastreiam dependências obsoletas, migram sintaxes defasadas, splitam classes e emitem PRs silenciosos, testados pelo TDD.

---

### 7. Análise de Métricas, Produtividade Empírica e a Transição Corporativa

#### 7.1. O Paradoxo da Produtividade de IA

| Métrica | Manual XP | Vibe Coding (SE 2.0) | AI‑XP Estruturado (SE 3.0) |
|---------|-----------|-----------------------|-----------------------------|
| Tempo de resolução de erros | Linha de base | Queda ilusória, gargalo em code review | Altamente previsível; auto‑reparável |
| Garantia arquitetural | Consistente | Acúmulo massivo de dívida | Contenção por Red‑Green‑Refactor; fitness functions |
| Volume de testes de qualidade | Fricção manual | Testes superficiais (tautológicos) | Cobertura algorítmica exaustiva; casos de borda previstos |
| Velocity end‑to‑end | Semanas/meses | Ilusão de alta performance; PRs 154% maiores, 91% mais tempo de revisão | Reduções tangíveis; ciclos fluidos |

**Estudos de caso:** Fintech CRED orquestrou Claude Code dentro de pipelines estritas de TDD e relatou **dobro de velocidade** sem degradação.

#### 7.2. Equipes Híbridas e Pair Programming

- **IA como Driver:** controle do teclado virtual; traduz requisitos validados, aplica conhecimento documentado.
- **Humano como Navigator:** engenheiro sênior transita para analista cognitivo – avalia o quadro arquitetural, dita refinamentos de prompt, orquestra time travel, impõe *human‑in‑the‑loop*.

#### 7.3. Checklist Exaustivo de Implementação Corporativa do AI-XP

**I. Precondições Estruturais e Dados**
- [ ] Metadados, diagramas C4, políticas estão formalizados e indexados para RAG?
- [ ] APIs permitem webhooks seguros bi‑direcionais para orquestração?

**II. Orquestração e Paradigma Multiagente**
- [ ] Framework de orquestração primário (LangGraph, CrewAI) foi selecionado?
- [ ] Partições lógicas multiagentes isolam informações críticas (Context Engineering)?

**III. Governança e Práticas AI-XP**
- [ ] Pipeline bloqueia modificação de arquivos de negócio a menos que teste associado falhe (Red Phase Constraint)?
- [ ] System Prompts mestres têm restrições explícitas de SOLID e Clean Architecture?
- [ ] Ferramentas de Linting e medição de complexidade forçam agentes refatoradores a simplificar?

**IV. Fluxos CI/CD e Proteção DevSecOps**
- [ ] Remediação autônoma configurada (alertas SAST/DAST invocam agente de segurança)?
- [ ] Princípio de least privilege aplicado na IaC (limitando blast radius)?
- [ ] Human‑in‑the‑loop Guardrails fixados antes da submissão à branch principal?

---

### 8. Conclusão

A fusão do formalismo do Extreme Programming com ecossistemas autônomos de IA (AI-XP) sinaliza o amadurecimento da Engenharia de Software Agêntica (SE 3.0). O “vibe coding” sem governança leva ao colapso arquitetural; a verdadeira produtividade exige submeter as capacidades estocásticas da máquina às amarras estruturais das metodologias clássicas.

Através dos loops VISION, ADAPT e LEAP, da orquestração multiagente, do TDD mandatório e da remediação autônoma de segurança, o AI-XP converte a IA em uma formidável linha de produção de software de classe empresarial: blindada de design à execução, ágil sob pressão e autônoma sem abdicar do controle humano.

---

## Fonte

- **PDF Original:** XP com Agentes de IA_ Tratado Técnico.pdf
- **Skill gerada automaticamente** com preservação máxima do conteúdo essencial.