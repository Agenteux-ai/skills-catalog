# Pi Extensions

A library of useful Pi (coding agent) extensions.

## Installing an extension

Pi loads TypeScript and JavaScript files from its extension directories. For directory-based extensions, it looks for an `index.ts` or `index.js` entry point. This repository's extensions use that directory layout.

### Available in all Pi sessions

Copy an extension directory into Pi's user extension directory:

```text
~/.pi/agent/extensions/exit/index.ts
```

For this repository, copy `pi-extensions/exit/` to `~/.pi/agent/extensions/exit/`. The user extension directory is based on Pi's agent directory, which defaults to `~/.pi/agent` and can be changed with `PI_CODING_AGENT_DIR`.

### Available in one project

From the project root, copy the extension directory into the project's `.pi/extensions/` directory:

```text
.pi/extensions/exit/index.ts
```

Project extensions load after project trust is granted. Alternatively, list a file or directory path under `extensions` in `.pi/settings.json`:

```json
{
  "extensions": ["./extensions/exit"]
}
```

Paths in project settings resolve from `.pi/`, so this example refers to `.pi/extensions/exit/`.

After installing or changing an extension while Pi is running, use `/reload` to reload resources. Otherwise, start a new Pi session. For example, the `exit` extension registers `/exit`, which shuts Pi down immediately.
