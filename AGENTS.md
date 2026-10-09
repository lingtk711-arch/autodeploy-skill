# AutoDeploy

This repo implements a shared toolkit for AI-generated project standardization and GitHub deployment.

## Agent-friendly workflow

1. Review the generated code for bloat and correctness
2. Scaffold a clean project layout
3. Compress noisy logs/config payloads
4. Cache project metadata across sessions
5. Push the project to GitHub automatically

## Commands

- `/autodeploy review`
- `/autodeploy scaffold auto`
- `/autodeploy compress --dry-run`
- `/autodeploy memory save my-project`
- `/autodeploy push --github-user=lingtk711-arch`

## Repo layout

- `SKILL.md` — main skill specification
- `skills/autodeploy/SKILL.md` — Claude-code friendly skill definition
- `codex.plugin.json` — Codex installation metadata
- `scripts/autodeploy.js` — command implementation

## License

MIT