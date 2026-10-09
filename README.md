# AutoDeploy Skill

AI project standardization and GitHub automation in one skill.

This repo combines modern agent patterns from:

- Ponytail: write less, keep the fix correct
- Caveman: shorter output and lower token cost
- Headroom: compressed context and cross-session memory
- Yeoman-style scaffolding: clean project layout
- GitHub CLI: repeatable GitHub repo creation and push

## Install

### Claude Code

```bash
/plugin marketplace add lingtk711-arch/autodeploy-skill
/plugin install autodeploy@autodeploy-skill
```

### Codex

```bash
codex plugin add github:lingtk711-arch/autodeploy-skill
```

## Quick usage

```bash
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress --dry-run
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch
```

## Included commands

- `review`: code-quality review using Ponytail-style rules
- `scaffold`: create a standard project structure for Python / Node / Go / Rust
- `compress`: shrink noisy logs, YAML, JSON, or config payloads to reduce token burn
- `memory`: save and restore project metadata across sessions
- `push`: initialize git, create a GitHub repo, and push the current project
- `status`: inspect the current project and recommended next actions

## Production workflow

```bash
cd /path/to/ai-generated-project
/autodeploy status
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress --dry-run
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch --visibility=private
```

## Example config

```json
{
  "github": {
    "user": "lingtk711-arch",
    "visibility": "private",
    "topics": ["ai-generated", "automation"]
  },
  "scaffold": {
    "auto_detect": true,
    "license": "MIT"
  },
  "compress": {
    "enabled": true,
    "exclude": ["node_modules", ".git", ".venv"]
  }
}
```

## License

MIT