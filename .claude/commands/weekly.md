Generate comprehensive weekly review and synthesis.

Read ALL context:
1. ~/memory/tasks/active.md (what's in progress)
2. ~/memory/tasks/backlog.md
3. ~/memory/tasks/waiting.md
4. All ~/memory/projects/*.md files
5. ~/memory/meta/processed/*.md from this week
6. Previous week's review if exists

Analyze:
- What tasks were completed? (marked [DONE])
- What decisions were made? (from processed entries)
- What was learned? (engineering/business insights)
- What's blocking progress?
- Which projects are healthy vs stale?

Generate weekly_reviews/[YYYY-MM-DD].md:

```markdown
# Weekly Review: Week of [Date]

## Summary
[2-3 sentence overview of the week]

## Completed Tasks
- [Task 1] - [brief note]
- [Task 2] - [brief note]
- ...

## In Progress
- [Active task 1] - Status: [%]
- [Active task 2] - Status: [%]

## Key Decisions
- [Decision 1]: [rationale]
- [Decision 2]: [rationale]

## Learnings
### Engineering
- [Pattern/insight learned]

### Business
- [Market/strategy insight]

## Blockers & Challenges
- [Current blocker 1]
- [Current blocker 2]

## Project Health Check
- **[Project A]**: [Status] - Last updated: [date]
- **[Project B]**: [Status] - Last updated: [date]

## Stale Items
- [Projects not updated in 2+ weeks]
- [Tasks stuck in waiting too long]

## Next Week Priorities
1. [Top priority]
2. [Second priority]
3. [Third priority]

## System Health
- Files updated this week: [count]
- SSOT violations: [list any inconsistencies found]
- Recommendations: [suggestions for system improvement]
```

Display to terminal for review.
Ask: "Commit this review? (y/n)"
If yes, commit and push.
