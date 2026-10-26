# Skills Catalog

A small catalog of reusable instructions for coding agents. It currently includes skills for creating repository contributor guidance and generating project READMEs, intended for developers who want to reuse these workflows in agent-enabled projects.

## Skills

- [`guide/`](guide/SKILL.md) — creates an `AGENTS.md` contributor guide for a repository.
- [`readme/`](readme/SKILL.md) — generates or updates a project `README.md` based on its structure and configuration.

Each skill's `SKILL.md` contains its instructions and metadata.

## Project Structure

```text
.
├── guide/SKILL.md    # Contributor-guide generation skill
├── readme/SKILL.md   # README generation skill
├── AGENTS.md         # Repository contribution guidelines
├── LICENSE           # Apache License 2.0
└── README.md         # Catalog overview
```

## Contributing

See [AGENTS.md](AGENTS.md) for repository structure, content style, and validation guidance. This repository has no build system or automated test suite; review changes manually and run `git diff --check` before submitting.

## License

This project is licensed under the [Apache License 2.0](LICENSE).
