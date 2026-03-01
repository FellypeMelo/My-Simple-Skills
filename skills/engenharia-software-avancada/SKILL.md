# Engenharia de Software Avançada – Skill para LLM

## Identificação

- **Nome:** `engenharia-software-avancada`
- **Descrição:** Tratado abrangente de engenharia de software avançada cobrindo SOLID, Clean Code, padrões de projeto, arquiteturas distribuídas, DevOps, observabilidade e práticas de excelência em engenharia.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **engenharia de software de alta performance**, incluindo tópicos clássicos e contemporâneos, com ênfase especial na integração com Inteligência Artificial para geração e validação de código.

### Escopo do conhecimento

- Fundamentos matemáticos (complexidade assintótica, Big‑O, análise amortizada, modelos de computação)
- Estruturas de dados profundas (arrays, listas, hash tables, árvores balanceadas, grafos, heaps, B‑Trees, Skip Lists)
- Algoritmos essenciais e avançados (ordenação, busca, programação dinâmica, algoritmos em grafos, gulosos, backtracking, divisão e conquista)
- Design Patterns (GoF e modernos para cloud‑native: Saga, Outbox, Sidecar, Circuit Breaker)
- Clean Code profundo (SOLID, heurísticas, qualidade automatizável)
- Clean Architecture + engenharia moderna (separação de camadas, dependência invertida, pragmatismo)
- Engenharia de prompt para AI coding (metodologia BAVS, templates)
- Anti‑patterns em AI coding (falsas abstrações, dependências alucinadas, happy path fallacy)
- Sistema Mestre de Codificação com IA (pipeline ABIV, template universal)

### Como usar este conhecimento

1. **Diagnóstico da necessidade**  
   - Identifique se a questão envolve teoria de algoritmos, decisões arquiteturais, boas práticas de código, ou uso de IA para gerar/refatorar código.
   - Classifique a profundidade requerida: desde uma explicação conceitual até a implementação concreta com análise de complexidade.

2. **Aplicação dos princípios**  
   - Sempre que possível, relacione a resposta aos fundamentos matemáticos (Big‑O, análise amortizada) e aos padrões de design apropriados.
   - Para questões de código gerado por IA, utilize os anti‑patterns e as diretrizes de prompt engineering (BAVS) para sugerir correções e evitar armadilhas.
   - Ao recomendar arquiteturas, privilegie simplicidade (KISS, YAGNI) e isolamento de camadas (Clean Architecture).

3. **Estrutura de resposta recomendada**  
   - Comece com uma visão de alto nível ou definição.
   - Se relevante, apresente a notação matemática ou a complexidade envolvida.
   - Inclua exemplos de código (bem formatados) que ilustrem a aplicação correta.
   - Finalize com referências cruzadas aos tópicos do tratado (ex.: “conforme discutido na Parte 4, o padrão Outbox…”).

4. **Validação e boas práticas**  
   - Ao lidar com IA, lembre‑se de que o código gerado pode conter erros sutis; oriente o usuário a aplicar os checklists de qualidade (Parte 5 e Parte 9).
   - Reforce a necessidade de testes, mutation testing e validação de dependências.

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- Análise de complexidade de algoritmos (Big‑O, Ω, Θ, little‑o)
- Estruturas de dados (arrays, listas, hash tables, árvores AVL, Red‑Black, grafos, heaps, B‑Trees)
- Algoritmos de ordenação, busca, programação dinâmica, grafos (Tarjan, Dijkstra, etc.)
- Design patterns (GoF, Saga, Outbox, Sidecar, Circuit Breaker)
- Clean Code, SOLID, princípios de design (KISS, YAGNI, DRY)
- Arquitetura de software (Clean Architecture, microsserviços, cloud‑native)
- Engenharia de prompt para código com IA (BAVS, templates)
- Anti‑patterns em código gerado por IA (overengineering, dependências alucinadas, testes de happy path)
- Ferramentas de IA para codificação (Copilot, Cursor, Claude Code) e como usá‑las com rigor técnico
- Revisão de código, refatoração, dívida técnica

**Palavras‑chave:** engenharia de software, SOLID, clean code, padrões de projeto, design patterns, arquitetura distribuída, DevOps, observabilidade, complexidade assintótica, Big‑O, análise amortizada, estrutura de dados, algoritmos, programação dinâmica, árvores balanceadas, Red‑Black, AVL, hash table, B‑Tree, Skip List, grafo, Tarjan, Saga, Outbox, Sidecar, Circuit Breaker, Clean Architecture, prompt engineering, BAVS, AI coding, vibe coding, anti‑patterns, overengineering, dependências alucinadas, mutation testing.

---

## Conteúdo Completo

### Sumário

- **PARTE 1 — Fundamentos Matemáticos e Teóricos**
- **PARTE 2 — Estruturas de Dados Profundas**
- **PARTE 3 — Algoritmos Essenciais e Avançados**
- **PARTE 4 — Design Patterns (GoF e Modernos)**
- **PARTE 5 — Clean Code Profundo**
- **PARTE 6 — Clean Architecture + Engenharia Moderna**
- **PARTE 7 — Engenharia de Prompt para AI Coding**
- **PARTE 8 — Anti-Patterns em AI Coding**
- **PARTE 9 — Sistema Mestre de Codificação com IA**

---

## PARTE 1 — Fundamentos Matemáticos e Teóricos

A engenharia de software de alta performance contemporânea exige uma compreensão rigorosa dos limites computacionais. Com o advento da Inteligência Artificial (IA) atuando como copiloto ou agente autônomo na geração de código, a responsabilidade do arquiteto de software desloca-se da mera digitação de sintaxe para a validação matemática e estrutural das soluções propostas.

### 1. Notação Big-O, Complexidade Assintótica e Análise Rigorosa

A análise assintótica é o modelo mental primário que previne falhas sistêmicas em escala. Formalmente, a notação Big-O (ou Símbolo de Landau) descreve o limite superior do crescimento de uma função de complexidade:

\[
f(n) = O(g(n)) \iff \exists c > 0, n_0 > 0 \text{ tal que } 0 \leq f(n) \leq c \cdot g(n) \ \forall n \geq n_0.
\]

Além de Big-O, outras notações são essenciais:

- **Ômega (Ω):** limite inferior, \( f(n) = \Omega(g(n)) \) se existem constantes \(c, n_0\) tais que \(f(n) \geq c \cdot g(n)\) para \(n \geq n_0\).
- **Teta (Θ):** limite justo, \(f(n) = \Theta(g(n))\) se \(f(n) = O(g(n))\) e \(f(n) = \Omega(g(n))\).
- **Little-o (o):** limite superior não justo, \(f(n) = o(g(n))\) se \(\lim_{n \to \infty} f(n)/g(n) = 0\).

Ao solicitar otimizações a agentes de IA, o arquiteto deve exigir provas matemáticas utilizando o espectro completo dessas notações. Por exemplo, uma implementação ingênua de QuickSort pode ser apresentada como \(O(n \log n)\) em média, mas omitir o pior caso \(O(n^2)\).

### 2. Análise Amortizada e o Método do Potencial

Para estruturas dinâmicas, a análise de pior caso operação a operação é excessivamente pessimista. O **Método do Potencial** prova limites amortizados:

\[
\text{custo amortizado} = \text{custo real} + \Delta \text{potencial}.
\]

**Exemplo: Inserção em um array dinâmico**  
Definimos o potencial \(\Phi = |2 \cdot \text{tamanho} - \text{capacidade}|\).  
- Inserção sem realocação: custo real = 1, \(\Delta\Phi = 2\) → amortizado = 3.  
- Inserção com realocação (dobro): custo real = \(n+1\), \(\Delta\Phi = -n\) → amortizado = 1.  
Portanto, o custo amortizado é \(O(1)\). IAs frequentemente sugerem incrementos lineares de capacidade, violando essa prova e degradando performance.

### 3. Modelos de Computação e Trade-offs Algorítmicos

A IA tende a gerar algoritmos ótimos no modelo RAM (acesso de memória constante). No entanto, o hardware moderno possui hierarquias de cache. Surge o trade-off entre algoritmos **Cache-Aware** (parametrizados para tamanhos de cache) e **Cache-Oblivious** (eficientes assintoticamente independentes do cache). Na prática, algoritmos Cache-Aware iterativos podem superar os recursivos Cache-Oblivious devido a overhead de chamadas de função e localidade.

| Característica           | RAM-based (ingênuo) | Cache-Aware      | Cache-Oblivious          |
|--------------------------|----------------------|------------------|--------------------------|
| Acesso a memória         | Assumido constante   | Otimizado com parâmetros fixos | Otimizado via divisão recursiva |
| Complexidade de implementação | Baixa            | Média (requer tuning) | Alta (matemática profunda) |
| Desempenho (dados em RAM) | Bom                 | Excelente        | Subótimo devido a overheads |
| Desempenho (dados > RAM) | Degradação catastrófica | Bom (se reconfigurado) | Excelente |

### 4. Casos Reais de Falha por Complexidade

Ignorar a complexidade estrutural e confiar cegamente em IA pode levar a desastres. Exemplos notórios:  
- Escândalo do Horizon (UK Post Office): erros lógicos em cálculos de saldo.  
- TUI Airlines: classificação incorreta de passageiros subestimando peso da aeronave.  
- Citibank: transferência errônea de US$900 milhões devido a falha de interface e validação.

Esses casos reforçam que algoritmos não existem no vácuo; a validação humana rigorosa é indispensável.

---

## PARTE 2 — Estruturas de Dados Profundas

O domínio sobre implementações de baixo nível de estruturas de dados separa arquitetos principais de engenheiros que dependem exclusivamente de “vibe coding”.

### 1. Arrays, Listas Encadeadas, Pilhas e Filas

- **Arrays:** acesso \(O(1)\), localidade espacial máxima, mas inserções/remoções no meio são \(O(n)\).
- **Listas encadeadas:** inserções/remoções \(O(1)\) se o nó for conhecido, mas travessia \(O(n)\) com muitos cache misses.
- **Pilhas (LIFO) e Filas (FIFO):** abstrações sobre essas estruturas.

**Erro comum de IA:** ao implementar listas duplamente encadeadas em Rust ou C++, manipulação incorreta de ponteiros, gerando ciclos de referência. Solução: usar índices de vetores (arena allocation) em vez de ponteiros brutos.

### 2. Hash Tables

Entregam busca \(O(1)\) amortizado. Componentes críticos: função de hash e estratégia de resolução de colisões (encadeamento separado vs. endereçamento aberto). IAs frequentemente usam bloqueios globais em versões concorrentes. Para forçar correção, solicitar “locks finos por bucket (lock striping) ou algoritmos lock-free baseados em CAS”.

### 3. Árvores Balanceadas: BST, AVL e Red-Black (RB)

- **BST:** pode degenerar para lista linear.
- **AVL:** diferença de altura ≤ 1, altura máxima \(\approx 1.44 \log n\), buscas mais rápidas.
- **Red-Black:** critérios relaxados (caminho mais longo ≤ dobro do mais curto), altura ≤ \(2 \log n\), mas inserções e remoções mais rápidas (máximo 2 rotações por inserção, 3 por remoção).

IAs erram frequentemente na remoção de árvores RB, especialmente no caso “duplo preto”. Exemplo de código falho (inserção):

```typescript
function insertFixup(node) {
    while (node.parent.color === RED) {
        let uncle = getUncle(node);
        if (uncle.color === RED) {
            node.parent.color = BLACK;
            uncle.color = BLACK;
            // ERRO: esquece de colorir o avô de vermelho
            node = node.parent.parent;
        } else { /* rotações */ }
    }
}
```

**Prompt para correção:** descreva explicitamente os casos (tio vermelho, tio preto triângulo/linha) e assegure a propagação da recoloração até a raiz.

### 4. Grafos e Heaps

- **Grafos:** matriz de adjacência (densos, consultas \(O(1)\)) vs. lista de adjacência (esparsos).
- **Heaps:** acesso ao extremo \(O(1)\), inserção \(O(\log n)\). Erro comum: heapify construído em \(O(n \log n)\) em vez de \(O(n)\) (começar do último nó não‑folha).

### 5. Estruturas Avançadas: Skip Lists e B-Trees

- **B-Trees:** base de dados em bloco, alto grau de ramificação para minimizar acessos a disco.
- **Skip Lists:** equivalentes probabilísticos a árvores balanceadas, sem rotações. IAs tendem a usar tabelas hash em sistemas que exigem range queries, onde B-Trees ou Skip Graphs são mais adequadas.

---

## PARTE 3 — Algoritmos Essenciais e Avançados

### 1. Ordenação e Busca

- **Busca binária:** \(O(\log n)\). Cuidado com estouro de inteiros: `mid = low + (high - low) / 2`.
- **QuickSort:** alta localidade de cache, mas instável e pior caso \(O(n^2)\).
- **MergeSort:** estável, \(O(n \log n)\), mas espaço extra \(O(n)\).
- **HeapSort:** in-place, \(O(n \log n)\), mas má localidade de cache.

### 2. Programação Dinâmica (DP)

Princípio da subestrutura ótima. Complexidade típica \(O(n^2)\) ou \(O(n \cdot m)\). IAs tendem a usar recursão top-down que pode estourar pilha. Prompt estruturado:

> “Implemente o algoritmo Knapsack 0/1. Proíba recursão top-down. Utilize tabulação bottom-up otimizando espaço para um array unidimensional (\(O(W)\)).”

### 3. Algoritmos em Grafos: Componentes Fortemente Conexos (Tarjan)

Tarjan encontra SCCs em \(O(V+E)\). O erro clássico em código gerado por IA é a extração incorreta da pilha quando o nó é raiz. Exemplo falho:

```python
if ids[at] == low[at]:
    scc = []
    while stack[-1] != at:  # ERRO: não inclui o nó atual e pode não esvaziar corretamente
        node = stack.pop()
        onStack[node] = False
        scc.append(node)
```

Versão correta:

```python
if ids[at] == low[at]:
    scc = []
    while True:
        node = stack.pop()
        onStack[node] = False
        scc.append(node)
        if node == at:
            break
    result.append(scc)
```

### 4. Algoritmos Gulosos, Backtracking e Divide and Conquer

- **Guloso:** escolhas locais, ótimo apenas para problemas com propriedade de matroide. IAs frequentemente aplicam gulosos a problemas que exigem DP.
- **Backtracking:** constrói candidatos e retrocede.
- **Divide and Conquer:** ex.: Transformada Rápida de Fourier (FFT), análise via Teorema Mestre.

---

## PARTE 4 — Design Patterns (GoF e Modernos)

### 1. Criacionais, Estruturais e Comportamentais: Evolução

Os padrões da Gang of Four (1994) ainda são relevantes, mas devem ser aplicados com discernimento.  
- **Singleton:** hoje considerado anti‑pattern; prefira injeção de dependência.  
- **Observer:** evoluiu para programação reativa e event streaming.  
- **Decorator:** corresponde a Higher‑Order Components (React) ou decoradores nativos (Python/TypeScript).

### 2. Padrões Arquiteturais Modernos (Cloud-Native)

**Saga e Transactional Outbox**  
Em microsserviços, transações distribuídas exigem o padrão Saga: sequência de transações locais com compensações. O padrão Outbox garante que a publicação de eventos e a escrita no banco sejam atômicas: ambas na mesma transação local, com um relay (ex.: Debezium) publicando os eventos posteriormente.

Diagrama textual:

```
1. Inicia transação DB local
2. Salva pedido (estado PENDENTE)
3. Salva evento "PedidoCriado" na tabela Outbox
4. Commit da transação
   ↓
5. Leitura assíncrona do Outbox
   ↓
6. Distribui evento "PedidoCriado"
   ↓
7. Serviço de estoque recebe evento, atualiza estoque, salva evento na Outbox e publica.
```

**Sidecar e Circuit Breaker**  
- **Sidecar:** componente adjacente (ex.: proxy) que gerencia telemetria, mTLS, etc., sem poluir o código da aplicação.  
- **Circuit Breaker:** interrompe chamadas síncronas quando a taxa de erros ultrapassa um limite, permitindo recuperação.

### 3. Anti-Patterns e Complexidade Acidental Gerada por IA

IAs tendem a introduzir **complexidade acidental**: fábricas, classes abstratas e interfaces para problemas simples. Exemplo: para um cálculo de conversão de moeda, geram `AbstractCurrencyConverterFactoryImpl` em vez de uma função pura.

**Prompt preventivo:**  
> “Implemente a lógica de conversão de moeda. PROIBIÇÕES: Não utilize padrões criacionais (Factories, Builders, Abstract Classes). Aplique YAGNI rigorosamente. Mantenha o código procedimental ou métodos estáticos puros.”

---

## PARTE 5 — Clean Code Profundo

Clean code não é obsoleto na era da IA; tornou-se uma ferramenta estratégica para feedback rápido e alterações de baixo custo.

### 1. SOLID: Violações Clandestinas da IA

- **SRP:** cada classe deve ter um único motivo para mudar. IAs frequentemente violam ISP e DIP.

**Exemplo ruim (violação de ISP):**

```typescript
interface IMachineLearningPipeline {
    trainModel(data: Tensor): Model;
    evaluateMetrics(model: Model): Metrics;
    deployToKubernetes(model: Model): void; // Infraestrutura vazando para domínio!
}
```

**Refatoração com ISP:**

```typescript
interface IModelTrainingStrategy {
    train(data: Tensor): Model;
}
interface IModelEvaluator {
    evaluate(model: Model): Metrics;
}
interface IContainerDeployer {
    deploy(modelArtifact: Buffer): void;
}
```

### 2. Checklist de Qualidade Automatizável

- Funções com menos de 4 ramos lógicos.
- Classes com menos de 100-200 linhas.
- Injeção de dependência via construtores.
- Ausência de variáveis globais ou mutações inesperadas.
- Nomes que expressam intenção (evitar `list`, `tempObj`).
- Tratamento de erros com `Result<T,E>` em vez de `try/catch` silenciosos.

---

## PARTE 6 — Clean Architecture + Engenharia Moderna

Adota-se a **Arquitetura Pragmática**: retém princípios de isolamento e testabilidade, mas omite interfaces manuais supérfluas.

### 1. Separação de Camadas e Dependência Invertida

As dependências apontam para dentro (domínio). Nenhuma classe de domínio importa bibliotecas de rede, sistema de arquivos ou persistência.

**Modelo textual:**

```
=== FRONTEIRA DE ENTREGA ===
[ Interface de Usuário / APIs / Cron Jobs ] -> Traduz chamadas.

=== FRONTEIRA DE APLICAÇÃO ===
[ Use Cases (Orquestradores) ] -> Injetam repositórios; controlam fluxo.
          | (Dependência invertida via interfaces)
          v
=== FRONTEIRA DO DOMÍNIO ===
<- Puro, determinístico.

=== FRONTEIRA DE INFRAESTRUTURA ===
-> Implementam as interfaces dos use cases.
```

### 2. Estratégia para Forçar a IA a Respeitar Camadas

Definir regras em arquivos de memória do agente (ex.: `.cursorrules`):

> “DIRETRIZ DE ARQUITETURA: Toda a lógica em `src/domain` deve ser agnóstica de frameworks. Qualquer tentativa de adicionar `import axios`, `import mongoose` em um arquivo de domínio invalida a resposta. Adaptações de banco pertencem a `src/infrastructure/repositories`.”

---

## PARTE 7 — Engenharia de Prompt para AI Coding

### 1. O Pipeline BAVS (Blueprinting Algorítmico e Validação Socrática)

1. **Exigir Planejamento (Socratic Prompting):** antes do código, a IA debate falhas, custos assintóticos e justifica hipóteses.
2. **TDD Assistido (Spec-Driven Development):** testes funcionam como restrição final; o código só é gerado para passar nos testes.
3. **Self-Review Autônomo:** a IA critica sua própria implementação com base em heurísticas fornecidas.

### 2. Templates de Engenharia de Prompt Operacional

#### A. Template: Planejamento Algorítmico (Fase 1)

```
Atue como Arquiteto Distribuído Sênior. Nosso sistema enfrenta contenção em banco relacional durante atualizações massivas de inventário.
Não escreva código ainda. Conduza uma dialética. Analise o impacto em latência, consistência e concorrência das seguintes arquiteturas:
(a) Pessimistic Locking
(b) Optimistic Concurrency Control (OCC)
(c) Fila assíncrona (RabbitMQ)
Apresente um resumo comparativo com trade-offs teóricos e complexidade computacional. Confirme a compreensão antes de seguir.
```

#### B. Template: Implementação Isolada via TDD (Fase 2)

```
Construa o módulo InventoryPatcher aplicando a estratégia OCC decidida.
Regras:
1. Cumpra SRP estritamente.
2. Injete o cliente de banco; não use dependências globais.
3. Implemente primeiro os testes Jest cobrindo 3 casos de sucesso e 2 de falha (simulando colisão de versões).
4. Só produza o código fonte quando os testes refletirem uma especificação à prova de balas.
```

#### C. Template: Refatoração Guiada (Fase 3)

```
<INSERIR_CÓDIGO_AQUI>
[ALVO]: Refatorar para remover complexidade acidental.
- Quebre métodos com mais de 25 linhas com extrações de nome significativo.
- Aplique KISS e YAGNI: remova interfaces, classes abstratas ou builders supérfluos.
- Explique brevemente o custo computacional recuperado antes de expor o código modificado.
```

---

## PARTE 8 — Anti-Patterns em AI Coding

### 1. Falsas Abstrações e Overengineering

IAs geram milhares de linhas de abstrações desnecessárias (fábricas de fábricas). **Prevenção:** prompt com “Proibido antecipar recursos. Proibido estender classes a menos que 3 casos reais se beneficiem.”

### 2. Dependências Alucinadas e Violações de Segurança

IAs sugerem bibliotecas obscuras que podem não existir (risco de supply chain attack). Estudos indicam que até 45% do código gerado contém falhas de segurança. **Mitigação:** hooks de CI/CD que travam merges automáticos se manifestos de pacote forem alterados sem aprovação humana.

### 3. A Falácia da Confiança em Testes de Happy Path

IAs escrevem testes que validam apenas o caminho feliz, ignorando condições de corrida, exceções de hardware e valores nulos. **Prevenção:** exigir mutation testing e prompts adversariais: “Elabore testes que forcem gargalos assintóticos com entradas massivas maliciosas.”

---

## PARTE 9 — Sistema Mestre de Codificação com IA

### 1. O Pipeline Iterativo Ideal (Workflow ABIV)

1. **Modelagem Teórica (sem código):** humano submete premissas; IA valida viabilidade assintótica.
2. **Definição Contratual:** interfaces e especificações em Markdown; camadas de isolamento seladas.
3. **Mecânica Assistida e Geração (TDD):** IA gera testes; humano inspeciona; IA então gera código para passar nos testes.
4. **Self-Review de Complexidade:** IA auto‑avalia o código para garantir limites de memória e complexidade adequados.

### 2. Template Universal Master de Codificação

Insira este preâmbulo nas instruções globais do agente (Cursor, Copilot, Claude Code):

```
Você é um Distinguished Software Engineer. Sua capacidade será julgada pela aderência a:

1. RIGOR MATEMÁTICO: Sempre comente a complexidade Big-O e de memória em loops cruciais. Priorize modelos Cache-Aware.
2. SIMPLICIDADE BRUTAL: Rejeite padrões abstratos supérfluos. Princípios KISS e YAGNI.
3. INTEGRIDADE DE DOMÍNIO: Projeto usa Clean Architecture. Nenhum modelo de domínio pode ter ligações de infraestrutura (frameworks, DB, HTTP). Respeite fronteiras via Dependency Inversion.
4. INTEGRIDADE DE DEPENDÊNCIAS: Nunca adicione bibliotecas externas sem permissão.
5. RESILIÊNCIA E TRANSAÇÕES: Em microsserviços, considere falhas, retentativas, e use Outbox para mutações sensíveis.
6. METODOLOGIA DE ENTREGA: Execute etapas em partes lógicas isoladas. Pare e confirme abordagens antes de emitir milhares de linhas.
Concisão, performance sistêmica e segurança são suas únicas diretrizes.
```

### 3. Conclusão Final (Checklist Operacional)

Antes de mesclar código de IA na branch principal, verifique:

- [ ] A implementação algorítmica degenera com conjuntos de dados inesperados?
- [ ] O código contorna proteções de tipos e injeta vulnerabilidades (SQL, injeção de prompt)?
- [ ] O tratamento de interrupções (Circuit Breaker, timeouts) está adequado na camada de transporte?

---

## Fonte

- **PDF Original:** Tratado Técnico de Engenharia de Software Avançada.pdf
- **Skill gerada automaticamente** com preservação máxima de conteúdo.