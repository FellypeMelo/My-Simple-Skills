# 🧠 My Simple Skills

> **Repositório portável de skills técnicas** extraídas de PDFs especializados para uso com agentes de IA (Claude, Gemini, Antigravity, etc.).

[![Skills](https://img.shields.io/badge/skills-12-blue)]()
[![Content](https://img.shields.io/badge/content-655KB-green)]()
[![Language](https://img.shields.io/badge/language-PT--BR-yellow)]()

---

## 📋 O que é isso?

Uma coleção de **12 skills técnicas especializadas** extraídas de PDFs abrangentes sobre engenharia de software, arquitetura, testes, design e escrita — tudo otimizado para ser consumido por agentes de IA.

Cada skill preserva o **máximo detalhe** do PDF original, incluindo conceitos, padrões, anti-padrões, checklists, referências e frameworks.

---

## 🗂️ Skills Disponíveis

### Engenharia de Software & Arquitetura

| Skill | Páginas | Descrição |
|-------|---------|-----------|
| [`ia-arquiteto-software`](skills/ia-arquiteto-software/SKILL.md) | 27p | IA como Arquiteto Sênior — DDD, Hexagonal, ATAM, ADRs, prompting arquitetural |
| [`ia-refatoracao-cognitiva`](skills/ia-refatoracao-cognitiva/SKILL.md) | 13p | Refatoração cognitiva com IA — legacy code, complexidade, anti-padrões |
| [`ia-testes-qualidade`](skills/ia-testes-qualidade/SKILL.md) | 14p | Testes avançados com IA — TDD, mutation testing, cobertura inteligente |
| [`ia-engenharia-requisitos`](skills/ia-engenharia-requisitos/SKILL.md) | 39p | Engenharia de requisitos com IA — elicitação semântica, rastreabilidade |
| [`engenharia-software-avancada`](skills/engenharia-software-avancada/SKILL.md) | 22p | Tratado de engenharia avançada — SOLID, Clean Code, padrões, DevOps |

### AI Coding & Metodologias

| Skill | Páginas | Descrição |
|-------|---------|-----------|
| [`ai-coding-avancado`](skills/ai-coding-avancado/SKILL.md) | 25p | AI Coding avançado — prompt engineering, TDD agêntico, anti-vibe coding |
| [`xp-agentes-ia`](skills/xp-agentes-ia/SKILL.md) | 24p | Framework AI-XP — pair programming com IA, orquestração multiagentes |

### Escrita & Documentação

| Skill | Páginas | Descrição |
|-------|---------|-----------|
| [`ia-escrita-tecnica`](skills/ia-escrita-tecnica/SKILL.md) | 11p | Escrita técnica avançada — APIs, RFCs, post-mortems, comunicação |
| [`escrita-criativa-ia`](skills/escrita-criativa-ia/SKILL.md) | 19p | Escrita criativa com IA — narrativas, worldbuilding, personagens |

### Design & Frontend

| Skill | Páginas | Descrição |
|-------|---------|-----------|
| [`react-autoral-ux`](skills/react-autoral-ux/SKILL.md) | 20p | React autoral + UX experimental — animações, design systems |
| [`saas-ui-ux-design`](skills/saas-ui-ux-design/SKILL.md) | 23p | Design System SaaS não-convencional — glassmorphism, dark mode |
| [`analise-site-ia`](skills/analise-site-ia/SKILL.md) | 16p | Análise profunda de sites com IA — SEO, performance, acessibilidade |

---

## 🚀 Como Usar

### Com Claude Code / Antigravity

As skills são automaticamente detectadas via `.claude/settings.json` e `AGENTS.md`. Basta clonar este repo na raiz do seu projeto ou referenciar como submódulo:

```bash
# Clonar diretamente
git clone https://github.com/FellypeMelo/My-Simple-Skills.git

# Ou como submódulo
git submodule add https://github.com/FellypeMelo/My-Simple-Skills.git .skills
```

### Com Gemini CLI

As skills são detectadas via `.gemini/settings.json`:

```bash
# O Gemini CLI detecta automaticamente o diretório skills/
gemini chat  # As skills são carregadas automaticamente
```

### Uso Manual

Cada skill é um arquivo Markdown standalone. Copie o `SKILL.md` desejado para o contexto do seu agente.

---

## 📐 Estrutura do Repositório

```
My-Simple-Skills/
├── .claude/
│   └── settings.json          # Config para Claude Code
├── .gemini/
│   └── settings.json          # Config para Gemini CLI
├── AGENTS.md                  # Índice de skills + regras de ativação
├── skills/
│   ├── ia-arquiteto-software/
│   │   └── SKILL.md
│   ├── ia-refatoracao-cognitiva/
│   │   └── SKILL.md
│   ├── ia-testes-qualidade/
│   │   └── SKILL.md
│   ├── ia-engenharia-requisitos/
│   │   └── SKILL.md
│   ├── ia-escrita-tecnica/
│   │   └── SKILL.md
│   ├── engenharia-software-avancada/
│   │   └── SKILL.md
│   ├── ai-coding-avancado/
│   │   └── SKILL.md
│   ├── xp-agentes-ia/
│   │   └── SKILL.md
│   ├── escrita-criativa-ia/
│   │   └── SKILL.md
│   ├── react-autoral-ux/
│   │   └── SKILL.md
│   ├── saas-ui-ux-design/
│   │   └── SKILL.md
│   └── analise-site-ia/
│       └── SKILL.md
├── README.md
└── LICENSE
```

---

## 🔒 Leis Invioláveis (das skills)

Estas leis são extraídas dos PDFs e devem ser seguidas ao usar as skills:

1. **TDD é Mandatório** — Nunca modifique código sem um teste falhando primeiro
2. **Clean Architecture** — Domínio nunca importa infraestrutura
3. **Economia de Contexto** — Limite o escopo às linhas exatas de alteração
4. **Anti-Preguiça** — Proibido sumarizar código com `// ... código anterior aqui`
5. **YAGNI + KISS** — Funções ≤15 linhas, Classes ≤200 linhas

---

## 📚 PDFs Fonte

| PDF | Páginas | Chars |
|-----|---------|-------|
| IA como Arquiteto de Software Sênior | 27 | 75K |
| IA e Refatoração Cognitiva de Software | 13 | 29K |
| IA em Testes: Qualidade Real Avançada | 14 | 30K |
| IA na Engenharia de Requisitos: Guia Detalhado | 39 | 112K |
| IA para Escrita Técnica Avançada | 11 | 25K |
| Tratado Técnico de Engenharia de Software Avançada | 22 | 47K |
| Tratado Técnico AI Coding Avançado | 25 | 59K |
| XP com Agentes de IA: Tratado Técnico | 24 | 53K |
| Manual de Escrita Criativa com IA | 19 | 39K |
| Arquitetura React Autoral e UX Experimental | 20 | 53K |
| Unconventional SaaS UI/UX Design System | 23 | 50K |
| Análise Profunda de Site para IA | 16 | 41K |
| **Total** | **253** | **~612K** |

---

## 🤝 Contribuindo

1. Adicione novos PDFs no formato correto
2. Execute o script de conversão
3. Valide a skill gerada
4. Abra um PR

---

## 📄 Licença

MIT — veja [LICENSE](LICENSE)
