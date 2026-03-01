# IA e Refatoração Cognitiva de Software – Skill para LLM

## Identificação

- **Nome:** `ia-refatoracao-cognitiva`
- **Descrição:** Técnicas avançadas de refatoração de software assistida por IA, incluindo análise de complexidade, detecção de anti‑padrões, migração de legacy code e estratégias cognitivas para melhoria contínua de código.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **refatoração de software com suporte de Inteligência Artificial**, especialmente em contextos de código legado, dívida técnica, arqueologia de código e preservação de intenção. Os tópicos abrangem:

- Leis de Lehman e evolução de software
- Arqueologia de software (escavação de intenção, reconstrução de design)
- Carga cognitiva e dívida epistêmica
- Complexidade ciclomática vs. complexidade cognitiva
- Dívida técnica semântica e decadência de conhecimento
- Decisão entre refatorar vs. reescrever (rewrite)
- Preservação comportamental e verificação formal
- Metodologias práticas para refatoração cognitiva (behavioral locking, blast radius, context packaging)
- Riscos de “refuctoring” e alucinações em refatoração automática
- Técnicas de prompt para refatoração (KERNEL)

### Como usar este conhecimento

1. **Diagnóstico da necessidade**  
   - Identifique se a questão envolve melhoria de código existente, migração de sistemas legados, redução de complexidade, ou análise de impacto de mudanças.
   - Verifique se o usuário busca orientação teórica (conceitos, métricas) ou prática (exemplos de refatoração, prompts).

2. **Aplicação dos princípios**  
   - Utilize as **Leis de Lehman** para contextualizar a inevitabilidade da refatoração e a necessidade de esforços explícitos de manutenção.
   - Para sistemas legados mal documentados, recomende abordagens de **arqueologia de software** (ex.: BlackBoxToBlueprint) onde a IA infere comportamento a partir de entradas/saídas.
   - Ao lidar com dívida técnica, diferencie **dívida visível** (código desorganizado) de **dívida semântica** (perda de significado) – e sugira técnicas de mitigação.
   - Para avaliar a complexidade, utilize **métricas de complexidade cognitiva** (SonarSource) em vez de apenas complexidade ciclomática.
   - Na decisão entre refatorar e reescrever, aplique os critérios do **tipping point** (perda de intenção, dependências emaranhadas, incompatibilidade arquitetural).
   - Sempre que possível, recomende o **padrão estrangulador (Strangler Pattern)** como meio‑termo.
   - Para garantir a preservação comportamental, oriente o uso de **testes de caracterização** (gerados por IA) e, em casos críticos, **verificação formal** com ferramentas como Astrogator, Coq/Lean.

3. **Estrutura de resposta recomendada**  
   - Comece com um resumo do conceito ou problema.
   - Se relevante, apresente tabelas (ex.: Leis de Lehman, métricas de complexidade, taxas de sucesso de IA em refatoração).
   - Forneça exemplos de prompts estruturados (ex.: usando o framework **KERNEL**).
   - Inclua alertas sobre riscos como **refuctoring** e dívida epistêmica.
   - Finalize com recomendações de workflow (ex.: os 5 passos da refatoração cognitiva).

4. **Validação e boas práticas**  
   - Lembre‑se de que a IA pode gerar código que parece correto mas contém suposições silenciosas; a revisão humana é indispensável.
   - Sempre que possível, exija **testes automatizados** antes e depois da refatoração.
   - Use **análise de raio de impacto (blast radius)** para conter mudanças arriscadas.
   - Promova **PRs de intenção única** para facilitar a revisão.

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- Refatoração de código, melhoria de legado, modernização de sistemas
- Leis de Lehman, evolução de software
- Arqueologia de software, reverse engineering
- Carga cognitiva do desenvolvedor, complexidade de código
- Dívida técnica (especialmente semântica), decadência de conhecimento
- Refatoração assistida por IA, ferramentas de IA para refatoração
- Decisão entre refatorar vs. reescrever
- Preservação comportamental, testes de caracterização, verificação formal
- Riscos de “vibe coding”, dívida epistêmica, “refuctoring”
- Técnicas de prompt para refatoração (KERNEL)
- Migração de COBOL, .NET Framework para .NET Core

**Palavras‑chave:** refatoração, refactoring, código legado, legacy code, complexidade ciclomática, complexidade cognitiva, anti‑padrões, code smells, melhoria contínua, cognitive refactoring, Leis de Lehman, arqueologia de software, dívida semântica, dívida epistêmica, estrangulador, strangler pattern, refuctoring, verificação formal, KERNEL, testes de caracterização.

---

## Conteúdo Completo

### 1. Fundamentos da Evolução de Software e o Imperativo da Refatoração

As **Leis de Lehman** (formuladas a partir de 1974) descrevem a dinâmica de sistemas de software do tipo E (Evolucionários), que estão integrados a ambientes humanos e sociais. Duas leis são particularmente relevantes para a refatoração:

| Lei | Descrição | Implicação |
|-----|-----------|------------|
| **Mudança Contínua** | Um sistema do tipo E deve ser continuamente adaptado, ou tornar‑se‑á insatisfatório. | A manutenção é a maior parte do custo do ciclo de vida. |
| **Complexidade Crescente** | A estrutura degrada‑se a cada nova funcionalidade, a menos que haja esforços explícitos de manutenção. | Refatoração periódica é obrigatória para evitar colapso. |

A refatoração, conforme definida por Opdyke (1992) e popularizada por Fowler, é a técnica disciplinada de reestruturar código existente **sem alterar seu comportamento externo**, melhorando atributos como legibilidade, manutenibilidade e extensibilidade.

A decisão estratégica entre **refatorar** (preservar o ativo) e **reescrever** (reconstruir do zero) é central. Reescritas têm histórico notório de falhas; a refatoração é geralmente o caminho de menor risco. No entanto, com a redução do custo de geração de código por IA, o cálculo econômico muda – surge o **ponto de inflexão (tipping point)**.

---

### 2. A IA como Arqueóloga de Software: Escavação e Reconstrução de Intenção

**Arqueologia de software** é o estudo de implementações legadas mal documentadas para manutenção e evolução. Enquanto a análise estática tradicional foca em regras sintáticas, a IA pode atuar como exploradora digital:

- **BlackBoxToBlueprint:** Agente IA trata o sistema legado como uma caixa‑preta, experimenta entradas e observa saídas para mapear limites de decisão e extrair árvores de decisão. Útil quando o código‑fonte está corrompido ou o conhecimento tribal foi perdido.
- **Mapeamento de fluxos e dependências ocultas:** IA analisa milhões de linhas, identifica âncoras de execução (APIs, consumidores de mensagens) e rastreia fluxos de dados, anotando semanticamente *por que* certos caminhos existem.

#### Recuperação de Intenção e Programação Intencional

A **Programação Intencional** (Charles Simonyi) propõe separar a intenção computacional (o *que* o programa deve fazer) dos detalhes de implementação (o *como*). A refatoração cognitiva busca inverter o processo: usar IA para identificar conceitos de domínio (ex.: `Debit`, `Credit`) diluídos em código de baixo nível, elevando a abstração e permitindo evolução independente da tecnologia.

---

### 3. Carga Cognitiva e a Dívida Epistêmica na Era da IA

A carga cognitiva é um dos maiores obstáculos à produtividade. O ser humano médio mantém cerca de **quatro blocos de informação** na memória de trabalho. Métodos longos e aninhados excedem esse limite. IA pode mitigar fornecendo resumos em linguagem natural, mas introduz um novo risco: a **dívida epistêmica**.

- **Dívida epistêmica:** Ocorre quando uma equipe entrega código que funciona e passa nos testes, mas ninguém consegue explicar ou defender tecnicamente. A IA cria uma “ilusão de competência” (vibe coding), gerando código com suposições silenciosas que passam despercebidas.
- Peter Naur (1985) argumentava que um programa é a **teoria** construída na mente dos desenvolvedores. Se a teoria desaparece, o código torna‑se “software morto”, impossível de evoluir sem risco catastrófico.

#### Métricas de Complexidade

| Métrica | Foco | Aplicação |
|---------|------|-----------|
| **Complexidade Ciclomática (McCabe)** | Número de caminhos de execução independentes. | Estratégia de testes, cobertura. |
| **Complexidade Cognitiva (SonarSource)** | Esforço mental para entender o fluxo de controle. Penaliza aninhamentos profundos e quebras de fluxo. | Melhoria da legibilidade, redução de bugs. |

Fórmula simplificada:

\[
CC_{\text{cognitiva}} = \sum_{i=1}^{n} \text{peso}(estrutura_i) \times (1 + profundidade_i)
\]

A refatoração cognitiva visa reduzir esse valor, transformando labirintos lógicos em sequências lineares de intenção clara.

---

### 4. Análise de Dívida Técnica Semântica e Decadência de Conhecimento

- **Dívida técnica tradicional:** visível (código desorganizado, falta de testes).
- **Dívida técnica semântica:** invisível – o sistema processa dados, mas o significado dos dados ou da lógica foi perdido ou alterado silenciosamente (**decadência semântica** ou *knowledge drift*).

Sintomas: reuniões intermináveis de esclarecimento, lógica reescrita repetidamente, perda de confiança nas saídas. No contexto da IA, a dívida semântica é amplificada por respostas “quase certas” que erodem a confiança a longo prazo.

**Exemplo clássico:** Migração de C para Python. C depende de overflow de inteiros (comportamento definido). Python usa inteiros de precisão arbitrária. A IA traduz sintaticamente, mas o comportamento de overflow desaparece – uma falha latente que pode surgir anos depois.

#### Camadas de Defesa (Semantic Firewall)

| Nível | Estratégia | Ferramentas |
|-------|------------|-------------|
| 1 – Sintaxe | Análise estática (SAST) com foco em padrões de alucinação. | Linters, SonarQube. |
| 2 – Intenção | Testes baseados em propriedades, definição de invariantes. | Hypothesis, FsCheck. |
| 3 – Stress | Fuzzing híbrido para bordas e race conditions. | LibFuzzer, AFL++. |
| 4 – Formal | Verificação formal, provas de equivalência. | Coq, Lean, Astrogator. |

---

### 5. Refatoração vs. Reescrita: O Tipping Point na Era da IA

Historicamente, a recomendação era “não reescreva do zero”. Com IA, o custo de geração de código caiu, alterando o cálculo. Sinais de que o sistema cruzou o limiar para reescrita:

- Intenção original completamente perdida (não há mais conhecimento tribal).
- Dependências tão emaranhadas que qualquer alteração causa efeito cascata incontrolável.
- Arquitetura incompatível com necessidades futuras (ex.: monólito síncrono para microsserviços orientados a eventos).
- Custo de re‑implementar via IA é menor que remendar o legado.

**Padrão Estrangulador (Strangler Pattern):** meio‑termo onde novas funcionalidades são construídas em torno do legado, substituindo‑o gradualmente.

#### O Risco do “Refuctoring”

“Refuctoring” é o ato de alterar código com intenção de refatorar, mas quebrando o comportamento silenciosamente. Acontece quando a IA, focada em métricas de “code health”, remove blocos aparentemente redundantes que tratam exceções críticas.

Taxas de sucesso de modelos de IA em refatorações complexas:

| Modelo | Sucesso (out‑of‑the‑box) | Sucesso com verificação de fatos |
|--------|---------------------------|----------------------------------|
| PaLM 2 (code) | 37,29% | > 96% |
| GPT‑3.5 | 30,26% | > 96% |
| GPT‑4 | marginalmente superior | > 98% |
| phind‑codellama | 18,14% | N/A |

A combinação com verificação (AST, testes automatizados) eleva a taxa para mais de 96%.

---

### 6. Preservação Comportamental via Verificação Formal

A preservação comportamental é o “voto de castidade” da refatoração. Para garantir em escala industrial, recorre‑se a métodos formais auxiliados por IA.

- **Astrogator:** Usa uma Linguagem de Consulta Formal (Formal Query Language) como ponte entre linguagem natural e especificação matemática. Um interpretador simbólico verifica equivalência entre implementação gerada e especificação.
- Particularmente eficaz para **DSLs** (linguagens de domínio específico), que têm semântica mais tratável.
- Verificação de equivalência simbólica prova que, para **todos** os inputs possíveis, o comportamento é idêntico – algo que testes de unidade tradicionais não podem garantir.
- Custo ainda alto (~9 linhas de prova por linha de código), mas IA está automatizando a geração de lemmas e táticas em assistentes como Rocq (ex‑Coq).

---

### 7. Metodologias Práticas para Refatoração Cognitiva

Workflow recomendado para arquitetos seniores:

1. **Bloqueio de Comportamento (Behavioral Locking):** Antes de tocar no código, gere testes de caracterização (com IA) que capturem o comportamento atual em resposta a fluxos de produção reais.
2. **Análise de Raio de Impacto (Blast Radius Analysis):** Use IA para mapear dependências do módulo a ser refatorado; isole a zona de impacto com segmentação de rede e identidade.
3. **Redução de PRs para “Intenção Única”:** Cada Pull Request deve ter um único objetivo claro (ex.: “extrair lógica de validação de impostos”) e ser pequeno o suficiente para revisão humana exaustiva.
4. **Embalagem de Contexto (Context Packaging):** Forneça à IA contexto rico: regras de negócio, padrões arquiteturais da empresa, restrições de segurança.
5. **Uso de Padrões de Prompt Estruturados:** Adote o framework **KERNEL**:
   - **K**eep it simple
   - **E**asy to verify
   - **R**eproducible
   - **N**arrow scope
   - **E**xplicit constraints
   - **L**ogical structure

---

### 8. Arqueologia em Sistemas Críticos: COBOL e .NET

- **COBOL:** IA pode ler milhões de linhas de código procedural e documentar fluxos de trabalho esquecidos, reduzindo projetos de anos para trimestres. Estratégia: traduzir lógica para linguagens modernas enquanto se criam *wrappers* de API para componentes legados que ainda não podem ser movidos (coexistência segura).
- **.NET Framework → .NET Core:** IA reduz tempo de desenvolvimento, mas exige que o desenvolvedor atue como “gerente de supervisão”. A verificação humana é inegociável, pois a IA pode sugerir APIs que não existem na versão alvo ou ignorar restrições de segurança.

---

### 9. Conclusão: O Arquiteto como Guardião da Intenção

A refatoração cognitiva representa a maturidade da engenharia de software na era da IA. O maior ativo de um sistema é a **intenção** que o gerou e a capacidade da equipe de compreendê‑lo e evoluí‑lo. A IA, como arqueóloga de software, fornece as lentes para enxergar através da entropia e recuperar o design perdido.

O rigor técnico exigido vai além de código limpo: demanda compreensão de métricas de carga cognitiva, dívida semântica e verificação formal. O arquiteto do futuro será avaliado pela clareza com que preserva e expressa a intenção do sistema, garantindo que a tecnologia sirva ao propósito do negócio sem se tornar um fardo cognitivo insustentável.

---

## Fonte

- **PDF Original:** IA e Refatoração Cognitiva de Software.pdf
- **Skill gerada automaticamente** com preservação máxima do conteúdo essencial.