---
name: plan-ngo-event-call
description: Help an NGO, student club or institution plan an event and write a volunteer call, using what similar organisations are already running on hangel. Use when the user wants to plan an event, draft a volunteer call or announcement, choose a date that avoids clashes, or find document templates for running volunteers.
---

To plan an event and a volunteer call:

1. Ask for what is missing: purpose, audience, city or online, a date range, expected size, and which volunteer roles are needed. Use bracketed placeholders such as [organisation name] and [contact email] for anything the user has not given. Do not invent organisation details.
2. Call the hangel connector's `list_events` tool with keywords and the city to see upcoming events on similar topics, so the user can avoid date clashes and see how others describe their events.
3. Call `list_volunteering` with similar keywords to see how other organisations word volunteer roles, hours and requirements.
4. Call `search_library` for helpful templates or legislation (for example volunteer agreements or activity report templates) and list the matches with their hangel `url`.
5. Draft, in the user's language: an event brief (title, summary, agenda, roles, timeline and checklist), a volunteer call (role, tasks, time commitment, skills, what volunteers gain, how to apply) and a short announcement text.
6. Say that publishing is done by the organisation in its own hangel panel; this connector is read-only and does not create events or listings.
