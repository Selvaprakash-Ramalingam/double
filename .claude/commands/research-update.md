Update company research intelligence from job postings.

Read ~/memory/research/companies.md and extract:
- Company names
- Career page URLs
- Last updated timestamps

For each company:
1. Fetch careers page via https://r.jina.ai/[url]
2. Extract current job postings
3. Compare to stored data in companies.md
4. Identify changes:
   - New roles posted
   - Roles removed (filled/canceled)
   - Tech stack keywords changed
   - Team size signals
   - Growth indicators (rapid hiring, new departments)

5. Update companies.md:
   - Add [UPDATED: YYYY-MM-DD] tag
   - Update role listings
   - Note significant changes in company section
   - Update tech stack if new technologies mentioned

6. Append significant findings to ~/memory/research/markets.md:
   ```markdown
   ## [YYYY-MM-DD] Company Updates
   - [Company A]: Now hiring 3 ML engineers (was 0) - AI pivot signal
   - [Company B]: Removed all junior roles - possible hiring freeze
   - [Company C]: New roles in Rust/WASM - tech stack evolution
   ```

7. If substantial changes, commit:
   ```bash
   git commit -am "Research: Updated [X] companies"
   git push
   ```

Rate limiting: Wait 3 seconds between company fetches.
Show progress: "[X]/[total] companies processed"
