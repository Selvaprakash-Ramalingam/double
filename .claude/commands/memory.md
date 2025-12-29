Load complete memory context for this work session.

Read in this order:

1. **Active Context** (always read):
   - ~/memory/.inbox.md (unprocessed items)
   - ~/memory/tasks/active.md (current tasks)
   - ~/memory/tasks/waiting.md (blockers)
   - All files in ~/memory/projects/ (current projects)

2. **Domain Context** (read if relevant to session):
   - Ask: "What are we working on today?"
   - If code/technical: Read ~/memory/engineering/*.md
   - If business: Read ~/memory/business/*.md
   - If research: Read ~/memory/research/*.md
   - If personal: Read ~/memory/personal/*.md

3. **Summarize**:
   ```
   Active Tasks: [count] tasks in progress
   Projects: [list active projects]
   Unprocessed Inbox: [count] items
   Current Blockers: [list from waiting.md]
   Relevant References: [files loaded]
   ```

Do NOT update any files. This is read-only context loading.
