# Análise Profunda de Site para IA – Skill para LLM

## Identificação

- **Nome:** `analise-site-ia`
- **Descrição:** Framework completo de análise profunda de websites usando IA. Cobre auditoria SEO, performance, acessibilidade, segurança, arquitetura da informação, UX e otimização de conversão.

> **Nota:** O conteúdo desta skill, embora intitulado para análise de sites, concentra-se em **princípios fundamentais de engenharia de software com IA**, extraídos da filosofia “AkitaOnRails”. As técnicas e frameworks aqui descritos são aplicáveis a qualquer domínio de desenvolvimento assistido por IA, incluindo a construção e auditoria de websites.

---

## Instruções de Uso (para o LLM)

Esta skill deve ser ativada sempre que o usuário fizer perguntas ou solicitar ajuda sobre:

- Engenharia de prompt para código com IA
- Governança de agentes autônomos (Claude Code, Aider, etc.)
- Mitigação de alucinações e overengineering em código gerado por IA
- Aplicação de princípios “Akita” (simplicidade, isolamento, testes paranoicos)
- Estratégias de refatoração, testes de integração e validação em ambientes com IA
- Uso de ferramentas locais (Ollama, Qwen) e system prompts anti-preguiça
- Modelos mentais para orquestração de LLMs (separação de papéis, micro-prompts)

### Como usar este conhecimento

1. **Diagnóstico do problema**  
   - Identifique se a questão envolve geração de código, refatoração, depuração ou planejamento arquitetural com IA.
   - Classifique o nível de autonomia necessário (LLM simples, agente com ferramentas, ReAct, multiagente).

2. **Aplicação dos princípios fundamentais**  
   - **Economia de contexto:** limite o prompt às linhas exatas e informações essenciais; evite “flood and hope”.
   - **Separação de papéis:** use modelos pesados para arquitetura (cloud) e modelos leves locais para edição cirúrgica.
   - **Anti-preguiça:** system prompts devem exigir código completo (blocos SEARCH/REPLACE), sem comentários omissos.
   - **Isolamento paranoico:** diretórios de teste únicos e efêmeros (SecureRandom); sandboxing com agentfs/Docker.
   - **Refutação de overengineering:** proíba adição de dependências desnecessárias; siga a regra da simplicidade brutal.

3. **Estratégias de interação**  
   - Use **micro-prompts** para edições pontuais (especificando arquivo e linhas).
   - Use **prompts de arquiteto** para design baseado em restrições (pseudocódigo, máquinas de estado).
   - Desative “Deep Thinking” (reasoning_effort="NONE") em tarefas determinísticas.

4. **Validação e controle**  
   - Sempre que possível, exija que o agente gere um plano ou reflita antes de agir.
   - Utilize **testes de 7 camadas** com isolamento de estado e DevCache para lidar com não‑idempotência.
   - Em caso de falha recursiva, execute `git checkout` e reinicie o contexto (histórico limpo).

5. **Escolha do modelo**  
   - Consulte a tabela de categorização (Etapa 1) para entender os limites de cada abordagem.
   - Prefira modelos locais (Qwen, Ollama) para tarefas repetitivas e baixa latência.

### Formato de resposta preferido

- Sempre que possível, entregue **código funcional completo**, **diffs estruturados** ou **planos arquiteturais** em pseudocódigo.
- Inclua justificativas baseadas nos princípios (ex.: “evitei abstração prematura seguindo a regra da simplicidade”).
- Se a solução exigir mudanças profundas ou riscos, peça confirmação humana.

---

## Visão Geral

Este documento consolida um mapeamento exaustivo de publicações da escola “AkitaOnRails”, decodificando a postura técnica, o ceticismo fundamentado e as práticas operacionais de um engenheiro sênior no contexto de desenvolvimento com IA. O objetivo é formular um modelo mental acionável – o **Akita‑Driven AI Coding Framework** – um sistema rigoroso para mitigar entropia arquitetural, domar alucinações de agentes autônomos e aplicar Extreme Programming (XP) em um ecossistema dominado pela não‑determinística da IA.

---

## Quando Usar Esta Skill

Acione esta skill quando o usuário mencionar ou perguntar sobre:

- Engenharia de prompt para IA, system prompts, anti‑laziness
- Agentes autônomos de codificação (Claude Code, Aider, Cline)
- Vibe coding, overengineering, abstrações prematuras
- Testes de integração em monorepo, isolamento de estado, DevCache
- Limitações de LLMs (janela de contexto, sliding window attention, alucinação)
- Ferramentas locais: Ollama, Qwen, modelos quantizados
- Princípios Akita: simplicidade, fundamentos de computação, ceticismo
- Representações intermediárias (IR), especificação de domínio vs. sintaxe

**Palavras‑chave:** Akita, AI agents, prompt engineering, vibe coding, overengineering, system prompt, Aider, Ollama, Qwen, sliding window attention, alucinação, testes de integração, monorepo, DevCache, non‑idempotence, sandboxing, AgentFS, XP, IR.

---

## Conteúdo Completo

### Etapa 1 — Mapeamento Estratégico

O mapeamento inicial consolida o corpo de conhecimento disponível, abrangendo desde fundamentos de hardware até táticas de guerrilha para testes de integração.

#### 1. Inventário de Artigos e Categorização Temática

| Categoria Analítica | Título da Publicação | Foco Central e Abordagem Técnica |
|---------------------|------------------------|-----------------------------------|
| IA & Fundamentos de Hardware | Akitando 142 – Entendendo COMO ChatGPT Funciona | Mecânica de Transformers, auto‑atenção, vetores/matrizes em GPUs, processos estocásticos (Cadeias de Markov), limites de VRAM. |
| Ceticismo & Economia de Tokens | RANT – LLMs são LOOT BOXES! | Análise do modelo de incentivo predatório: ferramentas de “Deep Thinking” e RAGs excessivos como loot boxes. |
| Limites Arquiteturais & Testes | RANT – LLMs vão evoluir pra sempre? Desmistificando LLMs na Programação | Falácia da janela de contexto infinita (Sliding Window Attention), limites cognitivos, falhas recursivas em testes unitários. |
| Automação & Prompting Sênior | Seu próprio Co-pilot gratuito universal local (Aider, Ollama, Qwen) | Orquestração de agentes locais via CLI (Aider), injeção de System Prompts coercitivos contra preguiça da IA. |
| Engenharia de Plataforma & Workflow | Vibe Code: Do Zero à Produção em 6 DIAS (The M.Akita Chronicles) | Execução prática de arquitetura minimalista (Rails 8, SQLite, Kamal 2) supervisionando agentes (Claude Code). |
| Extreme Programming & Integração | Testes de Integração em MonoRepo (The M.Akita Chronicles) | Engenharia de resiliência através de isolamento paranoico, DevCache para IAs não‑idempotentes, validação com dados reais via Rsync. |
| Segurança & Contenção de Agentes | AI Agents: Garantindo a Proteção do seu Sistema | Estratégias de blindagem com AgentFS, containers Docker, limitação rigorosa de I/O. |
| Teoria da Linguagem & Representação | AI Agents: Qual seria a melhor Linguagem de Programação para LLMs? | Especificação de intenções via representações intermediárias (IR), separando intenção de negócio da escolha sintática. |

#### 2. Padrões de Pensamento Recorrentes

- **Supremacia dos fundamentos:** Conhecimento em cálculo, estatística, hardware (VRAM) é essencial para não ser refém da ferramenta.
- **Ceticismo em relação a promessas de escalabilidade:** Janelas de contexto “infinitas” são ilusórias devido à mecânica de atenção deslizante.
- **Isolamento paranoico e desconfiança sistemática:** Testes em diretórios efêmeros e únicos; ambiente host protegido por sandboxing.

---

### Etapa 2 — Extração de Princípios

Cada documento vital foi analisado sob uma matriz estruturada para converter reflexões em diretrizes tangíveis.

#### Artigo: RANT – LLMs são LOOT BOXES!

- **Tese:** O modelo de precificação baseado em tokens cria incentivo para gerar complexidade e loops recursivos.
- **Princípios extraídos:**  
  - Esforço de raciocínio não tem correlação linear com precisão em tarefas determinísticas.  
  - Precisão é inversamente proporcional ao ruído no prompt.
- **Aplicação em Prompt Engineering:**  
  - Use `reasoning_effort="NONE"` para correções locais.  
  - Prompt cirúrgico: apenas assinatura da função e erro exato.  
  - Instrua a IA a emitir apenas o bloco de substituição, sem explicações.
- **Anti‑padrão:** Stacktrace Dumping – colar milhares de linhas de log satura a atenção e força alucinações.

#### Artigo: RANT – LLMs vão evoluir pra sempre? Desmistificando LLMs na Programação

- **Tese:** Benchmarks sintéticos não representam desempenho em bases legadas; a atenção deslizante limita o foco real.
- **Princípios extraídos:**  
  - Avalie IA empiricamente dentro das restrições do projeto.  
  - Desacoplamento não é só boa prática, é exigência mecânica para evitar amnésia contextual.
- **Aplicação em Prompt Engineering:**  
  - Para refatorar módulos grandes, aponte linhas específicas (ex.: “linhas 150 a 200”).  
  - Instrua: “Considere interfaces anexadas como contratos imutáveis; não altere dependências externas.”
- **Anti‑padrão:** Confiança Cega em Benchmarks – delegar criação de testes à IA em uma iteração gera falsos positivos.

#### Artigo: Seu próprio Co-pilot gratuito universal local (Aider, Ollama, Qwen)

- **Tese:** Ferramentas locais dão controle sobre system prompts e parâmetros, expondo o “segredo da mágica”.
- **Princípios extraídos:**  
  - IAs são preguiçosas por padrão; precisam de instruções explícitas contra omissões.  
  - Controle paramétrico (limite de histórico) evita degradação em sessões longas.
- **Aplicação em Prompt Engineering:**  
  - System prompt anti‑preguiça: “Proibido usar comentários para omitir código; todo bloco SEARCH/REPLACE deve ser completo.”
- **Anti‑padrão:** Lazy Output Acceptance – aceitar outputs parciais e tentar completar manualmente.

#### Artigo: Testes de Integração em MonoRepo | Bastidores do The M.Akita Chronicles

- **Tese:** Em mono-repos, a não‑idempotência das LLMs exige defesa em profundidade (7 camadas).
- **Princípios extraídos:**  
  - Estado compartilhado é intolerável; cada teste deve rodar em diretório efêmero único.  
  - DevCache estabiliza respostas variáveis.
- **Aplicação em Prompt Engineering:**  
  - “Todo teste de I/O deve criar diretório com SecureRandom.hex(8) e destruí‑lo no teardown.”
- **Anti‑padrão:** Diretórios fixos para artefatos de teste – causa poluição de estado.

#### Artigo: Vibe Code: Do Zero à Produção em 6 DIAS | The M.Akita Chronicles

- **Tese:** Com escolhas de infraestrutura brutalmente simples, um profissional pode construir e implantar um sistema complexo em 6 dias delegando sintaxe à IA.
- **Princípios extraídos:**  
  - Aumento de produtividade não justifica complexidade; overengineering é inimigo.  
  - IA opera melhor em ambientes padronizados e maduros.
- **Aplicação em Prompt Engineering:**  
  - Prompts restritivos: “Sistema baseado estritamente em Rails 8 + SQLite; nenhuma outra dependência sugerida.”
- **Anti‑padrão:** AI‑Driven Overengineering – deixar a IA ditar tecnologias (Kubernetes, Kafka) para projetos pequenos.

#### Artigo: AI Agents: Garantindo a Proteção do seu Sistema

- **Tese:** Agentes autônomos no terminal são ameaça crítica; devem ser confinados.
- **Princípios extraídos:**  
  - Princípio do menor privilégio: agente não deve ter acesso irrestrito a arquivos ou rede.
- **Aplicação em Prompt Engineering:**  
  - Prompts operacionais com amarras: “Aja dentro do sandbox; comandos restritos aos subdiretórios listados.”
- **Anti‑padrão:** Root Agent Execution – executar agente no diretório raiz com permissões globais.

#### Artigo: AI Agents: Qual seria a melhor Linguagem de Programação para LLMs?

- **Tese:** Comunicação ideal com LLMs é via representações intermediárias (IR) – especificações puras de restrições lógicas.
- **Princípios extraídos:**  
  - Separe intenção de negócio da escolha sintática.  
  - Modularização deve ser guiada por fronteiras de domínio, não por hierarquia de pastas.
- **Aplicação em Prompt Engineering:**  
  - Prompts arquiteturais: “Defina invariâncias da entidade Usuário; não adicione detalhes de persistência ou controllers.”
- **Anti‑padrão:** Syntax Dictation – ditar linha por linha, anulando a capacidade generativa.

---

### Etapa 3 — O Modelo Mental de Akita Aplicado à Inteligência Artificial

A decodificação das publicações revela um modelo denso, pragmático e implacável.

#### 1. Como Akita estruturaria prompts para codificação?

- Separação severa de papéis:  
  - Modelo pesado (cloud) como **Arquiteto** – recebe interfaces contratuais, gera pseudocódigo focado no domínio.  
  - Modelo leve local (Qwen via Ollama) como **Editor** – recebe micro‑prompts determinísticos, emite blocos SEARCH/REPLACE completos.
- Isolamento cirúrgico do contexto: apenas as linhas que precisam ser alteradas.
- System prompts repletos de proteções contra preguiça computacional.

#### 2. Que tipo de prompt ele criticaria severamente?

- Prompts de “inundação e esperança” (Flood and Hope):  
  - Exemplo: “Meu servidor parou. Aqui estão 12 mil linhas de log e 5 arquivos. Encontre o erro e sugira melhores práticas.”  
  - Isso viola os limites da atenção deslizante e delega decisões subjetivas a uma máquina estatística.

#### 3. Como lidaria com alucinação e amnésia de código?

- Não argumenta com a IA; aplica engenharia de processo draconiana:  
  - Controle de versão agressivo (`git checkout` antes de qualquer gravação).  
  - Ao detectar alucinação, desfaz a alteração, limpa o histórico da conversa, desativa “Deep Thinking”, e injeta novo micro‑prompt.
- Compilação local e revisão estrutural são os únicos árbitros.

#### 4. Como o Extreme Programming (XP) seria aplicado ao uso de agentes?

- Pair programming assimétrico: humano dita, IA executa, humano fiscaliza.
- TDD clássico é volátil com IA; adota‑se o **Paradigma de 7 Camadas de Teste**:  
  - Testes rodam em diretórios efêmeros (SecureRandom) e são descartados.  
  - DevCache estabiliza resultados não‑idempotentes.  
  - IA não escreve testes de infraestrutura; é validada por eles.

#### 5. Como combater o overengineering provocado por agentes autônomos?

- Imposição de simplicidade brutal por padrão:  
  - Pilha tecnológica mínima (ex.: Rails 8 + SQLite).  
  - Prompts proíbem adição de bibliotecas externas sem necessidade matemática estrita.  
  - Agentes com acesso de gravação são enjaulados (agentfs, Docker).

---

### Etapa 4 — Framework Final: Akita-Driven AI Coding Framework

#### 4.1. Pilares Inegociáveis (Princípios de Governança)

1. **Fundamento Precede a Abstração:** Domínio de probabilidade, álgebra linear e hardware é indispensável.
2. **Atenção Vectorial Estrita (Axioma da Janela Fina):** Assuma que toda IA sofre de miopia seletiva; limite o contexto às linhas precisas.
3. **Economia da Estocástica:** Force determinismo via parametrização rigorosa; desative “Deep Thinking” em tarefas fechadas.

#### 4.2. Regras Operacionais de Interação

| Código | Definição | Mecanismo de Execução e Defesa |
|--------|-----------|--------------------------------|
| OP-01 | Separação Assíncrona de Papéis | Nunca misture análise arquitetural e correção sintática. Use modelos cloud para arquitetura (`architect=true`) e modelos locais para edição (`editor=true`). |
| OP-02 | Proteção Sistêmica Anti-Preguiça | System prompts devem proibir sumarização: “Todo bloco SEARCH/REPLACE deve ser emitido de forma completa.” |
| OP-03 | Blindagem de Sandboxing Ativo | Agentes executam em agentfs ou containers Docker efêmeros, com acesso restrito a disco e rede. |
| OP-04 | Supressão de Ruído Computacional | Em refatorações fechadas, use `reasoning_effort="NONE"` e limite histórico (ex.: `max-chat-history-tokens:8192`). |

#### 4.3. O Workflow Ideal: O Ciclo “Zero to Prod” (Arquitetura Vibe Code)

1. **Fundação e Contenção:** Decrete pilha estável (Rails 8, SQLite) e estabeleça sandbox (AgentFS).
2. **Delegação por IR:** Arquiteto emite restrições lógicas, assinaturas de controllers, migrações – sem poluição sintática.
3. **Iteração Cirúrgica em Terminal:** Micro‑prompts com system prompt anti‑preguiça; uso de SEARCH/REPLACE.
4. **Integração e Validação Paranoica:** Disparo de 7 camadas de testes com diretórios efêmeros e DevCache.
5. **Aprovação Estrita e Infraestrutura:** Discussão de topologia, deploy com tecnologia não‑inchada (Docker, Kamal). Qualquer sugestão complexa é vetada.

#### 4.4. Estrutura de Micro‑Prompts de Alto Rendimento

**Micro‑Prompt “Editor” (foco local, velocidade):**  
```
Mantenha foco estrito no arquivo lib/parsers/document_processor.rb, linhas 40 a 90. 
O método de parsing XML atual consome excesso de RAM. 
Refatore usando iteradores stream da biblioteca Nokogiri::XML::Reader. 
É proibido adicionar qualquer outra gem. 
A assinatura do método não pode mudar. 
Formato: apenas SEARCH/REPLACE, sem justificativas.
```

**Micro‑Prompt “Arquiteto” (design baseado em restrições):**  
```
Refatore sistema síncrono para background jobs. 
Modele o contrato conceitual da máquina de estado assíncrona, com retentativas exponenciais. 
Seja indiferente ao framework de mensageria. 
Formato: pseudocódigo robusto e definição dos estados.
```

#### 4.5. Estratégia de Validação e Auditoria Reversa

- **Guilhotina de Loops Recursivos:** Após falha, faça `git checkout`, limpe histórico, e reescreva micro‑prompt com “Deep Thinking” desligado.
- **Inspeção Contínua:** Mantenha modo `--verbose` ligado para monitorar tokens e limites.
- **Teste Cruzado em Realidade (Camadas 4 e 5):** Use Rsync com dados reais de produção em ambiente isolado; mocks são banidos.

#### 4.6. Estratégia de Refatoração Contínua no Ecossistema IA

- **Poda Algorítmica e Coesão Anti‑Amnésia:** Fatia módulos longos em blocos de responsabilidade única (adaptado aos limites de atenção da LLM).
- **Erradicação de Boilerplate Abstrato:** Revise diretórios recém‑construídos e consolide lógica repetitiva em utilitários nativos, reduzindo massa estrutural.

---

## Fonte

- **PDF Original:** Análise Profunda de Site para IA.pdf (conteúdo derivado da filosofia AkitaOnRails)
- **Skill gerada automaticamente** com preservação máxima de conteúdo.