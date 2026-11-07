---
name: scan-funding-calls
description: Scan the grant and funding calls that are open on hangel for a project or organisation and compare them by deadline and fit. Use when the user asks which grants or funds they can apply to, wants calls by theme, or asks to shortlist funding opportunities for an NGO, club, social enterprise or individual.
---

To scan open funding calls:

1. Ask for what is missing: organisation type (NGO, club, social enterprise, company or individual), theme, where the work happens, rough budget, and the timeframe for applying.
2. Call the hangel connector's `list_open_funds` tool several times with different theme keywords (the tool also matches common English words, so use both a Turkish and an English keyword). Collect the unique calls.
3. For the most promising calls, call `fetch` with the call's id (for example `fund:<id>`) to read the full summary.
4. Check each deadline against today's date and drop calls that have closed. Note rolling calls that have no fixed deadline.
5. Present a short table: call name, provider, deadline, budget if shown, focus areas, why it may fit, and the hangel `url`. Say when the record was last verified (`verifiedAt`) if the record shows it.
6. State clearly that eligibility and conditions must be confirmed in the provider's official call text, and do not estimate the chance of success. Mention that more detail and AI-assisted application drafting (hangel proje) are available after signing in at hangel.org.
