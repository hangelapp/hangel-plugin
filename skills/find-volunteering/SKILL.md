---
name: find-volunteering
description: Find volunteering opportunities on hangel that fit a person's interests, skills, city, time and format. Use when the user asks where they can volunteer, wants an opportunity matched to their skills, or asks about online, remote or urgent volunteering in Turkiye.
---

To find volunteering opportunities:

1. Ask only for what is missing: city (or "online"), cause or interests, skills, how much time, and whether the user wants a one-off or a regular commitment. Do not ask for a name, ID number, phone number or other personal data.
2. Call the hangel connector's `list_volunteering` tool with a short keyword for the cause, the city, and `online: true` if the user wants remote work. Use `urgentOnly: true` only if the user asks for urgent needs. Records are mostly Turkish; the tool also matches common English words, so try both a Turkish and an English keyword when the first search returns little.
3. If the user wants a longer-term connection to a cause, also call `search_ngos` for NGOs in that cause area and city, and `list_events` for upcoming events they could attend first.
4. Present three to seven options. For each: title, organisation, city or online, time commitment and application deadline when the record has them, and the hangel `url`. Translate Turkish text for the user and keep the original title next to it.
5. Say that applications are made by the user on the hangel page; the connector only reads public listings and cannot apply on their behalf.
6. If nothing fits, widen the keywords or city, suggest online opportunities or events, and say plainly that no match was found. Never invent a listing or state availability that the record does not show. Check each deadline against today's date before recommending it.
