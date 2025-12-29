Add new task to ~/memory/tasks/active.md.

Interactive prompts:
1. Task description: [ask user]
2. Priority (High/Medium/Low): [ask user]
3. Related project (if any): [ask user, suggest from ~/memory/projects/]
4. Estimated effort (optional): [ask user]
5. Dependencies/blockers: [ask user]

Format and append to ~/memory/tasks/active.md:

```markdown
## [Task Title]
**Priority:** [High/Medium/Low]
**Project:** [[projects/name.md]]
**Added:** YYYY-MM-DD
**Estimate:** [effort if provided]
**Dependencies:** [blockers if any]

[Description in detail]

---
```

Update project file if task is linked to a project.

Commit:
```bash
git commit -am "New task: [task name]"
git push
```
