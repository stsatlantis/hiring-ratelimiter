# Dev Container Setup

## Prerequisites

- [Colima](https://github.com/abiosoft/colima) — lightweight container runtime for macOS (replaces Docker Desktop)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) (`ms-vscode-remote.remote-containers`)

### Installing Colima

```sh
brew install colima docker
colima start
```

`colima start` launches the container runtime. Run it once after each reboot, or set it to start automatically:

```sh
brew services start colima
```

## Getting Started

1. Ensure Colima is running (`colima status`).
2. Open this repository in VS Code.
3. When prompted _"Reopen in Container"_, click it. If the prompt does not appear, open the Command Palette (`Cmd+Shift+P` / `Ctrl+Shift+P`) and run **Dev Containers: Reopen in Container**.
4. VS Code will build the container and install the extensions automatically. This may take a few minutes on first run.

## What's Included

- Latest stable Rust toolchain (via `rustup`)
- `clippy` — linter
- `rustfmt` — formatter
- `rust-analyzer` — language server (autocomplete, go-to-definition, inline errors)
- `CodeLLDB` — native debugger
- `Even Better TOML` — syntax support for `Cargo.toml`

## Common Commands

```sh
cargo build       # compile
cargo test        # run tests
cargo clippy      # lint
cargo fmt         # format
```
