# Plano de Implementação: 3 Novas Trilhas Claude Code

## Visão Geral

Criação de 3 novas trilhas baseadas em conteúdo existente:
- **Trilha 4**: MiniCurso18 (18 capítulos consolidados)
- **Trilha 5**: 95CC - Automação (WAT framework + deploy)
- **Trilha 6**: BeginCC - Guia do Iniciante (não-técnicos)

**Total de arquivos**: 27 novos HTML + edição do index.html principal

---

## Trilha 4: MiniCurso18 🟠 (Amber)

**Fonte:** `doc/minicurso18capitulos/` (18 capítulos consolidados em 8 módulos)
**Foco:** Curso completo e abrangente, do básico ao avançado
**Cor:** `text-amber-400`, `bg-amber-500/20`, `border-amber-500/30`

### Módulos

| Módulo | Capítulos Base | Título | 6 Tópicos |
|--------|---------------|--------|-----------|
| 4.1 | Cap 1-2 | Introdução ao Claude Code | Público-alvo, O que é, Paradigma shift, Diferenças de outras ferramentas, Conceito de vibe coding, Posicionamento no mercado |
| 4.2 | Cap 3-4 | Diferencial e Instalação | Subagentes paralelos, Context window 1M, Comparação Cursor/Windsurf, Pré-requisitos, Node.js, Conta Anthropic |
| 4.3 | Cap 5-6 | Primeiro Contato e Projeto | Terminal vs Warp vs Claudia, Comandos básicos, Modo dangerously, Estrutura HTML/CSS/JS, Feedback em tempo real, Iterações |
| 4.4 | Cap 7-8 | PRDs e Agentes | Modo Planning, PRDs automáticos, Claude como PM, Criação de agentes, subagents.cc, Orquestração paralela |
| 4.5 | Cap 9-10 | MCP e Comandos | Conceito MCP, Playwright/Exa/Firecrawl, Slash commands, Modos think, Customização, /security review |
| 4.6 | Cap 11-14 | Organização e Custos | Sessões modulares, claude.md, Redução de alucinações, Tokens Sonnet vs Opus, Relatórios de uso, Otimização |
| 4.7 | Cap 15-16 | Hooks e Segurança | Output style, Notificações, PreToolUse/PostToolUse, settings.json, Auditoria de vulnerabilidades, Limites |
| 4.8 | Cap 17-18 | Casos Avançados e Futuro | Sistema financeiro, Automação jurídica, E-learning adaptativo, Supply chain, Diagnóstico médico, Tendências futuras |

---

## Trilha 5: 95CC - Automação 🩵 (Teal)

**Fonte:** `doc/95cc/` (vídeo 36 min + WAT framework)
**Foco:** Construir automações práticas e deploy em produção
**Cor:** `text-teal-400`, `bg-teal-500/20`, `border-teal-500/30`

### Módulos

| Módulo | Título | 6 Tópicos |
|--------|--------|-----------|
| 5.1 | Interface e Ambiente | VS Code + extensão Claude Code, Estrutura de projetos, Explorer, Bypass permissions, Plan mode, Agente vs arquivos |
| 5.2 | Framework WAT | Workflows (instruções MD), Agents (decisão), Tools (execução .py), Self-improvement loop, Estrutura de pastas, Sistema .env |
| 5.3 | Planejamento com IA | claude.md como system prompt, Plan mode detalhado, Perguntas do agente, Auto-accept changes, To-do list visual, Iteração de planos |
| 5.4 | Construindo Tools | Python scripts executáveis, API integrations, Data transformations, Dependências e instalação, Erro e correção, Tool validation |
| 5.5 | MCP Servers Avançados | Exa para pesquisa web, Playwright (Microsoft), Instalação via CLI, Testes de conexão, Combinando MCPs, Segurança de MCPs |
| 5.6 | Skills Personalizados | Diferença Skills vs MCP, Skills globais vs projeto, Canvas design skill, Instalação de skills, Criando skills próprios, cloudcode-templates |
| 5.7 | Deploy no Modal | Modal.com infraestrutura, Cron triggers, Webhook triggers, Secrets management, Security review, Logs e monitoramento |
| 5.8 | Workflow Completo | YouTube Analytics exemplo, Scraping + análise + slides, PDF geração, Email sending, Google Sheets export, Produção automatizada |

---

## Trilha 6: BeginCC - Guia do Iniciante 🌹 (Rose)

**Fonte:** `doc/begincc/` (guia completo para iniciantes)
**Foco:** Pessoas não-técnicas, conceitos acessíveis
**Cor:** `text-rose-400`, `bg-rose-500/20`, `border-rose-500/30`

### Módulos

| Módulo | Título | 6 Tópicos |
|--------|--------|-----------|
| 6.1 | Por que Claude Code? | Hype explicado, Superhumano com IA, Paradigma shift, Cursor vs Claude Code, Não precisa saber programar, Investimento vs Resultado |
| 6.2 | Subagentes e Poder | Conceito de subagentes, Paralelo vs sequencial, Context window 1 milhão, Ramming de codebase, Shelf life de conversas, Fresh slate |
| 6.3 | Instalação Passo a Passo | Node.js download, npm install claude, Warp como alternativa, Primeiro comando "claude", Planos Anthropic ($20 vs $100-200), Login e autenticação |
| 6.4 | Cursor + Claude Code | VS Code/Cursor integração, Extensão Claude Code, Terminal dentro do editor, Dois AIs lado a lado, Run Cloud Code button, Múltiplas sessões |
| 6.5 | Seu Primeiro Site | claude dangerously skip, Prompt para website, Auto-building de arquivos, @ para targets específicos, Ask mode (shift+tab), Planning mode com Opus |
| 6.6 | MCPs Explicados | MCP como portas/senhas, Servidor único = múltiplas ações, Playwright para browser, Exa para pesquisa, Cipher para memória, Importar do Claude Desktop |
| 6.7 | Agentes Especializados | /agents comando, Gerar vs configurar manual, subagents.cc repositório, Designer, QA, PM agentes, Orquestração multi-agente, Cores de identificação |
| 6.8 | Dominando o Workflow | Slash commands (/clear, /compact, /resume), Output style, Security review, Think modes, Hooks para sons, settings.json, Claudia wrapper, Modular building |

---

## Estrutura de Arquivos

```
curso/
├── trilha4/
│   ├── index.html          # Landing da Trilha 4 (MiniCurso18)
│   ├── modulo-4-1.html
│   ├── modulo-4-2.html
│   ├── modulo-4-3.html
│   ├── modulo-4-4.html
│   ├── modulo-4-5.html
│   ├── modulo-4-6.html
│   ├── modulo-4-7.html
│   └── modulo-4-8.html
├── trilha5/
│   ├── index.html          # Landing da Trilha 5 (95CC Automação)
│   ├── modulo-5-1.html
│   ├── modulo-5-2.html
│   ├── modulo-5-3.html
│   ├── modulo-5-4.html
│   ├── modulo-5-5.html
│   ├── modulo-5-6.html
│   ├── modulo-5-7.html
│   └── modulo-5-8.html
├── trilha6/
│   ├── index.html          # Landing da Trilha 6 (BeginCC)
│   ├── modulo-6-1.html
│   ├── modulo-6-2.html
│   ├── modulo-6-3.html
│   ├── modulo-6-4.html
│   ├── modulo-6-5.html
│   ├── modulo-6-6.html
│   ├── modulo-6-7.html
│   └── modulo-6-8.html
└── index.html (principal - atualizar com 3 novos cards)
```

---

## Padrões Técnicos

### Cores por Trilha

| Trilha | Cor | Text Class | Background Class | Border Class |
|--------|-----|------------|------------------|--------------|
| T4 MiniCurso18 | Amber | `text-amber-400` | `bg-amber-500/20` | `border-amber-500/30` |
| T5 95CC | Teal | `text-teal-400` | `bg-teal-500/20` | `border-teal-500/30` |
| T6 BeginCC | Rose | `text-rose-400` | `bg-rose-500/20` | `border-rose-500/30` |

### Checklist de Página (ref/CHECKLIST_REVISAO.md)

- [ ] INEMA.CLUB link com `text-sky-400` ao lado do logo
- [ ] Light mode CSS override block em `<style>`
- [ ] Theme toggle funcionando
- [ ] Botões alinhados à esquerda (`justify-start`)
- [ ] Números de tópicos em badges circulares (`w-6 h-6 rounded-full`)
- [ ] 3 seções por tópico: "O que é", "Por que aprender", "Conceitos-chave"
- [ ] JavaScript para toggleTopic, theme toggle, modais

### Template Base

Usar `ref/MASTER_COMPLETO.md` como referência para componentes HTML/CSS/JS.

---

## Fontes de Conteúdo

| Trilha | Pasta | Arquivos Principais |
|--------|-------|---------------------|
| T4 | `doc/minicurso18capitulos/` | 18 arquivos .md (Capítulo 1-18) |
| T5 | `doc/95cc/` | 95CC.txt, CLAUDE (2) (1).md |
| T6 | `doc/begincc/` | (369) The Complete Beginner's Guide.txt |

---

## Estratégia de Implementação

1. **Criar diretórios**: trilha4/, trilha5/, trilha6/
2. **Criar index.html** de cada trilha (3 arquivos)
3. **Criar módulos em paralelo** usando 3 agentes
4. **Atualizar index.html principal** com novos cards
5. **QA final** para validar links, navegação, conteúdo

**Estimativa**: 27 arquivos HTML novos + 1 edição
