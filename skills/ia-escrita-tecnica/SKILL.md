# IA para Escrita Técnica Avançada – Skill para LLM

## Identificação

- **Nome:** `ia-escrita-tecnica`
- **Descrição:** Técnicas de escrita técnica de alta qualidade assistida por IA. Cobre documentação de APIs, RFCs, guias de arquitetura, post‑mortems e comunicação técnica efetiva.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **escrita técnica assistida por Inteligência Artificial**, incluindo tópicos como:

- Documentação de APIs, RFCs, guias de arquitetura, post‑mortems, manuais técnicos
- Arquitetura da informação para documentação (grafos, knowledge graphs, embeddings)
- Manutenção de documentação viva (Docs‑as‑Code, sincronização contínua com código)
- Análise lógica de argumentos técnicos, detecção de lacunas (gap analysis)
- Engenharia de prompt para controle estilístico (tom, voz, persona)
- Métricas de qualidade e avaliação de documentos técnicos gerados por IA
- Governança, riscos e ética na automação de escrita técnica

### Como usar este conhecimento

1. **Diagnóstico da necessidade**  
   - Identifique se a questão envolve criação, revisão, estruturação ou manutenção de documentação técnica.
   - Determine o tipo de artefato desejado: documentação de API (OpenAPI/Swagger), RFC, guia de arquitetura, post‑mortem, manual de usuário, etc.
   - Verifique se o usuário precisa de orientação sobre boas práticas, templates, ou integração com ferramentas de IA.

2. **Aplicação dos princípios**  
   - Para **arquitetura da informação**, recomende o uso de **grafos de conhecimento** e **embeddings** para representar relações semânticas e dependências (ex.: D‑LLM, SurveyG).
   - Para **documentação viva**, adote o paradigma **Docs‑as‑Code** com integração CI/CD e agentes de IA que atualizam documentos a partir de mudanças no código (ex.: Mintlify, Kodesage).
   - Para **análise lógica**, utilize o framework **GAPMAP** (Toulmin‑Abductive Bucketed Inference) para estruturar argumentos e detectar lacunas de conhecimento.
   - Para **controle estilístico**, use frameworks de prompt como **COSTAR** (Context, Objective, Style, Tone, Audience, Response) e técnicas de **Chain‑of‑Thought** para garantir consistência.
   - Para **avaliação**, combine métricas automatizadas (fluência, aderência a templates) com revisão humana focada em nuances contextuais e ética.
   - Para **governança**, enfatize a segregação de dados, atribuição de fontes e aprovação humana para mudanças na “verdade fundamental”.

3. **Estrutura de resposta recomendada**  
   - Comece com uma visão geral do conceito ou problema.
   - Se relevante, apresente uma tabela comparativa (ex.: frameworks de prompt, tipos de arquitetura de informação).
   - Forneça exemplos de prompts bem estruturados para cada tarefa (ex.: “gere uma documentação de API seguindo o padrão OpenAPI”).
   - Inclua referências a casos de falha (ex.: desastres causados por documentação obsoleta) para reforçar a necessidade de rigor.
   - Finalize com recomendações de governança e checklist de validação.

4. **Validação e boas práticas**  
   - Lembre‑se de que a IA pode alucinar; sempre exija **atribuição de fontes** e **verificação humana** final.
   - Alerte contra a dependência excessiva de templates sintáticos que mascaram erros factuais.
   - Incentive o uso de **sistemas híbridos** onde a IA faz rascunhos e a equipe técnica valida e refina.
   - Aplique a regra dos **8%** : tarefas de precisão absoluta (ex.: códigos médicos) devem ser delegadas a sistemas determinísticos, não a LLMs.

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- Escrita técnica, documentação de software, manuais, guias
- Documentação de API, OpenAPI, Swagger, RFCs
- Post‑mortems, relatórios de incidentes
- Guias de arquitetura, documentação de infraestrutura
- Docs‑as‑Code, documentação viva, sincronização código‑documento
- Grafos de conhecimento, embeddings, RAG para documentação
- Engenharia de prompt para redação técnica (COSTAR, PTCF)
- Análise de argumentos, lacunas lógicas, consistência documental
- Avaliação de qualidade de documentação gerada por IA
- Governança de documentação com IA, riscos de alucinação

**Palavras‑chave:** escrita técnica, technical writing, documentação, API docs, RFCs, post‑mortems, comunicação técnica, documentation, Docs‑as‑Code, knowledge graph, embeddings, prompt engineering, COSTAR, Chain‑of‑Thought, GAPMAP, avaliação de IA, governança, alucinação.

---

## Conteúdo Completo

### Parte 1 – Arquitetura da Informação e Representação de Conhecimento

A base de qualquer sistema avançado de documentação técnica é a **arquitetura da informação**. Com a IA, essa arquitetura evolui de hierarquias lineares para **grafos de conhecimento** e **representações vetoriais**.

| Componente Arquitetural | Mecanismo | Benefício para Escrita Técnica |
|-------------------------|-----------|--------------------------------|
| **Grafos de Conhecimento (D‑LLM)** | Comunidades cognitivas interconectadas | Raciocínio multi‑salto, rastreio de dependências complexas |
| **Grafos de Citação Hierárquicos (SurveyG)** | Nós (documentos) e arestas (citações, similaridade) | Manutenção de rigor acadêmico em documentos longos |
| **Modelos de Traço (TraceLLM)** | Geração de grafos de chamadas de microsserviços | Documentação baseada em comportamento real, simulação |
| **Embeddings Vetoriais** | Codificação de texto em espaços de alta dimensão | Captura de relações semânticas latentes |
| **Mecanismos de Atenção** | Priorização de segmentos de entrada | Foco em informações críticas para a construção lógica |

**Aplicação prática:** Para documentar um sistema complexo, recomenda‑se a construção de um grafo de conhecimento que relacione componentes, APIs, dependências e decisões arquiteturais. A IA pode ser treinada para navegar nesse grafo e gerar explicações contextualmente precisas.

---

### Parte 2 – Documentação Viva e Ecossistemas Agênticos

O paradigma **Docs‑as‑Code** trata a documentação como código: versionada, revisada por pares e integrada a pipelines CI/CD. Agentes de IA monitoram mudanças no código e atualizam automaticamente a documentação correspondente.

| Prática | Fluxo de Trabalho | Impacto |
|---------|-------------------|---------|
| **Docs‑as‑Code Integrado** | Documentos no repositório Git, CI/CD valida e publica | Documentação sempre atualizada com o deploy |
| **Sincronização Agêntica** | Agentes analisam PRs e atualizam arquivos Markdown | Redução drástica de trabalho manual e dívida de documentação |
| **Visualização Dinâmica** | Mapeamento automático de dependências e serviços | Facilita onboarding e compreensão de sistemas complexos |
| **Revisão Transparente** | Ferramentas comparam versões e sugerem mudanças | Qualidade e conformidade mantidas |
| **Edição Visual para Não‑Devs** | Interfaces que geram PRs automaticamente | Democratização da contribuição |

**Ferramentas exemplares:** Mintlify, Kodesage, sistemas que integram LLMs para gerar documentação a partir de código.

---

### Parte 3 – Análise de Progressão Lógica e Inferência de Gaps de Conhecimento

A coerência lógica é vital na escrita técnica. O framework **GAPMAP** utiliza o esquema **TABI** (Toulmin‑Abductive Bucketed Inference) para estruturar argumentos:

- **Alegação (Claim)**
- **Fundamentos (Grounds)**
- **Garantia (Warrant)** – conexão lógica entre dados e conclusão

Essa estrutura força a IA a expor seu raciocínio, permitindo que revisores humanos identifiquem falhas lógicas ou evidências insuficientes. A **mineração de argumentos** (Argument Mining) extrai alegações, premissas e relações inferenciais de discursos técnicos, detectando contradições e contra‑evidências.

**Aplicação:** Ao redigir um post‑mortem ou RFC, exija que a IA justifique cada afirmação com fundamentos e garantias, facilitando a revisão crítica.

---

### Parte 4 – Engenharia de Prompt para Controle Estilístico e Normalização de Voz

O controle de estilo é alcançado por frameworks de prompt estruturados:

| Framework | Componentes | Aplicação |
|-----------|-------------|-----------|
| **COSTAR** | Contexto, Objetivo, Estilo, Tom, Audiência, Resposta | Definição de voz institucional |
| **PTCF** | Persona, Tarefa, Contexto, Formato | Redação de SOPs, RFCs com conformidade |
| **Chain‑of‑Thought** | Sequenciamento de passos de raciocínio | Explicação de processos complexos |
| **Few‑Shot** | Exemplos de referência no prompt | Padronização de terminologia |
| **Delimitadores Estruturais** | Tags como ### ou """ | Separação clara instrução‑dados |

**Personas específicas** (ex.: “redator técnico sênior seguindo normas GMP”) alinham a IA ao jargão e ética do domínio. **Regras do que fazer / não fazer** eliminam ambiguidades.

**Exemplo de prompt estilístico:**
```
Você é um redator técnico sênior especializado em documentação de APIs REST. Siga as diretrizes do Google Developer Documentation Style Guide. Reescreva o texto abaixo com tom neutro, voz ativa e precisão terminológica.
```

---

### Parte 5 – Métricas de Avaliação e Desempenho em Sistemas Híbridos

Avaliar sistemas híbridos exige métricas além da fluência linguística.

| Dimensão | Feedback Humano | Feedback IA | Implicação |
|----------|-----------------|-------------|------------|
| Legibilidade | Superior (direto) | Tendência à verbosidade | IA requer filtros de concisão |
| Especificidade Técnica | Limitada por fadiga | Alta e consistente | IA ideal para revisões em volume |
| Nuance Contextual | Insuperável | Limitada a padrões | Humanos validam casos de borda |
| Escalabilidade | Baixa | Extrema | IA permite feedback em tempo real |
| Risco de Alucinação | Baixo | Presente | Auditoria humana contínua necessária |

**Problema dos 8%:** LLMs falham em tarefas de precisão absoluta (ex.: códigos médicos). Enquanto a compreensão semântica pode ser alta (44%), a correspondência exata pode ser abismal (1,22%). Use IA para rascunho e estruturação; sistemas determinísticos para validação final.

---

### Parte 6 – Governança, Riscos e Ética da Automação

Riscos principais:
- **Alucinação confiante**: documentos com aparência autoritativa mas erros factuais.
- **Dependência de templates sintáticos**: repetição de padrões sem raciocínio real.
- **Perda do processo de escrita**: escrever é cristalizar o pensamento; delegar totalmente pode reduzir compreensão.

**Casos históricos de falha:**
- Colapso da torre de água (1973) – revisão de documento não aprovada.
- Erro bilionário em usina de aço – especificações obsoletas.

**Camadas de governança:**
1. **Segregação de Dados** – IA ancorada exclusivamente em dados proprietários aprovados.
2. **Atribuição de Fonte** – cada sugestão vinculada a um template, contrato ou regra.
3. **Controle Baseado em Funções** – apenas especialistas seniores atualizam a “verdade fundamental”.

**Recomendação final:** A IA transforma o redator técnico em um **arquiteto de conhecimento** e **editor de sistemas inteligentes**. As capacidades humanas de empatia, julgamento ético e responsabilidade permanecem insubstituíveis.

---

## Fonte

- **PDF Original:** IA para Escrita Técnica Avançada.pdf
- **Skill gerada automaticamente** com preservação máxima do conteúdo essencial.