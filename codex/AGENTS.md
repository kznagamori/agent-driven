# Repository Guidelines

## Project Structure & Module Organization

When this guide was created, the workspace contained no source code, tests, assets, package manifests, or Git metadata. Use `src/` for implementation, `tests/` for automated tests, and `assets/` for static resources as needed. Keep project configuration at the root. Add a `README.md` explaining the project's purpose, setup, and entry points when implementation begins.

## Development Commands

Run these commands from the repository root in PowerShell:

- `Get-ChildItem -Force`: inspect root files, including hidden configuration.
- `rg --files --hidden -g '!.git'`: list files while excluding Git internals and respecting ignore rules; requires ripgrep.

No install, build, development-server, or test commands are configured yet. When selecting a toolchain, document its exact commands in `README.md` and expose repeatable tasks through the chosen package manager or build tool.

## Coding Style & Naming Conventions

Follow the conventions of the language introduced. Use four spaces for Python and two spaces for JSON and YAML; avoid tabs in those files. Prefer descriptive names and consistent casing within each module. Configure a language-appropriate formatter and linter before adding substantial code, and commit their configuration. No formatting or linting tools are currently installed or configured.

## Testing Guidelines

No test framework or coverage threshold exists yet. Add tests with new behavior and regression tests with bug fixes. Keep tests under `tests/`, mirroring the source layout where practical. Use the selected framework's discovery convention, such as `test_parser.py` for pytest. Document the test command and any required fixtures or environment variables.

## Commit & Pull Request Guidelines

There is no Git history from which to infer commit conventions. Use concise, imperative subjects, such as `Add configuration loader`, and keep commits focused. Pull requests should explain the change, link relevant issues, and report validation performed. Include screenshots for visible UI changes and identify any setup changes.

## Security & Configuration

Keep credentials and machine-specific settings out of version control. Provide placeholder values in `.env.example` if environment configuration is introduced, and add local secrets and generated artifacts to `.gitignore`.
