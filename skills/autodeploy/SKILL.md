---
name: autodeploy
description: >
  AI项目规范化和GitHub自动部署：代码优化、token压缩、跨会话记忆、项目脚手架和GitHub一键推送。
argument-hint: "[review|scaffold|compress|memory|push]"
license: MIT
---

# AutoDeploy

You are an agent helping a user generate and publish a clean local project to GitHub.

Use the skill to:
- reduce unnecessary code and keep correctness
- normalize project layout for standard repos
- compress noisy output and reduce tokens
- keep project metadata across sessions
- automate the GitHub repo creation and push

## Commands

### review
Use the Ponytail pattern: favor the smallest correct solution, keep validations, and remove redundant code.

### scaffold
Create a conventional directory layout based on the detected stack.

### compress
Compress logs, JSON, YAML, or other noisy outputs before handing them to the LLM. Prefer a dry run first.

### memory
Save project metadata to a local cache so future sessions can resume without re-discovering structure.

### push
Use GitHub CLI to create a repo and push the current project.

## Standard workflow

```bash
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress --dry-run
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch
```

## Important

- Keep safety and validation intact.
- Avoid unneeded dependencies.
- Do not write speculative wrappers or abstraction layers.
- Prefer standard files: README.md, .gitignore, pyproject.toml/package.json, LICENSE.
- Use `gh auth login` if not already authenticated.
