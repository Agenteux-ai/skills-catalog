# Repository Guidelines

## Project Structure & Module Organization
This repository is a small catalog of reusable coding-agent skills, not an application. Each skill lives in its own top-level directory (currently `guide/` and `readme/`) and is defined by a `SKILL.md` file containing YAML frontmatter and instructions. Keep additions self-contained in a clearly named directory. The root `README.md` provides the catalog description; `LICENSE` applies to the repository. There is no separate source, test, or asset tree at present.

## Build, Test, and Development Commands
There is no build system or automated test suite configured. For local inspection, use:

- `find . -maxdepth 2 -type f | sort` to review the catalog files.
- `git diff --check` to catch whitespace errors before submitting changes.
- `git status --short` to confirm the intended files changed.

When changing a skill, verify that its frontmatter and instructions agree and that references point to real files.

## Content Style & Naming
Use Markdown for skill instructions and keep each skill's entry point named `SKILL.md`. Use lowercase, hyphen-separated directory names that describe the skill. Follow the existing format: YAML frontmatter with a concise `name` and `description`, followed by direct, actionable instructions. Prefer short headings and bullet lists; avoid claiming commands, tooling, or capabilities that are not supported by repository files. Preserve consistent Markdown spacing and end files with a newline.

## Testing Guidelines
No test framework, test naming convention, or coverage target is currently defined. Review documentation changes manually for clarity, accuracy, valid relative references, and consistency with the target skill. Run `git diff --check` as a minimum validation.

## Commit & Pull Request Guidelines
The available Git history uses short, imperative summaries (for example, “Initial commit of 'guide' and 'readme' skills.”). Keep commit subjects concise and describe the change. Pull requests should explain the skill or documentation change, identify affected paths, and include any relevant manual validation; link an issue when one exists. Screenshots are generally unnecessary for this documentation-focused repository.
