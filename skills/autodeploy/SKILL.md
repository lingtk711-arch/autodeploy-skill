---
name: autodeploy
description: >
  AI project standardization and GitHub publishing: Ponytail-style lean code review, Caveman-style token savings, Headroom-style memory, standard project scaffolding, and one-click GitHub push.
argument-hint: "[review|scaffold|compress|memory|push|status]"
license: MIT
---

# AutoDeploy

You are an agent helping a user generate and publish a clean local project to GitHub.

Use the skill to:
- reduce unnecessary code while keeping correctness and safety
- normalize project structure for standard repos
- compress noisy output and reduce token cost
- preserve project metadata across sessions
- automate GitHub repo creation and push

## Commands

### review
Use Ponytail-style rules: favor the smallest correct solution, keep validations, and remove redundant code.

### scaffold
Create a conventional directory layout based on the detected stack.

### compress
Compress logs, JSON, YAML, or other noisy outputs before handing them to the LLM. Prefer a dry run first.

### memory
Save project metadata to a local cache so future sessions can resume without re-discovering structure.

### push
Use GitHub CLI to create a repo and push the current project.

### status
Inspect the current project and propose the next action. This should read the project tree and infer whether it is ready to scaffold, validate, or push.

## Standard workflow

```bash
/autodeploy status
/autodeploy review
/autodeploy scaffold auto
/autodeploy compress --dry-run
/autodeploy memory save my-project
/autodeploy push --github-user=lingtk711-arch --visibility=private
```

## Important

- Keep safety and validation intact.
- Avoid unneeded dependencies.
- Do not write speculative wrappers or abstraction layers.
- Prefer minimal standard files: README.md, .gitignore, pyproject.toml or package.json, LICENSE.
- Use `gh auth login` if the GitHub CLI is not authenticated.
- Prefer `private` visibility by default unless the user explicitly wants public.
