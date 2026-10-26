# Agenteux Skills and Pi Extensions

A small collection of reusable coding-agent skills and Pi extensions. The skills provide workflows for creating repository contributor guidance and generating project READMEs; the Pi extension adds an immediate `/exit` command for users who prefer it to `/quit`.

## Getting Started

### Prerequisites

- A coding agent that supports the Agent Skills format to use the skills.
- [Pi](https://github.com/earendil-works/pi) to use the Pi extension.

### Installation

This repository has no package manifest or automated installer. Use the skill directories with your coding agent's skill-loading mechanism. Load `pi-extensions/exit/index.ts` through Pi's extension mechanism (for example, pass its path with `pi --extension`).

### Running

Once loaded in Pi, enter `/exit` to shut Pi down immediately.

## Contents

- `guide/` — skill for creating an `AGENTS.md` repository guide.
- `readme/` — skill for generating or updating a project README.
- `pi-extensions/exit/` — Pi extension implementing the `/exit` command.

## Tech Stack

- Markdown for skills and documentation.
- TypeScript for the Pi extension, using Pi's `ExtensionAPI`.

There are no package manifests or declared third-party dependencies in this repository.

## Project Structure

```text
.
├── guide/SKILL.md                # Contributor-guide generation skill
├── readme/SKILL.md               # README generation skill
├── pi-extensions/README.md       # Pi extensions catalog
├── pi-extensions/exit/           # Immediate /exit command extension
├── AGENTS.md                     # Repository contribution guidelines
├── LICENSE                       # Apache License 2.0
└── README.md                     # Project overview
```

## Contributing

See [AGENTS.md](AGENTS.md) for repository structure, content style, and validation guidance. There is no build system or automated test suite; run `git diff --check` to check changes for whitespace errors.

## License

This project is licensed under the [Apache License 2.0](LICENSE).
