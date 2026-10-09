---
name: autodeploy
description: >
  AI项目规范化和GitHub自动部署：用 Ponytail 规则压缩代码、Caveman 优化 token、Headroom 缓存上下文、Yeoman 风格脚手架和 GitHub 一键推送。
argument-hint: "[review|scaffold|compress|memory|push]"
license: MIT
---

# AutoDeploy

Use this skill to standardize an AI-generated project, reduce token waste, and publish it to GitHub with a clean structure.

## Commands

- `/autodeploy review` — review code for unnecessary complexity and hidden risk
- `/autodeploy scaffold [python|node|go|rust|auto]` — create a conventional project skeleton
- `/autodeploy compress [--dry-run]` — compress noisy logs/config outputs to save tokens
- `/autodeploy memory save|load|list|restore` — persist project metadata across sessions
- `/autodeploy push [--github-user=USER]` — initialize git and push to GitHub

## Workflow

1. Review the code with Ponytail-style minimalism rules.
2. Normalize the project layout.
3. Compress bulky logs, YAML, JSON, or command output.
4. Save project metadata for later sessions.
5. Create a GitHub repo and push.

## Rules

- Prefer the smallest correct change.
- Keep safety, validation, and error handling.
- Reuse standard library or built-in platform features before adding custom code.
- Avoid repeated code and unnecessary scaffolding.
- Generate the minimum files needed for a clean artifact and a repository-ready project.

## Push requirements

Before pushing:

```bash
gh auth login
```

Then run:

```bash
/autodeploy push --github-user=lingtk711-arch
```

## Best-practice stack

- Ponytail: less generated code, better maintainability
- Caveman: shorter prompts and compressed output
- Headroom: cross-session memory and compressed context
- Yeoman-style templates: consistent layout
- GitHub CLI: repeatable repo automation

## Example

```bash
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch
```
