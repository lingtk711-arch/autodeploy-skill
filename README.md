# AutoDeploy Skill

AI project standardization and GitHub automation in one skill.

This repository combines the best ideas from:
- Ponytail: write less, keep correctness
- Caveman: shorter outputs and lower token use
- Headroom: compressed context and session memory
- Yeoman-style scaffolding: standard project layout
- GitHub CLI: automatic GitHub pushes

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

## Usage

```bash
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress --dry-run
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch
```

## Included commands

- `review` — code quality review using Ponytail-style rules
- `scaffold` — create a conventional project structure
- `compress` — compress logs/config output to reduce token use
- `memory` — save and restore project metadata across sessions
- `push` — create a GitHub repo and push the project

## License

MIT