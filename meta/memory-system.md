# Double Memory System Rules

## Core Concept
This is **Double**, an external memory system for LLMs. Since AI assistants lack native memory between sessions, this directory structure provides persistent context that can be loaded at the start of each interaction.

## Update Frequency Guidelines
- `engineering/*` - Update when you learn a new pattern or best practice
- `projects/*` - Update when priorities shift or decisions are made
- `tasks/*` - Update daily as work progresses
- `business/*` - Update when tracking business metrics, ideas, or insights
- `personal/*` - Update when capturing writing style, ideas, or preferences
- `meta/*` - Update when the system itself changes

## Agent Responsibilities
When working on a project with both workspaces open:
1. Update `projects/[name].md` with high-level decisions
2. Update `tasks/active.md` as you complete work
3. Update `engineering/*` when you discover reusable patterns
4. Update `business/*` when tracking business metrics or insights
5. **Check for staleness:** When updating a fact, search for cross-references and update them
6. **Maintain SSOT:** If information exists in multiple places, consolidate to one canonical location
7. **Date your updates:** Add "Last updated: YYYY-MM-DD" when modifying time-sensitive info

## Staleness Prevention

### Single Source of Truth (SSOT)
- Store each fact in **one canonical location**
- Use cross-references instead of duplicating information
- Example: Store company funding in `research/companies.md`, reference it from other files
- When updating canonical data, check for cross-references that might need updating

### Review Schedule
- **Daily:** `tasks/active.md`, `tasks/backlog.md`, `tasks/waiting.md`
- **Weekly:** `projects/*.md` (current priorities, decisions)
- **Monthly:** 
  - `research/companies.md` (funding rounds, team changes)
  - `research/people.md` (new content, role changes)
  - `business/*` (metrics, active ideas)
- **Quarterly:** 
  - `engineering/*.md` (best practices evolution, new patterns)
  - `research/markets.md` (market trends)
- **Annually:** `personal/*.md` (writing style, preferences)

### Dated Information
Add timestamps to facts that commonly change:
```markdown
- **Stage:** Series B, $675M - *verified 2025-12-22*
- **Last updated:** 2025-12-22
```

### Cross-Reference Format
Use consistent linking:
```markdown
See research/companies.md#CompanyName for details
[Company](research/companies.md#CompanyName) announced...
```

### When Information Changes
1. Update the canonical source
2. Search for cross-references: `grep -r "old fact" .`
3. Update or verify cross-references are still accurate
4. Note the change in `meta/changelog.md` if significant

## File Naming Conventions
- Use lowercase with hyphens for multi-word files: `memory-system.md`
- Use descriptive names that indicate content: `python.md` not `lang1.md`
- Keep filenames concise but clear

## Writing Style
- Use markdown for all files
- Keep entries concise and scannable
- Use bullet points and headers liberally
- Date-stamp significant updates when relevant
- Write for your future self - assume no context

## Git Workflow
- Commit regularly as knowledge accumulates
- Use descriptive commit messages: "Add async patterns to Python guide"
- Push to keep remote backup current
- Private repo for personal thoughts, public template for structure
