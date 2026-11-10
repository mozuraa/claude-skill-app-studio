# Ideias de apps e jogos · App & game ideas — Claude Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Claude Skill](https://img.shields.io/badge/Claude-Skill-D97757)

**[Português](#português) · [English](#english)**

---

## Português

Uma [skill](#o-que-é-uma-skill) para o **Claude** (Claude Code, app Claude e claude.ai).

### O que faz

Gera **2 a 3 ideias bem desenvolvidas** de apps ou jogos **novos** que uma pessoa sozinha consegue construir e publicar (iOS, Android, web ou desktop). Em vez de uma lista de títulos soltos, cada ideia vem pensada a fundo: público, ciclo principal, diferença face à concorrência, modelo de negócio, esforço, primeiros passos e riscos.

### Quando é ativada

O Claude usa-a sozinho quando pedes algo como:

- "Que jogo devia fazer a seguir?"
- "Dá-me uma ideia de app para crianças"
- "Quero um projeto que consiga acabar num fim de semana"
- "O que posso criar com SwiftUI?"

Também a podes chamar diretamente com `/ideias-apps`.

### O que recebes

Cada ideia vem sempre com:

- O que é
- Para quem
- Como funciona
- O que a torna diferente
- Como ganha dinheiro
- Esforço
- Primeiros passos
- Riscos

No fim, o Claude diz qual recomenda e porquê, e oferece-se para aprofundar.

Vê um exemplo completo em [`examples/exemplo.md`](examples/exemplo.md).

### Detalhes

- Usa o contexto que o Claude já tem (projetos anteriores, tecnologias que usas) para propor ideias que encaixam no que sabes fazer.
- Nunca propõe copiar uma app ou jogo existente — pode inspirar-se num género ou mecânica e diz qual.
- Se o pedido for vago, não faz perguntas: gera ideias variadas e oferece-se para afinar.
- Responde na língua em que escreves — as instruções estão em português, mas funciona em qualquer língua.

### Instalação

**Claude Code (para todos os teus projetos)**

```bash
git clone https://github.com/mozuraa/claude-skill-ideias-apps.git ~/.claude/skills/ideias-apps
```

**Claude Code (só num projeto)** — dentro da pasta do projeto:

```bash
git clone https://github.com/mozuraa/claude-skill-ideias-apps.git .claude/skills/ideias-apps
```

Abre uma sessão nova para a skill ser carregada.

**App Claude / claude.ai**

1. Nesta página, carrega em **Code → Download ZIP**.
2. No Claude, abre as **Definições** e procura a secção **Skills** (em *Capacidades*).
3. Carrega o ZIP. A skill fica disponível nas tuas conversas.

> As skills personalizadas precisam de estar ativadas na tua conta/organização.

### Atualizar

```bash
cd ~/.claude/skills/ideias-apps && git pull
```

### O que é uma skill?

Uma skill é uma pasta com um ficheiro `SKILL.md`: um nome, uma descrição de quando deve ser usada e instruções. O Claude lê só a descrição até ela ser útil; quando o pedido encaixa, carrega as instruções e segue-as. Não instala programas nem corre código — é só texto.

### Estrutura

```
claude-skill-ideias-apps/
├── SKILL.md            # a skill (nome, descrição e instruções)
├── examples/
│   └── exemplo.md      # exemplo de pedido e resposta
├── README.md
├── CHANGELOG.md
└── LICENSE
```

### Família de skills de ideias

| Skill | Para quê |
|---|---|
| [`ideias-apps`](https://github.com/mozuraa/claude-skill-ideias-apps) *(esta)* | Ideias de apps e jogos |
| [`ideias-funcionalidades`](https://github.com/mozuraa/claude-skill-ideias-funcionalidades) | Ideias de funcionalidades |
| [`ideias-monetizacao`](https://github.com/mozuraa/claude-skill-ideias-monetizacao) | Ideias de monetização |
| [`brainstorming`](https://github.com/mozuraa/claude-skill-brainstorming) | Brainstorming |

### Contribuir

Sugestões e melhorias são bem-vindas: abre uma *issue* ou um *pull request*. Se a skill não se ativou quando devia (ou ativou quando não devia), diz qual foi o pedido — ajuda a afinar a descrição.

### Licença

[MIT](LICENSE) — podes usar, alterar e partilhar livremente, mantendo o aviso de licença.

---

## English

A [skill](#what-is-a-skill) for **Claude** (Claude Code, the Claude app and claude.ai).

### What it does

Generates **2–3 well-developed ideas** for **new** apps or games that a solo developer can actually build and ship (iOS, Android, web or desktop). Instead of a list of loose titles, each idea is fully thought through: audience, core loop, what sets it apart, business model, effort, first steps and risks.

### When it triggers

Claude uses it on its own when you ask things like:

- "What game should I make next?"
- "Give me an app idea for kids"
- "I want a project I can finish in a weekend"
- "What could I build with Flutter?"

You can also call it directly with `/ideias-apps`.

### What you get

Every idea always includes:

- What it is
- Who it's for
- How it works
- What makes it different
- How it makes money
- Effort
- First steps
- Risks

At the end, Claude says which one it recommends and why, and offers to go deeper.

See a full example in [`examples/exemplo.md`](examples/exemplo.md) (in Portuguese).

### Details

- Uses the context Claude already has (past projects, your tech stack) to suggest ideas that fit what you can build.
- Never proposes copying an existing app or game — it may draw on a genre or mechanic and says which.
- If the request is vague it doesn't ask questions: it gives varied ideas and offers to refine.
- Replies in the language you write in — the instructions are in Portuguese, but it works in any language.

### Installation

**Claude Code (all your projects)**

```bash
git clone https://github.com/mozuraa/claude-skill-ideias-apps.git ~/.claude/skills/ideias-apps
```

**Claude Code (one project only)** — from the project folder:

```bash
git clone https://github.com/mozuraa/claude-skill-ideias-apps.git .claude/skills/ideias-apps
```

Start a new session so the skill is loaded.

**Claude app / claude.ai**

1. On this page, click **Code → Download ZIP**.
2. In Claude, open **Settings** and find the **Skills** section (under *Capabilities*).
3. Upload the ZIP. The skill becomes available in your chats.

> Custom skills must be enabled for your account/organization.

### Updating

```bash
cd ~/.claude/skills/ideias-apps && git pull
```

### What is a skill?

A skill is a folder with a `SKILL.md` file: a name, a description of when it should be used, and instructions. Claude only reads the description until it becomes relevant; when a request matches, it loads the instructions and follows them. It installs no programs and runs no code — it's just text.

### Idea skills family

| Skill | What for |
|---|---|
| [`ideias-apps`](https://github.com/mozuraa/claude-skill-ideias-apps) *(this one)* | App & game ideas |
| [`ideias-funcionalidades`](https://github.com/mozuraa/claude-skill-ideias-funcionalidades) | Feature ideas |
| [`ideias-monetizacao`](https://github.com/mozuraa/claude-skill-ideias-monetizacao) | Monetization ideas |
| [`brainstorming`](https://github.com/mozuraa/claude-skill-brainstorming) | Brainstorming |

### Contributing

Suggestions and improvements are welcome: open an issue or a pull request. If the skill didn't trigger when it should have (or did when it shouldn't), share the prompt — it helps tune the description.

### License

[MIT](LICENSE) — free to use, modify and share, keeping the license notice.
