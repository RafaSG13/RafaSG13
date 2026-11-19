<p align="center">
  <img src="assets/header.svg" alt="Rafa Serrano: iOS engineer, Swift, SwiftUI, UIKit; developer tools in Go and Python" width="100%">
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rafaelserranogamarra"><img src="https://img.shields.io/badge/LinkedIn-rafaelserranogamarra-0A66C2?style=for-the-badge" alt="LinkedIn"></a>
  <a href="mailto:rafasrrg13@gmail.com"><img src="https://img.shields.io/badge/Email-rafasrrg13%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Open_to-remote_iOS_roles-2ea44f?style=for-the-badge" alt="Open to remote iOS roles">
</p>

iOS engineer on the Zara app, a single app that serves every market. I've worked on it since 2023 at Nomasystems, mostly in Swift, SwiftUI and UIKit. Before that I was an Oracle DBA.

What pulls me in is how an app is put together: how it's split into modules, how it's tested and how its pieces depend on each other. Outside work I build developer tools in Go and Python, and an iOS app of my own. I ship them the way I'd want to receive them: CI on every pull request, tagged releases with a changelog, Homebrew formulae, and an `AGENTS.md` in each repository so coding agents start with the context they need.

## What I work on

- In-store features: appointment booking, orders destined for a store, and finding an item on the shop floor or in the stockroom.
- As part of the team, moving a monolithic codebase to Domain / Network / Presentation layers in Swift Package Manager modules, with unit tests on use cases, mappers and view models.
- Migrating legacy UIKit screens to SwiftUI and removing hidden dependencies on the way.
- Live Activities updated through push notifications, Apple Wallet passes, Quick Actions and accessibility work (Dynamic Type included).
- AI in the development workflow: module READMEs and `AGENTS.md` files so coding agents get context they can actually use.

That code lives in private repositories. The projects below are personal.

## Projects

### [minimal](https://github.com/RafaSG13/Minimal) · a coding-agent harness for the terminal

<p align="center">
  <a href="https://github.com/RafaSG13/Minimal"><img src="https://raw.githubusercontent.com/RafaSG13/Minimal/HEAD/assets/banner.svg" alt="minimal: bare by default, yours by config" width="100%"></a>
</p>

<p align="center">
  <a href="https://pypi.org/project/mnml-agent/"><img src="https://img.shields.io/pypi/v/mnml-agent?style=for-the-badge&color=6f86f4&label=PyPI" alt="PyPI version"></a>
  <img src="https://img.shields.io/badge/Python-3.11%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.11+">
  <img src="https://img.shields.io/badge/UI-Textual-b665ea?style=for-the-badge" alt="UI: Textual">
</p>

A small agent loop (model → tools → model) with a Textual UI, written so that every piece can be read in one sitting and replaced from a single Python file. Works with Claude, Gemini and any OpenAI-compatible server (OpenAI, OpenRouter, Ollama, LM Studio) on one provider-neutral history, so you can switch provider mid-conversation.

- Tools, slash commands, providers, hooks, panels, themes and modes are all extensions. The model knows the API: it writes its own, hot-reloads them and uses them in the same turn.
- Sub-agents with their own tools, model and provider, tracked by agent id; modes restrict which tools the model may use (a plan/build pair ships in the marketplace).
- Safe by default: confirmations, allow/deny permission rules, a project's extensions run only after `/trust`, global installs show a static scan of the code first, and edits are refused on files that changed since the model read them.
- [minimal-marketplace](https://github.com/RafaSG13/minimal-marketplace): the default git-based marketplace, with 50 extensions, tools, widgets and themes, versioned by extension API and checked in CI against every change to minimal.

```bash
uv tool install mnml-agent        # or: brew install rafasg13/tap/minimal
```

### [Pandora](https://github.com/RafaSG13/Pandora) · a terminal vault for secrets

<p align="center">
  <a href="https://github.com/RafaSG13/Pandora"><img src="https://raw.githubusercontent.com/RafaSG13/Pandora/HEAD/assets/pandora-logo.svg" alt="Pandora" width="100%"></a>
</p>

<p align="center">
  <a href="https://github.com/RafaSG13/Pandora/releases"><img src="https://img.shields.io/github/v/release/RafaSG13/Pandora?style=for-the-badge&color=a855f7" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/macOS%20%7C%20Linux%20%7C%20Windows-555555?style=for-the-badge" alt="macOS, Linux and Windows">
</p>

A full-screen TUI plus a scriptable CLI that keep API keys, tokens and passwords out of dotfiles and shell history.

- Master-password vault: names, notes and values encrypted with Argon2id and XChaCha20-Poly1305; values also kept in the OS keyring (macOS Keychain, Windows Credential Manager, Linux Secret Service) under random IDs.
- `get`, `add`, `run` (injects secrets into one process only), `gen`, encrypted `export`/`import` with age, tags and multi-line secrets such as SSH keys.
- A clipboard that clears itself after 15 seconds and is kept out of clipboard history on macOS and Windows, an idle lock that drops the key from memory, and safe concurrent writes from several processes.
- No network, no telemetry. Releases with checksums and a written threat model.

```bash
brew install rafasg13/tap/pandora
```

### [Messup](https://github.com/RafaSG13/ios-messup) · personal finance for iOS 26

<p align="center">
  <a href="https://github.com/RafaSG13/ios-messup"><img src="https://raw.githubusercontent.com/RafaSG13/ios-messup/HEAD/docs/messup-git-header.jpeg" alt="Messup: expense and payment tracking for the beautifully absent-minded" width="100%"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/iOS-26%2B-000000?style=for-the-badge&logo=apple&logoColor=white" alt="iOS 26+">
  <img src="https://img.shields.io/badge/Swift-6-F05138?style=for-the-badge&logo=swift&logoColor=white" alt="Swift 6">
  <img src="https://img.shields.io/badge/SwiftData-local--only-0A84FF?style=for-the-badge" alt="SwiftData, local-only">
</p>

Expense, income and savings tracker, my university final project rebuilt as a local-only app: no backend, no login, no third-party dependencies.

- SwiftUI with Liquid Glass, SwiftData on device, Swift 6 language mode; Model-View with `@Observable` services injected through the environment.
- Monthly and per-category budgets with notifications at 80 % and 100 %, period comparisons with projections, spending insights and CSV export.
- An App Intent to log an expense from Siri, Shortcuts, Spotlight or the Action button.
- Shared components in a local SPM design-system package; logic covered with Swift Testing.

### [NavigatorUI](https://github.com/RafaSG13/NavigatorUI) · navigation for SwiftUI

<p>
  <img src="https://img.shields.io/badge/iOS-16%2B-000000?style=for-the-badge&logo=apple&logoColor=white" alt="iOS 16+">
  <img src="https://img.shields.io/badge/SPM-compatible-F05138?style=for-the-badge&logo=swift&logoColor=white" alt="Swift Package Manager">
</p>

Lightweight navigation library inspired by `UINavigationController`, with deep linking and modular destinations.

## Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=swift,apple,go,py,githubactions,git,bash" alt="Swift, Apple platforms, Go, Python, GitHub Actions, Git, Bash">
</p>

**iOS:** Swift · SwiftUI · UIKit · SwiftData · Swift Concurrency · Swift Package Manager · Swift Testing · XCTest · App Intents · Live Activities · PassKit · Accessibility

**Tooling:** Go · Python · Textual · Bubble Tea · uv · GoReleaser · GitHub Actions · Homebrew

## Contact

I'm looking for iOS roles at product companies, ideally fully remote and international. Reach me on [LinkedIn](https://www.linkedin.com/in/rafaelserranogamarra) or at rafasrrg13@gmail.com.
