# Claude Code – Mergulho Profundo

## O Guia Completo para Entender Como Funciona
**Por Mark Kashef – Janeiro de 2026**

---

## Sumário
1. Introdução: Por que este guia existe  
2. Visão geral: Arquitetura do Claude Code  
3. O ciclo Coletar → Agir → Verificar  
4. Entendendo o sistema de ferramentas  
5. Operações com arquivos: Read, Write, Edit  
6. Ferramentas de busca: Glob e Grep  
7. Bash: poder de execução de comandos  
8. Gerenciamento de contexto: a analogia do balde  
9. Gerenciamento de sessões  
10. Customização: Claude.md, Skills e MCP  
11. Dicas de especialista e boas práticas  
12. Guia rápido de referência  

---

## 1. Introdução: Por que este guia existe
Este guia é o resultado de horas de investigação profunda sobre como o Claude Code realmente funciona por baixo dos panos.  
O objetivo é simples: ajudar você a entender o Claude Code melhor do que 99% dos usuários.

Ao entender a “máquina por trás da cortina”, você passa a:
- Trabalhar com mais eficiência  
- Resolver problemas mais rápido  
- Otimizar seu fluxo de trabalho  
- Preservar a janela de contexto  
- Customizar o Claude Code para suas necessidades  

### O segredo: entreviste o próprio Claude Code
O Claude Code possui um subagente interno chamado **Claude Code Guide**, criado especificamente para explicar como funcionam o CLI, o Agent SDK e a API.

**Dica profissional:** use `@claude-code-guide` sempre que tiver dúvidas profundas.

---

## 2. Visão geral: Arquitetura do Claude Code
O Claude Code é composto por quatro grandes componentes:

- **Interface de Terminal** – onde você digita os comandos  
- **Gerenciador de Sessões** – controla o ciclo de vida das conversas  
- **Executor de Ferramentas** – executa leituras, buscas e comandos  
- **Camada de Permissões** – garante segurança antes de ações críticas  

> O verdadeiro diferencial não é a infraestrutura, mas a inteligência que orquestra tudo.

---

## 3. O ciclo Coletar → Agir → Verificar
Este é o modelo mental central do Claude Code.

### Coletar (Gather)
- Lê arquivos  
- Explora estrutura de código  
- Faz buscas  
- Lê o arquivo Claude.md  

### Agir (Act)
- Edita arquivos  
- Cria novos arquivos  
- Executa comandos Bash  

### Verificar (Verify)
- Executa testes  
- Revisa alterações  
- Corrige erros automaticamente  

---

## 4. Entendendo o sistema de ferramentas
O Claude Code escolhe ferramentas com base na intenção:

| Necessidade | Ferramenta |
|------------|-----------|
| Ler arquivos | Read |
| Criar arquivos | Write |
| Editar arquivos | Edit |
| Buscar arquivos | Glob |
| Buscar conteúdo | Grep |
| Executar comandos | Bash |

Cada execução gera **novo contexto**.

---

## 5. Operações com arquivos
### Read
Usado para visualizar arquivos.  
⚠️ PDFs consomem muito contexto.

### Write
Cria arquivos novos:
- Documentação  
- Playbooks  
- Código  

### Edit
Edita apenas trechos específicos, economizando tokens.

---

## 6. Ferramentas de busca: Glob e Grep
- **Glob**: encontra arquivos por padrão de nome  
- **Grep**: busca texto dentro dos arquivos  

Fluxo eficiente:
```
Glob → Grep → Read
```

---

## 7. Bash: poder total
Permite:
- Instalar dependências  
- Rodar testes  
- Compilar projetos  
- Executar Git  

⚠️ Use com cuidado.

---

## 8. Gerenciamento de contexto: a analogia do balde
O contexto é um balde com tamanho fixo (~200k tokens).  
Quando passa de **40–50%**, a qualidade começa a cair.

Dica:
```
/context
```
para verificar uso.

---

## 9. Gerenciamento de sessões
- Cada terminal = nova sessão  
- Sessões são *stateless*  
- Persistem apenas arquivos, Claude.md e commits  

Use múltiplos terminais para isolar contextos.

---

## 10. Customização: Claude.md, Skills e MCP
- **Claude.md**: memória persistente  
- **Skills**: fluxos sob demanda  
- **MCP**: integrações externas (use com moderação)  

---

## 11. Dicas de especialista
- Use Plan Mode  
- Resuma antes de compactar  
- Use subagentes  
- Grave aprendizados no Claude.md  
- Suba permissões gradualmente  

---

## 12. Guia rápido
### Comandos essenciais
- `/context`
- `/compact`
- `/install GitHub`
- `@claude-code-guide`

### Regra de ouro
> Coletar → Agir → Verificar

---

**Agora vá construir algo incrível 🚀**
