# How To Run an Onboarding Session

This file contains the exact commands to paste when starting or resuming a client onboarding session in Claude Code.

---

## Before You Start

Make sure you are:
- Working in the `AINO MD Content Creator` project directory in Claude Code
- Starting a **new conversation** (not continuing an old one)
- Have the client's name ready and a folder name decided

**Client folder naming rule:** Use lowercase, hyphenated names. The folder name becomes the client's permanent ID throughout the system.

| Client Name | Client ID (folder name) |
|---|---|
| Acme Corp | `acme-corp` |
| John Smith Consulting | `john-smith-consulting` |
| The Wellness Studio | `the-wellness-studio` |

Be consistent. Once a folder is created, do not rename it.

---

## Starting a Fresh Client Session

Paste this into a new Claude Code conversation:

```
Read onboarding/onboarding_agent.md and follow it exactly.

The client name is: [FULL CLIENT NAME]
The client ID is: [lowercase-hyphenated-id]

Run the startup routine now. This is a fresh session — no stage files exist yet.
```

**What happens next:**
1. The agent runs its startup routine and confirms no stages exist
2. It delivers the Opening Preamble
3. It begins Stage 1: Business Context
4. After each stage completes, it saves a file to `memory/client_profiles/[client-id]/stages/`
5. This continues through Stage 9, then compiles the final profile at Stage 10

---

## Resuming a Partial Session

If a session was interrupted or spread across multiple sittings, paste this:

```
Read onboarding/onboarding_agent.md and follow it exactly.

The client name is: [FULL CLIENT NAME]
The client ID is: [lowercase-hyphenated-id]

Run the startup routine now. This is a resume — check memory/client_profiles/[client-id]/stages/ to see which stages are already complete, then pick up from the next pending stage.
```

**What happens next:**
1. The agent scans the stages folder and identifies which stage files exist
2. It announces which stages are complete and where it's resuming from
3. It picks up from the first incomplete stage without repeating any completed ones

---

## After Onboarding Completes

When Stage 10 finishes, two files will be saved:

| File | Purpose |
|---|---|
| `memory/client_profiles/[client-id]/profile.json` | Machine-readable profile — feeds future agents |
| `memory/client_profiles/[client-id]/brief.md` | Plain English summary — share with client |

**Your next steps:**

1. **Open `brief.md`** — read it top to bottom and check for any fields marked as needing more detail

2. **Check the Readiness Score** at the bottom of the brief:
   - **High (85–100):** Data is complete and specific. Ready to begin content creation.
   - **Medium (65–84):** Usable, but some areas lack depth. Content can begin, but a follow-up may be needed before highly targeted work.
   - **Low (below 65):** Significant gaps exist. Schedule a follow-up session before starting content work.

3. **Share `brief.md` with the client** for their review and approval
   - The brief is written in plain English — no jargon, no technical terms
   - The client should confirm it accurately reflects their business before content creation begins

4. **Once the client approves the brief** → Phase 2 (content strategy) can begin
   - Phase 2 is not yet built. The approved profile is the foundation it will use.

---

## Updating a Specific Answer After Onboarding

If the client wants to change or add to an answer after a stage is complete, paste this:

```
Read onboarding/onboarding_agent.md and follow it exactly.

The client ID is: [client-id]

The client wants to update their answer for Stage [N] — specifically [describe the field or topic]. Load the existing stage file, update only the relevant field, and preserve all other data. Re-save the file and confirm what was changed.
```

The agent will load the existing stage file, change only what was requested, and preserve everything else.

---

## What the Readiness Score Means

The readiness score is calculated at Stage 10 based on how complete and specific the client's answers were.

| Score | Label | What It Means |
|---|---|---|
| 85–100 | High | All required fields are filled and specific. Content creation can begin immediately. |
| 65–84 | Medium | Most data is solid, but some areas need more depth. Usable, but flag those areas for follow-up before certain content types. |
| Below 65 | Low | Too many gaps or vague answers. Recommend a follow-up session before starting content work. |

Flags in the brief show exactly which areas are weak and why.

---

## File Reference

| File | What It Is |
|---|---|
| `CLAUDE.md` | Project overview and rules — always read first |
| `onboarding/onboarding_agent.md` | Full agent operating instructions |
| `onboarding/question_flow.md` | Question bank for all 10 stages |
| `schemas/client_profile.schema.json` | JSON Schema defining the profile structure |
| `memory/client_profiles/` | Where all client data is saved |
| `workflows/run_onboarding.md` | This file — how to run a session |
