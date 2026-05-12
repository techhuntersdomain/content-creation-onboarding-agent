# AINO MD Content Creator — AI Content Agency Pipeline

## What This System Is

This is an AI-powered content agency pipeline. It is built to produce high-quality, client-specific content at scale — but only after a complete, validated client profile exists.

**Current phase: Phase 1 — Client Onboarding & Discovery**

Phase 1 extracts everything needed to understand a client's business, audience, voice, goals, and constraints. No content is created until this phase is complete and the client has approved their profile.

---

## The Cardinal Rules

1. **No content is ever generated before a complete, validated client profile exists.**
   The `profile.json` for a client must exist and pass validation before any content work begins.

2. **The validation rule:** `profile.json` may not be written if any required fields are missing or remain flagged as vague. The validation layer must pass before compilation.

3. **The immutability rule:** Stage files are write-once records. Once a stage file exists, it may only be modified if:
   - The user explicitly requests a change, or
   - The agent is resolving a flagged required field during validation.
   All existing valid data must be preserved when updating a stage file.

4. **The boundary rule:** The onboarding agent never generates content, suggests content ideas, or proposes strategy. Its sole role is to extract and structure client information. If asked for content or strategy during onboarding, it acknowledges the request and explains it will be handled after the profile is complete.

---

## File Map

```
AINO MD Content Creator/
├── CLAUDE.md                          ← You are here. Read this first.
│
├── onboarding/
│   ├── onboarding_agent.md            ← Agent operating instructions (identity, rules, save logic, validation)
│   └── question_flow.md               ← Question bank for all 10 stages (core questions, branches, fallbacks)
│
├── schemas/
│   └── client_profile.schema.json     ← JSON Schema defining the complete client profile structure
│
├── memory/
│   └── client_profiles/               ← One folder per client, created at runtime
│       └── {client-id}/
│           ├── stages/                ← Stage files saved after each interview stage
│           │   ├── 01_business.json
│           │   ├── 02_offer.json
│           │   └── ... through 09_workflow.json
│           ├── profile.json           ← Final compiled profile (machine-readable, feeds future agents)
│           └── brief.md               ← Plain English summary (shared with client for approval)
│
└── workflows/
    └── run_onboarding.md              ← How to start or resume an onboarding session
```

---

## Client Folder Naming Convention

Client folders use lowercase, hyphenated names. This name becomes the `client_id` in the JSON profile.

| Client Name | Folder Name |
|---|---|
| Acme Corp | `acme-corp` |
| John Smith Consulting | `john-smith-consulting` |
| The Wellness Studio | `the-wellness-studio` |

Be consistent. The folder name is used throughout the system as the client identifier.

---

## How To Run an Onboarding Session

See `workflows/run_onboarding.md` for the exact commands to paste.

**Starting a new client:** Paste the start command with the client name and ID.
**Resuming a session:** Paste the resume command — the agent will detect which stages are complete and pick up from the next one.

---

## Project Status

| Phase | Status | Description |
|---|---|---|
| Phase 1 — Onboarding | ✅ Built | Client discovery, profile generation, client brief |
| Phase 2 — Content Strategy | 🔲 Not built | Content planning based on the client profile |
| Phase 3 — Content Creation | 🔲 Not built | Actual content generation per platform/format |
| Phase 4 — Review & Publishing | 🔲 Not built | Approval workflow, scheduling, publishing |

---

## Notes

- `.superpowers/` is used by the brainstorm visual companion — add it to `.gitignore`
- Client profiles in `memory/client_profiles/` may contain sensitive business information — treat accordingly
