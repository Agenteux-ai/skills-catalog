---
name: readme-gen
description: Generates or updates a README.md file from the project structure. Use 
  when the user asks to write or udpate a README, document the project, or 
  says "generate README" or "update README."
---

Generate or update the README.md file.

1. Scan the project root for:
   - pom.xml, package.json, project.json, Cargo.toml, pyproject.toml, go.mod (determine 
     language/framework)
   - Docker files (docker-compose.yml, Dockerfile)
   - CI config (.github/workflows/, .gitlab-ci.yml)
   - Environment files (.env.example)
   - License file
   - README.md (if it exists)

2. Read the main entry point to understand what the project does

3. Generate a README with these sections:

## Project Name
One-paragraph description of what the project does and who it's for.

## Getting Started

### Prerequisites
List runtime requirements found in the project.

### Installation
Step-by-step based on the actual package manager and setup files.

### Running
Based on scripts in package.json, Makefile, or common conventions.

### Environment Variables
If .env.example exists, list each variable with a description.

## Tech Stack
List frameworks and major dependencies found in package files.

## Project Structure
Show the top-level directory structure with one-line descriptions.

## Contributing
Standard contributing section if no CONTRIBUTING.md or AGENTS.md exists. If AGENTS.md file exists, reference it.

## License
Based on the LICENSE file if present.

## Rules
- Only include sections that apply to this project
- All commands must be based on actual project files, not guesses
- If something is unclear, note it rather than making it up
- If the README.md file already exists confirm with the user before updating it with new project information.
