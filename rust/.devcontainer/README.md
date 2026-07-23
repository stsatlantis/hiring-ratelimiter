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
- `LiveShare` — for session sharing
- `claude` — AI agent

## Common Commands

```sh
cargo build       # compile
cargo test        # run tests
cargo clippy      # lint
cargo fmt         # format
```

## Live-Sharing Claude

Sharing terminal sessions is possible, but needs the following steps:
1. Candidate must open the Terminal view, then press Enter in it,
2. Candidate must request Terminal access by pressing the relevant button in the bottom-right corner of the screen,
3. Interviewer must accept the terminal request in read/write mode.

Claude can be quite finicky in the Live Share, the following steps are recommended to provide an okay experience:
1. Start `claude` after the candidate has access to the terminal.
2. Clear the screen with `clear` before starting `claude`.
3. Resize the VSCode window until it looks correct on the candidate's screen (usually the width needs to be decreased). The candidate might also need to resize their window, it's best to ask the candidate to share screen while you figure this out.
