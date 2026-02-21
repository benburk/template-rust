# Template Rust

A starting point for Rust projects that constrains LLM-assisted development to a known-good structure. Without a template, every new repo gets a different project layout, different tooling choices, and different dependency decisions. This template locks in [Clippy](https://github.com/rust-lang/rust-clippy) for linting, [dprint](https://dprint.dev/) for formatting, and [Nix](https://nixos.org/) for reproducible builds — rename and customize.

## Setup Instructions

Rename the package to match your project:

1. Update `name` in `Cargo.toml`
2. Update `pname`, `description`, and `mainProgram` in `flake.nix`
3. Run `direnv allow && just bootstrap && just check`

Then start building:

- Add modules to `src/`
- Add dependencies with `cargo add`

## Development

```bash
just              # Show available recipes
just bootstrap    # Build the project
just check        # Lint and format check
just fmt          # Auto-format code
just test         # Run tests
just run          # Run the project
just build        # Build release binary
```

## Tech Stack

[Rust](https://www.rust-lang.org/) • [Clippy](https://github.com/rust-lang/rust-clippy) • [dprint](https://dprint.dev/) • [Nix](https://nixos.org/) • [direnv](https://direnv.net/) • [just](https://github.com/casey/just)
