<p align="center">
  <img src="icon.svg" width="160" alt="App doctor — telemóvel com batimento cardíaco, penso rápido e estetoscópio">
</p>

<h1 align="center">App doctor — Claude Skill</h1>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/Claude-Skill-D97757" alt="Claude Skill">
</p>

<p align="center">
📚 Faz parte da <b><a href="https://github.com/mozuraa/claude-skills">biblioteca de skills de mozuraa</a></b> · Part of <b><a href="https://github.com/mozuraa/claude-skills">mozuraa's skills library</a></b>
</p>

<p align="center"><b><a href="#português">Português</a> · <a href="#english">English</a></b></p>

---

## Português

Uma [skill](#o-que-é-uma-skill) para o **Claude** que funciona como **médico da tua app**, seja iOS, Android, Flutter, React Native/Expo ou desktop. Examina tudo o que afeta o bom funcionamento, mostra-te um relatório de saúde por prioridades, dá-te a opinião sincera sobre o que fazer primeiro e corrige — só o que autorizares. É especialmente útil **antes de enviar para a App Store ou para o Google Play**.

### O que examina (12 áreas)

| Área | Exemplos |
|---|---|
| 💥 **Estabilidade** | crashes, `!`/`try!`/`!!` perigosos, thread principal, concorrência, ANRs, registo de crashes |
| 🧩 **Funcionamento e idiomas** | fluxos de ponta a ponta, atualização sem perder dados, deep links, notificações, traduções, plurais, datas |
| 📐 **Layout e alinhamentos** | iPhone SE até Pro Max e iPad, áreas seguras e Dynamic Island, edge-to-edge no Android, teclado, texto grande, modo escuro, rotação |
| 🖼️ **Ícones e imagens** | ícone em todas as variantes (escuro, tingido, adaptativo, monocromático), resoluções, memória de imagens, capturas da loja |
| ⚡ **Desempenho e bateria** | arranque, bloqueios, fluidez, fugas de memória, rede, localização, tamanho da app, jogos |
| 🔒 **Segurança** | segredos dentro da app, Keychain/Keystore, HTTPS/ATS, deep links, WebViews, validação de compras, regras do backend, manifest Android |
| 🛡️ **Privacidade** | permissões e textos de pedido, Privacy Manifest e APIs de razão obrigatória, etiquetas de privacidade, Data safety, ATT, apagar conta, RGPD |
| ♿ **Acessibilidade** | VoiceOver/TalkBack, texto dinâmico, contraste, alvos de 44 pt/48 dp, reduzir movimento |
| 🏪 **Regras das lojas** | motivos de rejeição mais comuns da App Store e do Google Play, metadados, restaurar compras, Iniciar sessão com a Apple, target API |
| 📶 **Rede, offline e dados** | modo avião, erros do servidor, onde guardar dados, migrações sem perder progresso |
| 💳 **Compras e monetização** | produtos, preços da loja, estados pendente/cancelado, restaurar, subscrições, paywall honesto, anúncios |
| 🧹 **Build e código** | avisos, versões, configuração de release, assinatura, dSYM, linter, testes |

A lista completa (mais de 140 verificações) está em [`references/checklist.md`](references/checklist.md) e os comandos (Xcode, `simctl`, Gradle, `adb`, Flutter, Expo) em [`references/como-verificar.md`](references/como-verificar.md).

### Como trabalha

1. **🩺 Consulta:** faz-te algumas perguntas, como em que plataforma está a app, em que fase (desenvolvimento, quase na loja, rejeitada), se é um exame completo ou um problema concreto, e se pode corrigir.
2. **🔬 Exame:** verifica com provas. Compila a app, corre-a no simulador no ecrã mais pequeno e no maior, em modo escuro e com o maior texto, lê os registos de crash e procura no código os padrões perigosos. Sem prova, não aponta problemas.
3. **📋 Relatório de saúde:** mostra uma tabela por área (🟢🟡🟠🔴), os problemas por gravidade e, se for caso disso, a resposta a "Pronta para enviar para a loja? Sim / Ainda não".
4. **💬 Opinião e perguntas:** diz-te francamente o que faria primeiro e o que não vale o esforço, e pergunta-te o que só tu podes decidir. Se sugerires algo, diz-te honestamente se concorda e porquê.
5. **🛠️ Tratamento:** corrige uma coisa de cada vez, sem nunca perder dados dos utilizadores, verifica cada correção e pede confirmação antes de tudo o que é arriscado.
6. **✅ Alta:** resume o que ficou resolvido, o que falta, o que tens de fazer tu (por exemplo no App Store Connect) e a lista final antes de enviar para a loja.

### Exemplos de pedidos

- "A minha app crasha quando abro as definições"
- "Está pronta para enviar para a App Store?"
- "A Apple rejeitou com a regra 5.1.1, o que faço?"
- "No iPhone SE os botões ficam cortados"
- "A app é segura? Cumpre o RGPD?"
- "Revê a minha app toda e melhora o que conseguires"

Vê um exemplo completo de relatório em [`examples/exemplo.md`](examples/exemplo.md).

### Segurança e ética

A skill só examina apps que são tuas ou que estás autorizado a analisar, e todas as verificações são passivas: lê código e configuração e corre a app no simulador. Nunca ataca servidores nem explora falhas. Quando encontra um segredo exposto, não o repete e diz-te como o revogar.

### Funciona com

Swift, SwiftUI, UIKit, SpriteKit, Objective-C, Kotlin, Java, Jetpack Compose, Flutter/Dart, React Native, Expo, Electron e apps de macOS. Funciona melhor no **Claude Code**, com acesso ao projeto e ao simulador ou emulador.

### Instalação

**Claude Code (para todos os teus projetos)**

```bash
git clone https://github.com/mozuraa/claude-skill-app-doctor.git ~/.claude/skills/app-doctor
```

**Claude Code (só num projeto)** — dentro da pasta do projeto:

```bash
git clone https://github.com/mozuraa/claude-skill-app-doctor.git .claude/skills/app-doctor
```

**Ou com toda a biblioteca, como plugin:** ver [mozuraa/claude-skills](https://github.com/mozuraa/claude-skills).

**App Claude / claude.ai:** carrega em **Code → Download ZIP** e carrega o ZIP nas **Definições**, na secção **Skills** (em *Capacidades*).

Abre uma sessão nova para a skill ser carregada. Para atualizar: `cd ~/.claude/skills/app-doctor && git pull`.

### O que é uma skill?

Uma skill é uma pasta com um ficheiro `SKILL.md`: um nome, uma descrição de quando deve ser usada e instruções. O Claude lê só a descrição até ela ser útil; quando o pedido encaixa, carrega as instruções e segue-as.

### Estrutura

```
claude-skill-app-doctor/
├── SKILL.md                   # a skill: consulta → exame → relatório → decisão → tratamento → alta
├── references/
│   ├── checklist.md           # 12 áreas, 140+ verificações (iOS, Android e multiplataforma)
│   └── como-verificar.md      # Xcode, simctl, Gradle, adb, Flutter, Expo, pesquisas no código
├── examples/
│   └── exemplo.md             # exemplo de consulta e relatório
├── icon.svg
├── README.md
├── CHANGELOG.md
└── LICENSE
```

### Contribuir

As regras das lojas mudam todos os anos. Se encontrares algo desatualizado, abre uma *issue* ou um *pull request*.

### Licença

[MIT](LICENSE)

---

## English

A [skill](#what-is-a-skill) for **Claude** that acts as your **app's doctor**, for iOS, Android, Flutter, React Native/Expo or desktop. It examines everything that affects how well the app works, shows a health report by priority, gives its honest opinion on what to do first, and fixes things, but only what you approve. It's especially useful **before submitting to the App Store or Google Play**.

### What it examines (12 areas)

| Area | Examples |
|---|---|
| 💥 **Stability** | crashes, dangerous `!`/`try!`/`!!`, main thread, concurrency, ANRs, crash reporting |
| 🧩 **Functionality & languages** | end-to-end flows, updates without data loss, deep links, notifications, translations, plurals, dates |
| 📐 **Layout & alignment** | iPhone SE to Pro Max and iPad, safe areas and Dynamic Island, Android edge-to-edge, keyboard, large text, dark mode, rotation |
| 🖼️ **Icons & images** | app icon in every variant (dark, tinted, adaptive, monochrome), resolutions, image memory, store screenshots |
| ⚡ **Performance & battery** | launch, hangs, smoothness, memory leaks, network, location, app size, games |
| 🔒 **Security** | secrets inside the app, Keychain/Keystore, HTTPS/ATS, deep links, WebViews, purchase verification, backend rules, Android manifest |
| 🛡️ **Privacy** | permissions and purpose strings, Privacy Manifest and required-reason APIs, privacy labels, Data safety, ATT, account deletion, GDPR |
| ♿ **Accessibility** | VoiceOver/TalkBack, Dynamic Type, contrast, 44 pt/48 dp targets, reduce motion |
| 🏪 **Store rules** | the most common App Store and Google Play rejection reasons, metadata, restore purchases, Sign in with Apple, target API |
| 📶 **Network, offline & data** | airplane mode, server errors, where to store data, migrations without losing progress |
| 💳 **Purchases & monetization** | products, store prices, pending/cancelled states, restore, subscriptions, honest paywall, ads |
| 🧹 **Build & code** | warnings, versions, release configuration, signing, dSYMs, linter, tests |

The full list (140+ checks) is in [`references/checklist.md`](references/checklist.md) and the commands (Xcode, `simctl`, Gradle, `adb`, Flutter, Expo) in [`references/como-verificar.md`](references/como-verificar.md) (in Portuguese; Claude translates as needed).

### How it works

1. **🩺 Consultation:** asks you a few questions, such as which platform the app is on, what stage it's at (in development, about to ship, rejected), whether you want a full checkup or have a specific problem, and whether it may fix things.
2. **🔬 Examination:** checks with evidence. It builds the app and runs it in the simulator on the smallest and largest screens, in dark mode and with the largest text, reads crash logs and searches the code for dangerous patterns. Without evidence, it doesn't report a problem.
3. **📋 Health report:** shows a table by area (🟢🟡🟠🔴), the issues by severity and, when relevant, the answer to "Ready to submit? Yes / Not yet".
4. **💬 Opinion & questions:** tells you frankly what it would do first and what isn't worth the effort, and asks you about the decisions only you can make. If you suggest something, it tells you honestly whether it agrees and why.
5. **🛠️ Treatment:** fixes one thing at a time without ever losing user data, verifies each fix, and asks before anything risky.
6. **✅ Discharge:** summarizes what was fixed, what's left, what you need to do yourself (for example in App Store Connect) and a final pre-submission checklist.

### Example prompts

- "My app crashes when I open settings"
- "Is it ready for the App Store?"
- "Apple rejected it under guideline 5.1.1, what do I do?"
- "On iPhone SE the buttons get cut off"
- "Is the app secure? Is it GDPR compliant?"
- "Review my whole app and improve whatever you can"

### Safety & ethics

The skill only examines apps you own or are authorized to analyze, and every check is passive: it reads code and configuration and runs the app in the simulator. It never attacks servers or exploits anything. When it finds an exposed secret, it doesn't repeat it and tells you how to revoke it.

### Works with

Swift, SwiftUI, UIKit, SpriteKit, Objective-C, Kotlin, Java, Jetpack Compose, Flutter/Dart, React Native, Expo, Electron and macOS apps. It works best in **Claude Code**, with access to the project and a simulator or emulator.

### Installation

**Claude Code (all projects)**

```bash
git clone https://github.com/mozuraa/claude-skill-app-doctor.git ~/.claude/skills/app-doctor
```

**Claude Code (one project only)**, from the project folder:

```bash
git clone https://github.com/mozuraa/claude-skill-app-doctor.git .claude/skills/app-doctor
```

**Or with the whole library, as a plugin:** see [mozuraa/claude-skills](https://github.com/mozuraa/claude-skills).

**Claude app / claude.ai:** click **Code → Download ZIP** and upload the ZIP in **Settings**, under **Skills** (in *Capabilities*).

Start a new session so the skill is loaded. To update: `cd ~/.claude/skills/app-doctor && git pull`.

### What is a skill?

A skill is a folder with a `SKILL.md` file: a name, a description of when it should be used, and instructions. Claude only reads the description until it becomes relevant; when a request matches, it loads the instructions and follows them.

### License

[MIT](LICENSE)
