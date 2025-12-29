Process all entries in ~/memory/.inbox.md and route to appropriate files.

Steps:
1. Read ~/memory/.inbox.md in full
2. For each entry, determine target domain:
   - Technical decisions/learnings → ~/memory/engineering/[relevant].md
   - Tasks/TODOs → ~/memory/tasks/active.md or ~/memory/tasks/backlog.md
   - Project updates → ~/memory/projects/[relevant].md
   - Business insights → ~/memory/business/[relevant].md
   - People/team info → ~/memory/research/people.md
   - Company intel → ~/memory/research/companies.md

3. Update target files:
   - Add new sections if needed
   - Preserve existing structure
   - Update "Last updated" timestamps
   - Cross-reference related files using [[links]]

4. Archive processed entries:
   - Move entries to ~/memory/meta/processed/[today's date].md
   - Clear ~/memory/.inbox.md

5. Git operations:
   ```bash
   git add .
   git commit -m "Daily sync: [date] - [2-3 word summary]"
   git push
   ```

Show summary:
- Files updated: [list]
- Tasks added: [count]
- Decisions captured: [count]
