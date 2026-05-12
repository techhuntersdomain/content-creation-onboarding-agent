# Question Flow — All 10 Stages

This file is the agent's question bank. For each stage, use the structure below. Adapt wording to the conversation — these are guides, not scripts.

**Stage structure:**
- **Goal** — what completing this stage gives us
- **Cross-Stage References** — what to check from prior stages before asking
- **Core Questions** — the primary questions to ask (adapt order to flow naturally)
- **Adaptive Follow-ups** — ask only if triggered by an earlier answer
- **Depth Check** — vague patterns to catch and how to probe them
- **"I Don't Know" Fallback** — how to help a stuck client
- **Stage Complete When** — measurable criteria for all required fields
- **Saves to** — the file path for this stage's data

---

## Stage 1 — Business Context

**Goal:** Understand the playing field — what they do, what industry they're in, where they are in their growth, and what makes them different.

**Cross-Stage References:** None — this is the first stage.

**Core Questions**
1. Tell me about your business. What do you do, and how long have you been doing it?
2. What industry are you in, and how would you describe your business to someone who's never heard of you?
3. What stage is the business at right now — early-stage and still finding your footing, or established and looking to grow?
4. What makes you different from others in your space? What's the thing your best clients say about you that competitors can't claim?
5. Who's behind the business — is it just you, or do you have a team? Roughly how many people?

**Adaptive Follow-ups**
- If "startup" or "early stage" → *"What's the biggest challenge you're working through right now as a business?"*
- If "established" or "enterprise" → *"What's the next growth milestone you're focused on?"*
- If location is mentioned → *"Are you primarily local, national, or international in how you serve clients?"*
- If "I've been doing this for years" → *"Has the business evolved significantly from what it started as?"*

**Depth Check**
- Watch for: vague differentiators like "we really care about our clients" or "we deliver results"
- Probe with: *"That's a great start — can you get more specific? What's something a competitor genuinely can't say about themselves that you can?"*
- Watch for: one-line business descriptions
- Probe with: *"Can you expand on that a bit? Walk me through what a typical engagement or transaction looks like from the client's perspective."*

**"I Don't Know" Fallback**
If they can't articulate their differentiator: *"Let me try a different angle — think about the last client who gave you a glowing review or referral. What did they say you did that surprised them? That's often where the real differentiator lives."*

**Stage Complete When:**
- Business name ✓
- Industry ✓
- Business description ≥ 2 sentences ✓
- Differentiator is specific and non-generic ✓
- Business stage (startup/growth/established/enterprise) ✓
- Team size (approximate) ✓

**Saves to:** `stages/01_business.json`

---

## Stage 2 — Offer / Product / Service

**Goal:** Understand exactly what the content needs to sell — the primary offer, what clients actually get, and the real objections that stand in the way of a sale.

**Cross-Stage References:**
- Business model from Stage 1 → shapes how you ask about delivery and pricing
- Business stage → a startup may have one offer; established businesses may have several

**Core Questions**
1. Walk me through your main offer — what exactly does someone get when they work with or buy from you?
2. How do clients typically come to you, and how does the buying process work?
3. What does a client's life or business look like after working with you? What's the real transformation?
4. What's the typical investment for your primary offer — or at least a ballpark range?
5. What objections do you hear most often from people who are close to buying but haven't yet?

**Adaptive Follow-ups**
- If multiple offers mentioned → *"Which one is your primary focus right now — the one you most want content to drive?"*
- If "high-ticket" or premium pricing → *"What's the typical sales cycle like — are people usually ready to buy quickly, or does it take time to build trust first?"*
- If "subscription" or recurring → *"What's the main reason people cancel or don't renew?"*
- If "done-for-you" service → *"What does the client experience look like during delivery — how hands-on are they?"*
- If digital product or course → *"What's the completion rate like, and what do people say once they've finished?"*

**Depth Check**
- Watch for: vague outcomes like "they grow their business" or "they feel better"
- Probe with: *"Can you give me a specific example? Think of your best client result — what actually changed for them, and ideally in measurable terms?"*
- Watch for: objections described as "price" with no nuance
- Probe with: *"When someone says it's too expensive, what do you think is really going on — is it a value question, a timing issue, or something else?"*

**"I Don't Know" Fallback**
If they struggle to articulate the transformation: *"Think about a client who got the best possible result from working with you. Before they came to you, what was their situation? And after — what had changed? Walk me through both sides of that."*

**Stage Complete When:**
- Primary offer described ✓
- Delivery model identified ✓
- ≥ 2 specific client outcomes (not generic) ✓
- Price range or tier acknowledged ✓
- ≥ 1 real objection named ✓

**Saves to:** `stages/02_offer.json`

---

## Stage 3 — Target Audience

**Goal:** Know exactly who the content is written for — their demographics, what they believe, what they're struggling with, and where they spend their time.

**Cross-Stage References:**
- Stage 1 B2B → shift to firmographic questions (job titles, company sizes, industries served, buying committees)
- Stage 1 B2C → focus on individual demographics, emotions, lifestyle
- Stage 2 transformation → use it to infer audience pain points and frame questions

**Core Questions**
1. Who is your ideal client — describe them as specifically as you can. Who do you do your best work with?
2. What are the biggest challenges or frustrations your audience is dealing with right now — the ones that keep them up at night?
3. What have they already tried before finding you, and why didn't it work?
4. What does your audience believe about their problem that might actually be holding them back — even if it's not true?
5. Where does your audience spend time online — which platforms, communities, or media do they pay attention to?

**Adaptive Follow-ups**
- If B2B → *"What job titles typically make the buying decision? And who else is usually involved in that decision?"*
- If B2B → *"What size companies do you work best with — is there a sweet spot in terms of headcount or revenue?"*
- If B2C → *"Roughly what age range are we talking about? And is there a gender skew, or is it pretty even?"*
- If "coaches" or "consultants" audience → *"Are these people just starting out, or are they already established and looking to scale?"*
- If niche audience mentioned → *"Are there specific communities, podcasts, publications, or influencers this audience follows?"*

**Depth Check**
- Watch for: audience described too broadly ("small business owners", "entrepreneurs", "women 25-45")
- Probe with: *"Can you get more specific? Of all the people who match that description, who is your absolute best-fit client? What makes them different from everyone else in that group?"*
- Watch for: pain points stated too generally ("they want more clients", "they're stressed")
- Probe with: *"Tell me more about that stress — what does a bad day actually look like for them? What are they thinking about when they wake up at 3am?"*

**"I Don't Know" Fallback**
If they can't define the audience: *"Let's work backwards. Think about your three best clients — the ones you'd clone if you could. What do they have in common? Not just demographics — what was their mindset, their situation, their frustrations when they came to you?"*

**Stage Complete When:**
- Primary audience segment described specifically ✓
- ≥ 3 pain points with enough detail to write to them ✓
- Something about what they've tried and why it failed ✓
- At least one existing belief or misconception identified ✓
- ≥ 1 online platform or community where they gather ✓

**Saves to:** `stages/03_audience.json`

---

## Stage 4 — Brand Voice & Tone

**Goal:** Define the writing style — the personality the brand communicates through, the adjectives that describe it, and what it should never sound like.

**Cross-Stage References:**
- Stage 3 pain points → *"When you speak to [specific pain point], what tone feels right — urgent and direct, or empathetic and patient?"*
- Stage 1 business stage → a startup might be punchy and bold; an established firm might be measured and authoritative
- Stage 2 offer type → high-ticket often means more trust-building tone; low-ticket can be more direct

**Core Questions**
1. How would you describe the personality of your brand? If it were a person at a dinner party, what would they be like?
2. Give me 3–5 words that describe how you want to sound. Not what you do — how you sound.
3. What do you absolutely never want to sound like? What would make you cringe if you saw it on your own content?
4. On a scale from very casual (like texting a friend) to very formal (like a corporate report) — where does your brand sit?
5. Is there a brand, creator, or piece of content — inside or outside your industry — that you think gets it right? What specifically do you like about it?

**Adaptive Follow-ups**
- If tone descriptors are generic ("professional", "friendly") → *"Give me an example of what [professional/friendly] sounds like for your brand specifically. What would a sentence in that voice actually say?"*
- If they mention a reference brand → *"What specifically about [brand] resonates — the vocabulary they use, the topics they cover, the attitude, something else?"*
- If "I don't want to sound salesy" → *"What does 'salesy' mean to you — what's the specific thing you want to avoid?"*
- If high-stakes industry (legal, finance, medical) → *"Does being authoritative ever feel at odds with being approachable for you? How do you balance that?"*

**Depth Check**
- Watch for: all five adjectives being safe/generic ("professional, friendly, helpful, modern, trustworthy")
- Probe with: *"Those make sense as a baseline — but what makes your voice distinct within those? If two brands were both professional and friendly, what makes yours yours?"*
- Watch for: "just be authentic" as a voice descriptor
- Probe with: *"Authenticity means something different for every brand — can you show me what that looks like? Describe a moment or a piece of content that felt genuinely you."*

**"I Don't Know" Fallback**
If they can't describe the voice: *"Let's try something different — tell me about a brand you follow or a writer you enjoy reading. It doesn't have to be in your industry. What is it about how they communicate that you like? We can work backwards from that."*

**Stage Complete When:**
- ≥ 3 tone descriptors identified (at least one is specific, not generic) ✓
- ≥ 1 "never sound like" example with enough detail to act on ✓
- Formality level placed on the spectrum ✓
- At least one reference or anti-reference noted ✓

**Saves to:** `stages/04_voice.json`

---

## Stage 5 — Content Goals

**Goal:** Align content to business outcomes — understand what success looks like, what's been tried before, and what the content is actually supposed to do.

**Cross-Stage References:**
- Stage 2 offer type → high-ticket = trust/authority goals; low-ticket = volume/awareness goals
- Stage 2 objections → content goals should address these; flag if there's a mismatch
- Stage 3 audience online behaviour → channels where goals can realistically be achieved

**Core Questions**
1. What do you want content to actually do for your business — what's the number one outcome you're looking for?
2. How will you know it's working? What does success look like in concrete, measurable terms?
3. What's your timeline — when do you want to start seeing results, and are there any key dates or launches coming up?
4. Have you tried content marketing before? If so, what happened — and if it didn't work, what do you think went wrong?
5. Is content marketing a significant investment for you right now, or are you testing the waters?

**Adaptive Follow-ups**
- If "lead generation" → *"What does a qualified lead look like for you — what action do you want them to take?"*
- If "brand authority" → *"Authority with whom specifically — your existing audience, a new audience, industry peers, press?"*
- If "tried it before and it didn't work" → *"Walk me through what you tried — how long, what platform, how consistent, and what metric told you it wasn't working?"*
- If vague KPI ("more engagement", "go viral") → *"Let's make that more specific — if you could choose one number to look at 90 days from now that would tell you content is working, what would it be?"*
- If upcoming launch mentioned → *"Tell me more about that — when is it, and what role do you want content to play in it?"*

**Depth Check**
- Watch for: "I just want to grow my audience" with no specificity
- Probe with: *"Grow it into what? What happens once the audience is bigger — what's the step that follows?"*
- Watch for: KPIs that can't be measured ("credibility", "trust", "visibility")
- Probe with: *"How would you measure that? What would you point to in 6 months as evidence that you'd built [credibility/trust]?"*

**"I Don't Know" Fallback**
If they're unsure what success looks like: *"Let's work backwards — if content was working perfectly a year from now, what would be different about your business? More clients? Higher prices? Speaking invitations? Press? Start there and we'll figure out what to measure."*

**Stage Complete When:**
- Primary goal maps to one of: lead_generation, brand_authority, community_building, direct_sales, retention, awareness ✓
- Primary KPI is measurable (not just aspirational) ✓
- Timeline acknowledged (even "ASAP" or "no specific deadline" is valid) ✓
- Previous content attempts noted, or confirmed this is their first time ✓

**Saves to:** `stages/05_goals.json`

---

## Stage 6 — Platforms & Formats

**Goal:** Know exactly which channels to create for, in what formats, and at what frequency — and understand any platform-specific operational context.

**Cross-Stage References:**
- Stage 3 online hangouts → prioritise platforms where the audience already is
- Stage 5 previous attempts → note if a platform was tried and failed — approach it directly
- Stage 5 timeline/budget → calibrate how ambitious the platform plan should be
- Stage 1 team size → solo operators need lighter production formats

**Core Questions**
1. Where do you want to show up with content — which platforms matter most to you right now?
2. Are there formats you're drawn to — short posts, long articles, video, audio, email, something else?
3. How often do you realistically want to publish? Don't tell me the ideal — tell me what's actually sustainable for you.
4. Is there a platform you've avoided but feel like you should be on? What's been holding you back?
5. What resources do you have available — do you have someone helping with content, or is this all on you?

**Adaptive Follow-ups**
- If LinkedIn mentioned → *"Is this your personal profile, a company page, or both?"*
- If newsletter mentioned → *"What platform are you on — or planning to use? And how big is your list right now?"*
- If video mentioned → *"Do you have the capacity to film and edit, or would you need that handled for you?"*
- If podcast mentioned → *"How long are your episodes typically, and where do you publish them?"*
- If "I don't know where to start" → *"Based on what you've told me about your audience [reference Stage 3], they seem most active on [X]. Does that feel right to you?"*
- If multiple platforms named → *"If you had to pick just one to focus on first, which feels most natural or has the most traction already?"*

**Depth Check**
- Watch for: listing 5+ platforms without prioritisation
- Probe with: *"That's a solid list — but if we're being realistic about what's sustainable, which one or two should we treat as primary and build everything else around?"*
- Watch for: "I want to post every day" from someone who's never posted consistently
- Probe with: *"I want to make sure we set a pace you can actually maintain. What's the most you've consistently published in the past?"*

**"I Don't Know" Fallback**
If they're not sure which platform to focus on: *"Let's make it simple — where does your ideal client spend the most time online based on what you told me earlier? And where do you personally feel most comfortable showing up? Those two answers usually point to the right starting point."*

**Stage Complete When:**
- ≥ 1 primary platform confirmed ✓
- ≥ 1 format confirmed ✓
- Posting frequency confirmed for primary platform ✓
- Platform-specific operational notes captured where relevant (newsletter list size, video capacity, etc.) ✓

**Saves to:** `stages/06_platforms.json`

---

## Stage 7 — Competitors & References

**Goal:** Understand the competitive landscape — who they're up against, whose content they admire, and what they refuse to copy.

**Cross-Stage References:**
- Stage 1 industry and differentiator → frame competitor questions around where they fit in the market
- Stage 4 voice references → check if any were competitors (that's valuable signal)
- Stage 3 audience online hangouts → who else is showing up in those spaces?

**Core Questions**
1. Who are your main competitors — the people or businesses your ideal client might consider instead of you?
2. Of those competitors, whose content or marketing do you think is actually good? What are they doing well?
3. Is there anyone — inside or outside your industry — whose content you genuinely admire? What makes it stand out?
4. What do your competitors do that you refuse to do? What's off the table for you?
5. What's the gap in your market — what are your competitors not doing that you could own?

**Adaptive Follow-ups**
- If they can't name competitors → *"Think about it from your client's perspective — if they didn't come to you, where would they go or what would they do instead?"*
- If they name a big brand as competition → *"Are you competing head-to-head with them, or do you serve a niche they don't fully address?"*
- If content inspiration is someone personal and specific → *"What is it about how they communicate — is it the topics, the format, the tone, the consistency, something else?"*
- If "I don't have real competitors" → *"That's interesting — what does your client do if they choose not to work with you at all? Even 'do nothing' or 'DIY' counts as competition."*

**Depth Check**
- Watch for: "I don't really pay attention to competitors"
- Probe with: *"Fair enough — but think about it from your audience's perspective. What else is competing for their attention or their budget in this space?"*
- Watch for: vague inspiration references like "I like good content"
- Probe with: *"Give me a specific example — a post, a newsletter, a video, a brand. Something you saw recently that made you think 'I want to create something like that.'"*

**"I Don't Know" Fallback**
If they can't think of content they admire: *"Let's flip it — think about content you've saved, shared, or gone back to more than once. Doesn't have to be in your industry. What was it, and why did it stick with you?"*

**Stage Complete When:**
- ≥ 1 direct competitor named ✓
- ≥ 1 content inspiration named (inside or outside industry) ✓
- Something they refuse to copy or do ✓
- At least one differentiator relative to the competition ✓

**Saves to:** `stages/07_competitors.json`

---

## Stage 8 — Content Constraints

**Goal:** Define the guardrails — topics that are off-limits, legal or compliance requirements, sensitivities in the industry, and anything that's caused problems before.

**Cross-Stage References:**
- Stage 1 regulated industry → open this stage directly with compliance questions
- Stage 1 industry → some industries have implicit sensitivities (health claims, financial advice, legal disclaimers)
- Stage 2 offer objections → some constraints may be tied to how the offer is legally described

**Core Questions**
1. Are there any topics, angles, or statements that are completely off-limits for your content — things I should never write or say on your behalf?
2. Does your industry have any legal or compliance requirements that affect what you can publish? Things like disclaimers, regulated claims, or restricted language?
3. Has content ever caused a problem for your business — a complaint, a misunderstanding, or something that landed badly? What happened?
4. Are there any competitors, public figures, or situations you want to stay well away from mentioning?
5. Is there anything sensitive about your business or industry that I should be aware of before creating content?

**Adaptive Follow-ups**
- If finance/investment → *"Are there specific FCA, SEC, or other regulatory requirements around how you describe returns, performance, or advice?"*
- If healthcare/wellness → *"Are there health claims you need to avoid — anything around treatment, cure, or diagnosis language?"*
- If legal services → *"Do you need specific disclaimers on content — 'not legal advice' type language?"*
- If "no constraints" stated → *"Good to know. Just to confirm — are you comfortable with me referencing competitors, taking strong opinions, or using humour when appropriate?"*
- If past content problem mentioned → *"Tell me more — what happened, and what would you want to handle differently now?"*

**Depth Check**
- Watch for: "just keep it professional" as the only constraint
- Probe with: *"Understood — is there anything more specific? Any topics, claims, or tones that you want to make sure we never go near?"*
- Watch for: assuming no constraints in clearly regulated industries
- Probe with: *"Given that you're in [industry], are there any standard disclaimers or restricted phrases I should know about?"*

**"I Don't Know" Fallback**
If they're unsure about constraints: *"That's okay — let me ask it differently. Imagine a piece of content went out under your name that caused a problem. What's the scenario you'd be most concerned about? Even hypothetically, that tells us a lot about what to be careful with."*

**Stage Complete When:**
- Off-limits topics acknowledged (even if empty list is confirmed explicitly) ✓
- Compliance requirements noted or confirmed as N/A ✓
- Stage not skipped — client has explicitly engaged with the questions ✓
- `explicitly_confirmed_no_constraints: true` set if they confirmed no restrictions ✓

**Saves to:** `stages/08_constraints.json`

---

## Stage 9 — Approval Workflow

**Goal:** Understand how the working relationship operates — who reviews content, how many rounds of revision are expected, what good feedback looks like, and who makes the final call.

**Cross-Stage References:**
- Stage 1 team size → solo operators likely have a simpler workflow; larger teams may have multiple reviewers
- Stage 5 timeline → tight timelines need faster turnaround expectations set upfront

**Core Questions**
1. When content is ready for review, who needs to see it — is that just you, or are other people involved?
2. Who has the final say on whether something gets published?
3. How many rounds of revisions do you typically expect before something is approved?
4. What's a realistic turnaround time on your end when content comes in for review?
5. How do you prefer to give feedback — written comments in a document, a quick call, a voice note, or something else?

**Adaptive Follow-ups**
- If team involved → *"Is there a particular person who tends to be the bottleneck in approvals — someone whose sign-off is always the last step?"*
- If "just me" → *"Good — and how do you prefer content delivered to you for review? Google Doc, email, Notion, something else?"*
- If multiple revision rounds expected → *"What tends to drive most of the revisions — tone, factual accuracy, strategic direction, something else?"*
- If tight turnaround mentioned → *"And on our side, how quickly do you need content delivered — is there a standard lead time that works for you?"*

**Depth Check**
- Watch for: "however long it takes" as a turnaround time
- Probe with: *"I want to make sure we plan around your schedule. Is there a window that usually works — a day or two, a few days, a week?"*
- Watch for: "it's fine, just send it" as feedback style
- Probe with: *"What does good feedback look like for you — do you prefer to mark up a document, hop on a quick call, or give notes another way?"*

**"I Don't Know" Fallback**
If they haven't thought about workflow: *"That's okay — we can keep it simple. The key thing is: who's the one person whose approval means content can go live? And roughly how long do you need to review something before that decision gets made?"*

**Stage Complete When:**
- Primary reviewer named ✓
- Final approver named ✓
- Revision rounds acknowledged (even "1 round max" or "as needed" is valid) ✓
- Turnaround time acknowledged ✓
- Feedback format or delivery preference noted ✓

**Saves to:** `stages/09_workflow.json`

---

## Stage 10 — Final Profile

**This is not an interview stage. It is a compilation and validation step.**

Follow the instructions in `onboarding_agent.md` Sections H and I exactly:

1. Run the Validation Layer (Section H)
2. Fill any remaining required field gaps with targeted follow-up questions
3. Merge all 9 stage files into `profile.json`
4. Calculate the Client Readiness Score
5. Write `brief.md` in plain English
6. Confirm completion to the user with the readiness score and next steps

The brief structure:
```
# [Client Name] — Client Brief
**Date completed:** [date]
**Readiness Score:** [High / Medium / Low]

## About the Business
[Plain English summary from Stage 1]

## What They Offer
[Plain English summary from Stage 2]

## Their Audience
[Plain English summary from Stage 3]

## Their Brand Voice
[Plain English summary from Stage 4]

## Content Goals
[Plain English summary from Stage 5]

## Platforms & Formats
[Plain English summary from Stage 6]

## Competitive Landscape
[Plain English summary from Stage 7]

## Content Constraints
[Plain English summary from Stage 8]

## Approval & Workflow
[Plain English summary from Stage 9]

## Readiness Score
**[High / Medium / Low] — [N]/100**

[Plain-English explanation of the score. What it means. What (if anything) should happen before content creation begins.]

[If Medium or Low: list the specific areas that need more depth, in plain language.]
```
