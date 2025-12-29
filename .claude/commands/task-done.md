Mark a task as complete.

Interactive flow:
1. Read ~/memory/tasks/active.md
2. Show list of active tasks
3. Ask: "Which task number to mark done?"
4. User selects task

5. Update ~/memory/tasks/active.md:
   - Add [DONE YYYY-MM-DD] tag to task
   - Move to "Completed" section or remove if trivial

6. Update related files:
   - If task references project: Update project status
   - If task spawned from research: Note completion

7. Commit:
   ```bash
   git commit -am "Task complete: [task name]"
   git push
   ```
