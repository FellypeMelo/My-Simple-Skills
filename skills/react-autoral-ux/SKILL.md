# Arquitetura React Autoral e UX Experimental – Skill para LLM

## Identificação

- **Nome:** `react-autoral-ux`
- **Descrição:** Arquitetura React avançada com foco em UX experimental. Cobre padrões autorais de componentes, design systems não‑convencionais, animações, micro‑interações, acessibilidade e performance perceptual.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre **arquitetura React de alta identidade, UX experimental e design system autoral**, incluindo tópicos como:

- Rejeição de antipadrões (bibliotecas monolíticas, templates genéricos)
- Filosofias visuais: Neo‑Brutalismo, Neo‑Editorial
- Tipografia e espaçamento com rigor editorial
- Acessibilidade em interfaces não‑convencionais
- Manifesto UX com 10 regras arquitetônicas (supremacia do teclado, gestão de foco, cinética, etc.)
- Padrões de componentes: composição, Headless UI, estrutura de diretórios
- Design Tokens e CSS Custom Properties com Cascade Layers
- React Compiler e Signals para performance extrema
- Construção de telas complexas: Bento Grid, animações (Framer Motion), renderização de alta densidade (SVG vs. WebGL)
- Integração de conceitos estéticos, funcionais e técnicos

### Como usar este conhecimento

1. **Diagnóstico da necessidade**  
   - Identifique se a questão envolve design de componentes, escolha de bibliotecas, performance de renderização, acessibilidade, ou conceitos de UX experimental.
   - Determine se o usuário busca orientação conceitual (princípios de design) ou prática (implementação, código).

2. **Aplicação dos princípios**  
   - Para escolhas arquiteturais, use a crítica aos antipadrões (dependência de UI monolíticas, templates genéricos) como base para recomendar soluções autorais.
   - Ao discutir estética, recorra à fusão Neo‑Brutalista/Neo‑Editorial: honestidade estrutural, contraste deliberado, exposição crua de elementos interativos.
   - Para tipografia, aplique as regras editoriais: tamanho base ≥16px, espaçamento vertical mínimo de 1em, proibição de justificação, balanceamento de rags.
   - Em acessibilidade, destaque que o design brutalista não é hostil quando cores têm alto contraste (>4.5:1) e o DOM é semântico.
   - Use o **Manifesto UX** de 10 regras como checklist para projetar interações táticas (ex.: sempre priorizar atalhos de teclado, gerenciar foco deterministicamente).
   - Para componentes, defenda a **composição sobre herança**, o padrão **Headless UI** (separação entre lógica e apresentação) e a estrutura de diretórios co‑localizada.
   - Para estilos, empregue **Design Tokens** em três camadas (primitivos, semânticos, componentes) e **Cascade Layers** para controle de especificidade.
   - Em performance, explique a transição do uso manual de `useMemo`/`useCallback` para o **React Compiler** (memoização automática) e a adoção de **Signals** para dados de altíssima frequência.
   - Para telas densas, recomende **Bento Grid** com bordas rígidas, **Framer Motion** com física de molas, e renderização via **WebGL** (ex.: LightningChart) para milhões de pontos de dados.

3. **Estrutura de resposta recomendada**  
   - Comece com um resumo do conceito ou problema (ex.: “A fadiga de templates exige uma abordagem autoral…”).
   - Se relevante, apresente tabelas comparativas (ex.: estado React vs. Signals, camadas de tokens).
   - Forneça exemplos de código (JSX/TS) ou de configuração (CSS, tokens) para ilustrar.
   - Inclua alertas sobre armadilhas comuns (ex.: animações bloqueando a main thread, má gestão de foco).
   - Finalize com referências aos princípios do manifesto ou à integração arquitetônica global.

4. **Validação e boas práticas**  
   - Reforce que a identidade visual não deve comprometer acessibilidade ou performance.
   - Lembre‑se de que o React Compiler ainda é uma ferramenta em evolução; em casos extremos, Signals podem ser necessários.
   - Sempre recomende testar em dispositivos reais para verificar fluidez (60‑120 FPS).

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- React, arquitetura de componentes, design system
- UX experimental, interfaces não‑convencionais
- Neo‑Brutalismo digital, design Neo‑Editorial
- Tipografia responsiva, espaçamento editorial
- Acessibilidade em design autoral
- Padrões de componentes: Headless UI, render props, composição
- Estrutura de diretórios em larga escala
- CSS Custom Properties, Design Tokens, Cascade Layers
- React Compiler, Signals, performance de renderização
- Bento Grid, Framer Motion, animações com spring
- Renderização de alta densidade (WebGL, Canvas, SVG)
- Manifesto UX, interações táticas (keyboard‑first)

**Palavras‑chave:** React, UX experimental, design system, componentes, animações, micro‑interações, acessibilidade, performance, frontend, arquitetura React, Neo‑Brutalismo, Neo‑Editorial, Headless UI, Design Tokens, CSS Cascade Layers, React Compiler, Signals, Bento Grid, Framer Motion, WebGL, keyboard‑first.

---

## Conteúdo Completo

### Parte 1 – A Desconstrução do Paradigma Atual e a Eliminação de Antipadrões

A paisagem digital contemporânea, particularmente em produtos SaaS, atingiu um ponto crítico de saturação estética e estagnação funcional. A proliferação de bibliotecas de componentes genéricas, frameworks utilitários e templates pré‑fabricados estabeleceu um padrão de mediocridade visual, onde a eficiência na entrega substituiu a autoria e a inovação. Esse fenômeno é conhecido como **fadiga de templates** (*template fatigue*).

**Antipadrões a serem eliminados:**

- **Dependência crônica de frameworks de UI monolíticos e acoplados:** impedem a inovação na camada tática, misturando estado, acessibilidade e apresentação de forma rígida.
- **Arquitetura de dados baseada na exibição massiva e indiscriminada:** leva à paralisia analítica. A solução é a **revelação progressiva** (*progressive disclosure*), revelando informações incrementalmente.

A resposta arquitetônica exige experiências hiper‑personalizadas, micro‑interações funcionais e eliminação de ruído visual que não contribui para a tarefa.

---

### Parte 2 – Sistema de Identidade Visual: Neo‑Brutalismo e Design Neo‑Editorial

A filosofia visual funde os princípios audaciosos do **Neo‑Brutalismo digital** com a precisão rigorosa do **design Neo‑Editorial**.

- **Neo‑Brutalismo:** exposição crua dos elementos interativos, assimetria controlada, paletas de alto contraste, bordas rígidas, sombras duras. Inspirado no *béton brut* (concreto aparente) da arquitetura pós‑guerra.
- **Design Neo‑Editorial:** tipografia como elemento arquitetônico principal, regras estritas de composição herdadas do design impresso.

**Regras tipográficas:**

- Tamanho base ≥16px (ou referências relativas superiores).
- Espaçamento vertical mínimo de 1em entre blocos lógicos.
- **Proibição de justificação** em blocos de texto (priorizar alinhamento à esquerda com *rags* balanceados).
- Sem distorção geométrica de fontes.
- Contraste deliberado entre grotescas (dados) e serifadas (títulos).

**Acessibilidade no contexto brutalista:**

- Paleta restrita, mas com contraste ≥4.5:1 (ou 7:1 para texto principal).
- Marcação semântica profunda e ordem lógica no DOM para facilitar leitores de tela.

---

### Parte 3 – Manifesto UX: Re‑arquitetura de Interfaces Táticas e Cinéticas

10 regras arquitetônicas imutáveis para experiências de alta performance:

| Regra | Princípio | Impacto |
|-------|-----------|---------|
| 1. Supremacia do Teclado | Memória cinestésica | Command Palettes, navegação primária por teclado |
| 2. Gestão de Foco Determinística | Acessibilidade | *Focus traps*, ARIA complexo |
| 3. Honestidade Sistêmica de Estado | Visibilidade do status (Nielsen) | Feedback exato, micro‑interações semânticas |
| 4. Densidade de Informação Calibrada | Revelação progressiva | Hierarquia de dados clusterizada |
| 5. Supressão da Carga de Memória | Reconhecimento > recordação | Contexto onipresente |
| 6. Estética Funcional Mínima | “Menos, porém melhor” (Dieter Rams) | Pixels apenas para informação |
| 7. Prevenção por Design à Prova de Erros | Restrições sistêmicas | Layouts ocultam caminhos impossíveis |
| 8. Ortogonalidade e Consistência | Familiaridade (Nielsen/Shneiderman) | Comportamentos idênticos em toda a árvore |
| 9. Cinética Físico‑Matemática | Movimento natural | Animações com equações de mola (*springs*) |
| 10. Performance Visual Absoluta | Zero *layout thrashing* | Operações na GPU (transform/opacity) |

---

### Parte 4 – Arquitetura de Componentes: React Limpo e Escalabilidade Agnóstica

#### Composição sobre Herança

- Priorizar **composição** (objeto A **tem** um objeto B) em vez de herança (objeto A **é um** tipo de B).
- Uso de **Hooks customizados** para isolar lógica complexa.

#### Padrão Headless UI

- Componente que gerencia estado, acessibilidade e eventos, mas **não fornece markup**.
- Exemplo: um dropdown headless expõe `isOpen`, `getToggleButtonProps`, etc., permitindo que a camada de apresentação (Neo‑Brutalista) seja aplicada livremente.
- Separação radical entre comportamento e estética; resiliente a mudanças de identidade visual.

#### Estrutura de Diretórios Co‑localizada

```
src/components/DataGrid/
├── DataGrid.tsx          # componente principal
├── GridRow.tsx           # subcomponente privado
├── GridCell.tsx
├── DataGrid.helpers.ts   # lógica pesada
├── DataGrid.types.ts     # contratos TypeScript
└── index.ts              # barrel file (exporta apenas APIs públicas)
```

- Lógicas globais puras vão em `src/hooks/` e `src/utils.ts`.

---

### Parte 5 – Design System as Code: Engenharia de CSS e Taxonomia de Tokens

Repúdio ao Tailwind em prol de **CSS Custom Properties** (variáveis vivas no DOM) e **Design Tokens** estratificados:

| Camada | Função | Exemplo |
|--------|--------|---------|
| **Primitivos** | Valores absolutos (hex, rem) | `--color-zinc-900: #18181b` |
| **Semânticos** | Intenção contextual | `--surface-primary: var(--color-zinc-900)` |
| **Componentes** | Micro‑ajustes por estado | `--button-solid-hover-bg: var(--color-brand-500)` |

**Cascade Layers** para controle de especificidade:

```css
@layer reset, tokens, base, components, utilities;
```

Isso permite temas globais alterando apenas os tokens sem refatorar componentes.

---

### Parte 6 – Vanguarda Tecnológica: React Compiler e Paradigma Signals (2026)

#### React Compiler (AOT)

- Memoização automática em tempo de compilação; elimina necessidade de `useMemo`/`useCallback` manuais.
- Redireciona o foco do desenvolvedor para a lógica de negócio.

#### Signals para dados de altíssima frequência

Enquanto o React Compiler otimiza a maior parte da árvore, **Signals** (como os do Preact ou bibliotecas específicas) permitem atualizações cirúrgicas no DOM sem passar pelo Virtual DOM.

| Aspecto | React (memoizado) | Signals |
|---------|-------------------|---------|
| Disparo | Reexecuta componente | Atualiza nó DOM diretamente |
| Diffing | Virtual DOM | Nenhum |
| Fluxo | Prop drilling ou Context | Instâncias globais independentes |

Use Signals para painéis com WebSockets de alta frequência (ex.: transações financeiras).

---

### Parte 7 – Construção da Tela Central “AI‑Look”: O Teste de Estresse

#### Bento Grid

- Inspirado nas lancheiras japonesas, organiza informações díspares em módulos autossuficientes.
- Bordas rígidas (2‑4px), sem sombras, canvas dessaturado.
- Reflow matemático (sem media queries arbitrárias).

#### Animações com Framer Motion

- Uso de **spring physics** (`stiffness`, `damping`) para movimento natural.
- `<AnimatePresence>` para gerenciar entrada/saída.
- **Deferred Keyframe Resolution** para evitar engasgos.

#### Renderização de Alta Densidade

- **Para visualizações estáticas:** SVG com D3.js ou Nivo Charts.
- **Para milhões de pontos em tempo real:** WebGL (LightningChart, ECharts com Canvas) – o componente React age apenas como contêiner, delegando renderização para a GPU via shaders.

---

### Parte 8 – Conclusões Sistêmicas e Integração Arquitetônica Global

A arquitetura proposta transcende a mera identidade gráfica: é um tratado de engenharia visual paramétrica. Ao rejeitar bibliotecas monolíticas e adotar **Headless UI**, **Design Tokens** e **Cascade Layers**, garante‑se previsibilidade e imunidade a mudanças de marca. O **Manifesto UX** orienta interações tácteis e eficientes, enquanto o **React Compiler** e **Signals** viabilizam performance mesmo sob cargas extremas. O resultado é uma interface honesta, austera e inflexível, que coloca a função acima da decoração e entrega a mais alta fidelidade à intenção do projeto.

---

## Fonte

- **PDF Original:** Arquitetura React Autoral e UX Experimental.pdf
- **Skill gerada automaticamente** com preservação máxima do conteúdo essencial.