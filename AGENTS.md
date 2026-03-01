# My Simple Skills — Agent Instructions

This repository contains 12 specialized skills extracted from comprehensive technical PDFs.
When any of the trigger keywords below match the user's context, read the corresponding `SKILL.md` file entirely before responding.

## Available Skills

| Skill | Directory | Triggers |
|-------|-----------|----------|
| IA como Arquiteto de Software Sênior | `skills/ia-arquiteto-software/` | software architect, DDD, hexagonal architecture, clean architecture, ATAM, ADR, trade-offs, system design |
| IA e Refatoração Cognitiva de Software | `skills/ia-refatoracao-cognitiva/` | refatoração, refactoring, legacy code, complexidade ciclomática, code smells |
| IA em Testes: Qualidade Real Avançada | `skills/ia-testes-qualidade/` | TDD, testing, mutation testing, cobertura de testes, property-based testing |
| IA na Engenharia de Requisitos | `skills/ia-engenharia-requisitos/` | requirements engineering, elicitação, user stories, requisitos não-funcionais, rastreabilidade |
| IA para Escrita Técnica Avançada | `skills/ia-escrita-tecnica/` | escrita técnica, technical writing, documentação, API docs, RFCs, post-mortems |
| Engenharia de Software Avançada | `skills/engenharia-software-avancada/` | SOLID, clean code, design patterns, arquitetura distribuída, DevOps, observabilidade |
| AI Coding Avançado | `skills/ai-coding-avancado/` | AI coding, vibe coding, prompt engineering, TDD agêntico, multiagentes, context window |
| XP com Agentes de IA | `skills/xp-agentes-ia/` | XP, extreme programming, pair programming, AI-XP, TDD mandatório, DevSecOps |
| Escrita Criativa com IA | `skills/escrita-criativa-ia/` | escrita criativa, creative writing, narrativas, worldbuilding, personagens, storytelling |
| Arquitetura React Autoral e UX Experimental | `skills/react-autoral-ux/` | React, UX experimental, design system, animações, micro-interações, frontend |
| Unconventional SaaS UI/UX Design System | `skills/saas-ui-ux-design/` | SaaS, UI/UX, design system, glassmorphism, dark mode, dashboards, design tokens |
| Análise Profunda de Site para IA | `skills/analise-site-ia/` | análise de site, SEO, performance, acessibilidade, segurança web, UX audit |

## Usage Rules

1. **Always read the full SKILL.md** before responding on a matched topic
2. **Preserve Portuguese terminology** — these skills are written in PT-BR with technical terms
3. **Follow the Iron Laws** from the XP/AI-XP framework when writing code:
   - TDD is mandatory (never modify production code without a failing test first)
   - Clean Architecture is non-negotiable (domain never imports infrastructure)
   - YAGNI + KISS (no premature abstractions)
4. **Anti-patterns to avoid**: vibe coding, comments everywhere, over-specification, bugs déjà-vu
