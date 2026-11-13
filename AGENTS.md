# Repository Guidelines

## Project Structure & Module Organization

This repository is currently a blank workspace. Keep the root limited to
repository-wide configuration and documentation. As implementation is added,
use a predictable layout:

- `src/` for production source code, organized by feature or module.
- `tests/` for automated tests that mirror `src/` paths where practical.
- `assets/` for static, non-code resources such as images or fixtures.
- `docs/` for design notes, setup instructions, and decision records.

Avoid placing generated output, local caches, or credentials under version
control. Add the appropriate ignore rules before introducing build tooling.

## Build, Test, and Development Commands

No build system or package manager is configured yet. When one is introduced,
document the canonical commands here and in the project README. Prefer a small,
repeatable set of commands, for example:

- `npm run dev` - start the local development server.
- `npm test` - run the complete automated test suite.
- `npm run lint` - check formatting and static-analysis rules.
- `npm run build` - create a production build.

Do not add scripts that require undocumented local setup or hidden environment
state.

## Coding Style & Naming Conventions

Follow the formatter and linter selected for the language; commit formatted
code. Use 2 spaces for JSON, YAML, and JavaScript/TypeScript unless the chosen
tool enforces another convention. Name files and directories descriptively in
`kebab-case` (for example, `user-profile.ts`); use `PascalCase` for exported
types/components and `camelCase` for functions and variables. Keep modules
small, focused, and free of unrelated refactors.

## Testing Guidelines

Add tests with each behavior change. Use test names that describe observable
outcomes, such as `creates a profile when input is valid`. Keep test fixtures
minimal and deterministic. Run the full test and lint commands before opening
a pull request; add coverage expectations once a testing framework is selected.

## Commit & Pull Request Guidelines

There is no established Git history yet. Use concise, imperative commit
subjects, optionally with a conventional prefix: `feat: add profile endpoint`
or `fix: handle empty input`. Keep commits narrowly scoped.

Pull requests should explain the change, note tests run, link relevant issues,
and include screenshots for visible UI changes. Call out configuration changes,
new environment variables, or follow-up work explicitly.
