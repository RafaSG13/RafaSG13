# Rafael Serrano Gamarra

iOS engineer on the Zara app, a single app that serves every market. I've worked on it since 2023 at Nomasystems, mostly in Swift, SwiftUI and UIKit. Before that I was an Oracle DBA.

What pulls me in is how an app is put together: how it's split into modules, how it's tested and how its pieces depend on each other. Outside work I build developer tools in Python and Go, and ship them the way I'd want to receive them: tagged releases, checksums, a changelog and a written threat model.

## What I work on

- In-store features: appointment booking, orders destined for a store, and finding an item on the shop floor or in the stockroom.
- As part of the team, moving a monolithic codebase to Domain / Network / Presentation layers in Swift Package Manager modules, with unit tests on use cases, mappers and view models.
- Migrating legacy UIKit screens to SwiftUI and removing hidden dependencies on the way.
- Live Activities updated through push notifications, Apple Wallet passes, Quick Actions and accessibility work (Dynamic Type included).
- AI in the development workflow: module READMEs and `AGENTS.md` files so coding agents get context they can actually use.

That code lives in private repositories. The projects below are personal.

## Projects

### Security

| Project | What it is | Stack |
|---|---|---|
| [Pandora](https://github.com/RafaSG13/Pandora) | A terminal vault for secrets, backed by the operating system's keyring (macOS Keychain, Windows Credential Manager, Linux Secret Service). Keeps API keys and tokens out of dotfiles and shell history. A full-screen interface plus a scriptable CLI: `get`, `add`, `run` (injects secrets into one process only), encrypted export/import, a password generator, an idle lock and a clipboard that clears itself. No network, no telemetry. Released for macOS, Linux and Windows, with checksums and a Homebrew tap: `brew install RafaSG13/tap/pandora`. | Go, OS keyring, age encryption, GoReleaser |

### AI

| Project | What it is | Stack |
|---|---|---|
| [minimal](https://github.com/RafaSG13/Minimal) | Minimal, extensible coding-agent harness for the terminal. Claude (API key or Pro/Max subscription), Gemini and any OpenAI-compatible server, switchable mid-conversation. Tools, commands, providers, hooks and widgets come from Python extensions that the agent can write and hot-reload itself, with a git-based [marketplace](https://github.com/RafaSG13/minimal-marketplace). On PyPI as `mnml-agent`. | Python 3.11+, Textual, uv |

### iOS

| Project | What it is | Stack |
|---|---|---|
| [NavigatorUI](https://github.com/RafaSG13/NavigatorUI) | Lightweight navigation library for SwiftUI, inspired by `UINavigationController`, with deep linking and modular destinations. | Swift, SwiftUI, SPM · iOS 16+ |
| [ios-messup](https://github.com/RafaSG13/ios-messup) | Personal finance app (expenses, income, savings goals), a SwiftUI rebuild of my university final project. Domain / Data / Presentation layers, JWT auth stored in the Keychain with token refresh, Swift Charts. | SwiftUI, async/await, XCTest |

## Stack

Swift · SwiftUI · UIKit · Swift Package Manager · Swift Concurrency · XCTest · Live Activities · PassKit · Accessibility · Go · Python · Textual · GoReleaser · GitHub Actions

## Contact

I'm looking for iOS roles at product companies, ideally fully remote and international.

- LinkedIn: [rafaelserranogamarra](https://www.linkedin.com/in/rafaelserranogamarra)
- Email: rafasrrg13@gmail.com
