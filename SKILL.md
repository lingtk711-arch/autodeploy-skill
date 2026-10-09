---
name: autodeploy
description: >
  AI project standardization and GitHub publishing: Ponytail-style lean code review, Caveman-style token savings, Headroom-style memory, standard scaffolding, and one-click GitHub push.
argument-hint: "[review|scaffold|compress|memory|push|status]"
license: MIT
---

# AutoDeploy

Use this skill to standardize an AI-generated local project, reduce token waste, and publish it to GitHub with a clean structure.

## Commands

- `/autodeploy review` — review code for unnecessary complexity and keep correctness intact
- `/autodeploy scaffold [python|node|go|rust|auto]` — create a conventional project skeleton
- `/autodeploy compress [--dry-run]` — compress noisy logs, config, or output payloads to reduce token cost
- `/autodeploy memory save|load|list|restore` — save and restore project metadata across sessions
- `/autodeploy push [--github-user=USER] [--visibility=private|public]` — initialize git and push to GitHub
- `/autodeploy status` — inspect the project and provide the next action recommendation

## Recommended workflow

```bash
/autodeploy status
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress --dry-run
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch --visibility=private
```

## Rules

- Prefer the smallest correct fix.
- Keep validation, error handling, and security checks intact.
- Reuse the standard library or platform features before adding custom abstractions.
- Avoid repeated code and speculative wrappers.
- Generate the minimum files needed for a clean artifact and a repository-ready project.

## GitHub push requirements

Before pushing, authenticate once:

```bash
gh auth login
```

Then run:

```bash
/autodeploy push --github-user=lingtk711-arch
```

## Why this stack works

- Ponytail: less generated code, more maintainability
- Caveman: shorter prompts and less noisy output
- Headroom: compressed context and cross-session memory
- Yeoman-like scaffolding: consistent project structure
- GitHub CLI: repeatable repo automation

## Example

```bash
/autodeploy status
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch --visibility=private
```
