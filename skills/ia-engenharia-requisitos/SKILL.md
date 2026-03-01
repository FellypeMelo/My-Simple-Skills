# IA na Engenharia de Requisitos – Skill para LLM

## Identificação

- **Nome:** `ia-engenharia-requisitos`
- **Descrição:** Guia completo de engenharia de requisitos assistida por IA. Inclui elicitação semântica, análise de ambiguidades, rastreabilidade, validação de requisitos não‑funcionais e frameworks de decomposição.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **engenharia de requisitos com suporte de Inteligência Artificial**, incluindo tópicos como:

- Tradução de necessidades de negócio em especificações técnicas
- Detecção e correção de ambiguidades em requisitos
- Uso de padrões (IEEE 29148, ISO/IEC 25010) para garantir qualidade
- Geração de User Stories e critérios de aceitação (BDD/Gherkin)
- Elicitação assistida por IA (mineração, simulação, reconstrução semântica)
- Análise de trade‑offs e conflitos entre requisitos
- Engenharia de prompt normativo para requisitos
- Anti‑padrões e maturidade na adoção de IA em requisitos

### Como usar este conhecimento

1. **Diagnóstico da necessidade**  
   - Identifique se a questão envolve fase de elicitação, especificação, validação ou gestão de requisitos.
   - Verifique se o usuário busca orientação teórica (conceitos, normas) ou prática (prompts, templates).

2. **Aplicação dos princípios**  
   - Utilize as normas **IEEE 29148** e **ISO/IEC 25010** como base para avaliar a qualidade dos requisitos.
   - Para elicitação, recomende técnicas de mineração semântica, simulação de stakeholders e reconstrução contextual.
   - Para análise de ambiguidade, aplique a taxonomia de Berry & Kamsties (léxica, sintática, semântica, pragmática).
   - Para especificação ágil, use o modelo **INVEST** e transforme requisitos em cenários **BDD** com Gherkin.
   - Para validação, utilize o framework **HARE‑SM** (Human‑AI Requirements Engineering Synergy Model) para manter o humano no comando.

3. **Estrutura de resposta recomendada**  
   - Comece com uma visão de alto nível do conceito ou problema.
   - Se relevante, apresente tabelas comparativas (ex.: custo de correção por fase).
   - Inclua exemplos de prompts bem estruturados para cada tarefa (elicitação, desambiguação, geração de critérios de aceitação).
   - Finalize com referências aos anti‑padrões e recomendações de governança.

4. **Validação e boas práticas**  
   - Lembre‑se de que a IA não substitui o julgamento humano; o modelo **HARE‑SM** reforça a supervisão contínua.
   - Alerte contra a **ilusão da exatidão inquestionável** e a **delegação excessiva de autonomia**.
   - Incentive o uso de **prompt chaining** e **rastreabilidade** (justificativas baseadas nas normas).

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- Engenharia de requisitos, especificação de software
- Elicitação de requisitos com IA
- Ambiguidade em requisitos, detecção de conflitos
- Requisitos não‑funcionais, atributos de qualidade (ISO 25010)
- User stories, INVEST, critérios de aceitação, BDD, Gherkin
- Normas IEEE 29148, IEEE 830, ISO/IEC 25010
- Trade‑off analysis, ATAM (indiretamente)
- Rastreabilidade, gestão de backlog
- IA generativa para documentação de requisitos
- Anti‑padrões em requisitos com IA, maturidade de adoção

**Palavras‑chave:** engenharia de requisitos, requirements engineering, elicitação, user stories, requisitos não‑funcionais, rastreabilidade, análise de requisitos, especificação, IEEE 29148, ISO 25010, INVEST, BDD, Gherkin, ambiguidade, trade‑off, HARE‑SM, AI‑MM, prompt engineering, anti‑padrões.

---

## Conteúdo Completo

### 1. A Crise Sistêmica dos Requisitos e o Custo da Má Qualidade

A engenharia de requisitos é o principal gargalo na construção de software. Dados do **Consortium for Information & Software Quality (CISQ)** indicam que a má qualidade de software custou US$ 2,41 trilhões apenas nos EUA em 2022. O **Chaos Report** do Standish Group mostra que 66%‑70% dos projetos falham ou são “desafiados”. A causa raiz não é técnica, mas sim a má gestão de requisitos: ambiguidade, falta de envolvimento do usuário, volatilidade do escopo e especificações pobres.

Casos emblemáticos (Citibank – US$ 900 milhões, CrowdStrike – 8,5 milhões de dispositivos afetados) ilustram o impacto de requisitos mal especificados.

#### A Regra de 100 (IBM/Barry Boehm)

| Fase do Ciclo de Vida        | Multiplicador de Custo |
|-------------------------------|------------------------|
| Elicitação/Design de Requisitos | 1x (base)             |
| Implementação/Codificação     | 10x                    |
| Testes de Sistema/Integração  | 100x                   |
| Produção/Pós‑lançamento       | 1000x+                 |

Quanto mais tarde um erro é detectado, mais caro é corrigi‑lo. A IA aplicada à engenharia de requisitos visa reduzir esses custos ao identificar problemas precocemente.

---

### 2. Fundamentos Normativos: IEEE 29148 e ISO/IEC 25010

Para que a IA atue com rigor, deve ser ancorada em padrões internacionais.

#### IEEE 29148:2018 – Processos e Produtos de Engenharia de Requisitos

Substitui o antigo IEEE 830. Define características obrigatórias de um requisito de qualidade:
- **Necessário**
- **Livre de Implementação** (o *quê*, não o *como*)
- **Não Ambíguo**
- **Consistente**
- **Completo**
- **Verificável / Testável**
- **Singular**
- **Viável**

Estabelece também a hierarquia de especificações:
- **BRS** (Business Requirements Specification)
- **StRS** (Stakeholder Requirements Specification)
- **SyRS** (System Requirements Specification)
- **SRS** (Software Requirements Specification)

#### ISO/IEC 25010:2023 – Modelo de Qualidade de Produto de Software

Define nove características de qualidade (e suas subcaracterísticas) para requisitos não‑funcionais:
1. **Adequação Funcional** (completude, corretude, adequação)
2. **Eficiência de Desempenho** (comportamento temporal, utilização de recursos, capacidade)
3. **Compatibilidade** (coexistência, interoperabilidade)
4. **Capacidade de Interação** (reconhecibilidade, apreensibilidade, operabilidade, proteção contra erros, engajamento, inclusividade, assistência)
5. **Confiabilidade** (maturidade, disponibilidade, tolerância a falhas, recuperabilidade)
6. **Segurança** (confidencialidade, integridade, não‑repúdio, responsabilidade, autenticidade, resistência)
7. **Manutenibilidade** (modularidade, reusabilidade, analisabilidade, modificabilidade, testabilidade)
8. **Flexibilidade** (adaptabilidade, instalabilidade, substituibilidade, escalabilidade)
9. **Segurança Crítica (Safety)** (restrições operacionais, identificação de riscos, fail‑safe, avisos de perigo, integração segura)

---

### 3. A Sinergia Humano‑IA: O Modelo HARE‑SM

Pesquisas de Stanford e Carnegie Mellon demonstraram que agentes de IA totalmente autônomos falham 32%‑49% mais que humanos, e a automação total desacelera o trabalho em 17,7% devido à sobrecarga de verificação. O modelo híbrido (humano‑no‑comando) supera os agentes autônomos em **68,7%** em precisão e qualidade.

O **Human‑AI Requirements Engineering Synergy Model (HARE‑SM)** posiciona a IA como sondas semânticas nas fases de alta carga de informação, enquanto o engenheiro humano atua como **árbitro contextual**, validando decisões, negociando trade‑offs e garantindo alinhamento ético.

---

### 4. Elicitação Assistida por IA

#### 4.1 Mineração Massiva e Extração Estruturada
- Técnicas de **NER (Named Entity Recognition)** e modelagem de tópicos constroem grafos de conhecimento a partir de atas, e‑mails, manuais e legislação.
- Geração automática de glossários e diagramas UML/SysML iniciais.

#### 4.2 Reconstrução Semântica e Contextualização Implícita
- LLMs pré‑treinados em vastos repositórios técnicos preenchem lacunas semânticas (ex.: ao ouvir “dashboard de fraudes”, sugerem implicitamente requisitos de segurança, auditoria e desempenho).
- Alertam sobre **NFRs** não mencionados, baseando‑se em melhores práticas.

#### 4.3 Simulação de Stakeholders (Role‑playing)
- Engenheiros treinam entrevistas com **personas virtuais** geradas por IA, que revelam omissões e fornecem requisitos conflitantes típicos do domínio.
- Maximiza o aproveitamento do tempo com stakeholders reais.

#### 4.4 Elicitação Contínua via UGC (User‑Generated Content)
- Análise de sentimentos em reviews, issue trackers e redes sociais para descobrir requisitos latentes em tempo real.

---

### 5. Detecção Automatizada de Ambiguidade e Conflitos

#### Taxonomia de Ambiguidade (Berry & Kamsties)
1. **Léxica** – homonímia, polissemia sistemática.
2. **Sintática / Estrutural** – ambiguidade de anexação, ambiguidade de coordenação.
3. **Semântica** – anáfora mal resolvida, escopo de quantificadores.
4. **Pragmática** – jargões vagos (“velozmente”, “robusto”), falta de métricas.

#### Evolução do NLP4RE
- Antigas ferramentas baseadas em regras (ARM, QuARS) tinham precisão limitada (41%‑68%) e muitos falsos positivos.
- Modelos atuais baseados em **Transformers** (BERT, Sentence Transformers) mapeiam sentenças em embeddings densos, detectando ambiguidades contextuais com alta acurácia.
- Podem ser integrados a pipelines CI/CD para validar pull requests de documentos.

#### Detecção de Conflitos (Trade‑off Analysis)
- Entre 40% e 60% dos requisitos em projetos complexos geram conflitos.
- IA aplica **clustering** e **Processos Analíticos Hierárquicos (AHP)** para identificar colisões entre NFRs (ex.: segurança máxima vs. latência mínima).
- Simula impactos no cronograma e recursos, transformando discussões políticas em decisões baseadas em evidências.

---

### 6. Geração Formal e Ágil: User Stories e BDD

#### User Stories com INVEST
- **I**ndependente
- **N**egociável
- **V**alioso
- **E**stimável
- **S**mall (tamanho adequado)
- **T**estável

IA pode reescrever histórias vagas (“gerenciar carrinho”) para atender a INVEST, subdividindo e refinando.

#### Critérios de Aceitação em BDD (Gherkin)
A IA transforma requisitos em cenários executáveis:

```gherkin
Funcionalidade: Exclusão de produto do carrinho
  Dado que o usuário está na página do carrinho
  E o carrinho contém um item "Laptop" com quantidade 1
  Quando o usuário clicar em "Remover"
  Então o item deve desaparecer da lista
  E o subtotal deve ser recalculado em menos de 1000ms
```

Isso elimina ambiguidades e fornece base para testes automatizados.

---

### 7. Engenharia de Prompt Normativo

Para que a IA respeite os padrões IEEE 29148 e ISO 25010, o prompt deve ser estruturado com:

1. **Ancoragem Contextual Obrigatória** – Injetar a taxonomia da ISO 25010 no prompt, exigindo que a análise seja feita sob suas categorias.
2. **Instruções Processuais de Refinamento Iterativo** – Usar **Chain‑of‑Thought** para que a IA analise ambiguidades, conflitos e só então gere artefatos.
3. **Exigência de Justificativa Rastreável** – Toda recomendação deve ser vinculada a cláusulas das normas.

**Exemplo de prompt normativo:**

```
Com base na ISO/IEC 25010:2023, identifique os requisitos não‑funcionais implícitos na seguinte declaração de necessidade: "O sistema de login deve ser rápido e seguro." Para cada NFR, especifique a categoria (ex.: Performance Efficiency – Time Behaviour) e a subcaracterística, e justifique com base na norma.
```

Estudos mostram que prompts normativos alcançam até 80,4% de concordância com classificações de especialistas.

---

### 8. Anti‑padrões e Maturidade na Adoção de IA

#### Anti‑padrões Críticos
1. **Ilusão da Exatidão Inquestionável** – Tratar a IA como oráculo infalível, ignorando sua natureza probabilística.
   - *Mitigação:* Manter humanos no loop (HITL), exigir justificativas rastreáveis.
2. **Delegação Excessiva de Autonomia** – Permitir que agentes modifiquem requisitos ou arquitetura sem supervisão.
   - *Mitigação:* Fluxos de trabalho com aprovação humana obrigatória.
3. **Desalinhamento Qualitativo e Prompt Drift** – Prompts não versionados e sem governança, levando a especificações “sombra”.
   - *Mitigação:* Controle de versão de prompts, auditoria de entradas e saídas.

#### Modelo de Maturidade de Adoção de IA (AI‑MM)
- **Nível 1 – Exploração Disforme:** Experimentos isolados, sem padrões.
- **Nível 2 – Implantação Direcionada:** Uso controlado em departamentos, primeiros ganhos.
- **Nível 3 – Alinhamento Tático:** Práticas definidas, templates baseados em normas.
- **Nível 4 – Escala Quantitativa:** Integração em pipelines, métricas de qualidade.
- **Nível 5 – Inovação Madura:** Melhoria contínua, antecipação proativa de problemas.

---

### 9. Conclusão

A engenharia de requisitos assistida por IA, quando ancorada em normas (IEEE 29148, ISO 25010) e estruturada por prompts normativos, transforma o caos da comunicação em especificações claras, testáveis e rastreáveis. O modelo **HARE‑SM** garante a sinergia humano‑IA, evitando os anti‑padrões de autonomia excessiva e viés de automação. O caminho para a excelência passa pela adoção gradual dos níveis de maturidade (AI‑MM), culminando em organizações onde a IA potencializa, mas não substitui, o julgamento crítico do engenheiro de requisitos.

---

## Fonte

- **PDF Original:** IA na Engenharia de Requisitos_ Guia Detalhado.pdf
- **Skill gerada automaticamente** com preservação máxima do conteúdo essencial.