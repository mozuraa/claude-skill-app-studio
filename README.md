<p align="center">
  <img src="icon.svg" width="160" alt="App studio — telemóvel com batimento cardíaco, uma lâmpada, um lápis e um estetoscópio">
</p>

<h1 align="center">App studio — Claude Skill</h1>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/Claude-Skill-D97757" alt="Claude Skill">
  <img src="https://img.shields.io/badge/modos-Idear%20·%20Criar%20·%20Diagnosticar-8A63D2" alt="Modos">
</p>

<p align="center">
📚 Faz parte da <b><a href="https://github.com/mozuraa/claude-skills">biblioteca de skills de mozuraa</a></b> · Part of <b><a href="https://github.com/mozuraa/claude-skills">mozuraa's skills library</a></b>
</p>

<p align="center"><b><a href="#português">Português</a> · <a href="#english">English</a></b></p>

---

## Português

Um **estúdio completo de aplicações** para o **Claude** (iOS, Android, Flutter, React Native/Expo, desktop), com três modos que se encadeiam:

| Modo | Para quê | Exemplo de pedido |
|---|---|---|
| 💡 **Idear** | Ideias detalhadas de **apps e jogos novos** que consegues construir e publicar sozinho | "Que jogo devia fazer a seguir?" |
| 🛠️ **Criar** | **Constrói uma app contigo de raiz**, da ideia ao MVP e à publicação na App Store e no Google Play | "Quero fazer uma app para registar as minhas plantas" |
| 🩺 **Diagnosticar** | **Examina e corrige** tudo o que afeta a app: 12 áreas, 140+ verificações, relatório de saúde com opinião e "pronta para a loja?" | "A minha app crasha" · "A Apple rejeitou" |

Em todos os modos o Claude **faz perguntas, mostra provas, dá a sua opinião honesta e só avança com a tua autorização**. A ideia escolhida no Idear é o briefing do Criar; o Criar termina com um exame do Diagnosticar antes de ir para a loja; um diagnóstico pode levar a ideias para a próxima versão.

### 💡 Idear

- Duas a três ideias **bem desenvolvidas**, cada uma com: o que é, para quem, o ciclo principal, o que a torna diferente, como ganha dinheiro, esforço, primeiros passos e riscos.
- Ideias originais: nunca clones de apps ou jogos existentes.
- Tem um [catálogo de inspiração](references/idear/inspiracao.md) com:
  - géneros e mecânicas de jogos;
  - utilidades;
  - funcionalidades do sistema que dão ideias (widgets, Live Activities, IA no dispositivo);
  - como validar uma ideia antes de a construir;
  - uma grelha para comparar ideias;
  - ideias a evitar.

### 🛠️ Criar

```
1. Briefing ─► 2. Plano (MVP) ─► ✋ ─► 3. Design ─► 4. Fluxo principal ─► ✋ ─► 5. Resto da app ─► 6. Verificação ─► ✋ ─► 7. Lojas e entrega
```

- **Briefing** com as perguntas para cada tipo de app: jogos, utilidades, hábitos, saúde, crianças, social, negócios, brincadeiras.
- **Plano do MVP**: a versão mais pequena que já entrega valor, com a tecnologia, os dados e os custos. ✋ Aprovas.
- **Design nativo**, segundo as regras da Apple e da Google.
- **Fluxo principal primeiro**, a correr no simulador, com capturas. ✋ Aprovas.
- **Resto da app**: dados que nunca se perdem nas atualizações, permissões no momento certo, acessibilidade, ícone, compras com restauro, Privacy Manifest.
- **Verificação** com o modo Diagnosticar. ✋ Aprovas.
- **Publicação**: TestFlight, página da loja, privacidade, revisão e um guia `COMO-ATUALIZAR.md`.
- **Guias:**
  - [`briefing`](references/criar/briefing.md);
  - [`stack`](references/criar/stack.md): SwiftUI, Compose, Flutter, Expo, SpriteKit/Godot, onde guardar os dados, contas, compras, anúncios, crashes e custos;
  - [`design`](references/criar/design.md): convenções das plataformas, sistema de design, ecrãs essenciais, ícone e jogos;
  - [`lancamento`](references/criar/lancamento.md): contas, assinatura, testes, página da loja, privacidade, revisão, rejeições e depois do lançamento.

### 🩺 Diagnosticar

**Consulta → exame com provas → relatório de saúde (🔴🟠🟡🟢) → a minha opinião → decides → tratamento verificado → alta.**

O exame cobre 12 áreas: estabilidade · funcionamento e idiomas · layout em todos os ecrãs · ícones e imagens · desempenho e bateria · segurança · privacidade (Privacy Manifest, etiquetas, Data safety, ATT) · acessibilidade · regras da App Store e do Google Play · rede e dados · compras · build e código.

Guias: [`checklist`](references/diagnostico/checklist.md) (140+ verificações) e [`como-verificar`](references/diagnostico/como-verificar.md) (Xcode, `simctl`, Gradle, `adb`, Flutter, Expo).

### Segurança e ética

Só examina apps tuas, e as verificações de segurança são sempre passivas. Nunca perde dados dos utilizadores e nunca cria clones. Também não cria contas, não faz compras e não envia para as lojas sem ti: prepara tudo e diz-te exatamente que botão carregar.

### Exemplos

- [Idear: jogos para iPhone que se fazem num mês](examples/idear.md)
- [Criar: briefing e plano de uma app de plantas](examples/criar.md)
- [Diagnosticar: relatório de uma app de receitas antes da App Store](examples/diagnosticar.md)

### Instalação

**Claude Code**

```bash
git clone https://github.com/mozuraa/claude-skill-app-studio.git ~/.claude/skills/app-studio
```

**Ou com toda a biblioteca, como plugin:**

```
/plugin marketplace add mozuraa/claude-skills
/plugin install estudios@mozuraa-skills
```

**App Claude / claude.ai:** carrega em **Code → Download ZIP** e carrega o ZIP nas **Definições**, na secção **Skills** (em *Capacidades*).

Abre uma sessão nova para a skill ser carregada. Para atualizar: `cd ~/.claude/skills/app-studio && git pull`.

### Estrutura

```
claude-skill-app-studio/
├── SKILL.md                     # os 3 modos e as regras comuns
├── references/
│   ├── idear/inspiracao.md      # géneros, utilidades, validação, comparação
│   ├── criar/                   # briefing, stack, design, lancamento
│   └── diagnostico/             # checklist (12 áreas) e como-verificar (comandos)
├── examples/                    # idear.md, criar.md, diagnosticar.md
├── icon.svg · README.md · CHANGELOG.md · LICENSE
```

### História

A versão 2.0 junta duas skills anteriores, **ideias-apps** e **app-doctor**, cujos históricos de git estão preservados neste repositório, e acrescenta o modo Criar.

### Licença

[MIT](LICENSE)

---

## English

A **complete app studio** for **Claude** (iOS, Android, Flutter, React Native/Expo, desktop), with three linked modes:

| Mode | What for | Example prompt |
|---|---|---|
| 💡 **Idear** (Ideate) | Detailed ideas for **new apps and games** you can build and ship on your own | "What game should I make next?" |
| 🛠️ **Criar** (Create) | **Builds an app with you from scratch**, from the idea and MVP to the App Store and Google Play | "I want an app to track my plants" |
| 🩺 **Diagnosticar** (Diagnose) | **Examines and fixes** everything that affects an app: 12 areas, 140+ checks, a health report with its opinion and "ready for the store?" | "My app crashes" · "Apple rejected it" |

In every mode Claude **asks questions, shows evidence, gives its honest opinion and only proceeds with your approval**.

- **Ideate:** 2–3 original, well-developed ideas (audience, core loop, differentiation, business model, effort, first steps, risks), plus an inspiration catalog with validation methods and a comparison grid.
- **Create:** 7 phases with 3 approvals. It starts with an honest MVP, follows each platform's design conventions, builds the core loop first, keeps data versioned so updates never lose progress, and finishes with a store-ready verification and launch. Guides cover technology choice, data, accounts, purchases, ads, crash reporting, costs, design and the full store submission process.
- **Diagnose:** consultation → evidence-based exam → health report → opinion → you decide → verified fixes → discharge. It covers stability, functionality, layout on every screen, icons, performance and battery, security, privacy (Privacy Manifest, labels, Data safety, ATT), accessibility, store rules, data, purchases and build.

The guides are in Portuguese, but Claude replies in the language you write in.

### Installation

```bash
git clone https://github.com/mozuraa/claude-skill-app-studio.git ~/.claude/skills/app-studio
```

Or with the whole library as a plugin: `/plugin marketplace add mozuraa/claude-skills` then `/plugin install estudios@mozuraa-skills`. For the Claude app / claude.ai, use **Code → Download ZIP** and upload it under **Settings → Skills**.

### History

Version 2.0 merges two earlier skills, **ideias-apps** and **app-doctor** (both git histories are preserved here), and adds the Create mode.

### License

[MIT](LICENSE)
