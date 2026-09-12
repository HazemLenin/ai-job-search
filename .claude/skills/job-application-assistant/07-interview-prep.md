---
framework_version: 1.0.0
---

# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

<!-- These are populated by /setup from your actual experience. Below are templates showing the format. -->

### 1. [PROJECT_NAME] ([SKILL_DEMONSTRATED])
**S:** [CONTEXT - what was happening, what was the problem]
**T:** [YOUR RESPONSIBILITY - what you specifically needed to do]
**A:** [WHAT YOU DID - specific actions, tools, methods]
**R:** [OUTCOME - measurable results, adoption, impact]
**Use for:** "[QUESTION_TYPE_1]", "[QUESTION_TYPE_2]"

### 2. [PROJECT_NAME] ([SKILL_DEMONSTRATED])
**S:** [CONTEXT]
**T:** [YOUR RESPONSIBILITY]
**A:** [WHAT YOU DID]
**R:** [OUTCOME]
**Use for:** "[QUESTION_TYPE_1]", "[QUESTION_TYPE_2]"

### 3. [PROJECT_NAME] ([SKILL_DEMONSTRATED])
**S:** [CONTEXT]
**T:** [YOUR RESPONSIBILITY]
**A:** [WHAT YOU DID]
**R:** [OUTCOME]
**Use for:** "[QUESTION_TYPE_1]", "[QUESTION_TYPE_2]"

<!-- Add more STAR examples as needed. Aim for 4-6 covering different competencies. -->

## STAR Candidates (Complete Manually)

### Calendar API redesign (~70% load-time cut)
**Source:** CV / LinkedIn - Software Engineer, GAMP
**What happened:** Redesigned a calendar API and optimized DB queries, cutting load time by ~70%.
**Why it matters:** Performance optimization, measurable impact, "tell me about a technical improvement you drove."
**S/T/A/R stub:**
- Situation: The calendar view in GapMap (used daily by clients in Poland to manage market-stand bookings) was slow to load, causing visible friction for users checking availability.
- Task: As owner of the module, I needed to diagnose and fix the slowdown without disrupting the live booking flow.
- Action: [Fill in: what you found when profiling - e.g. inefficient queries, missing indexes, over-fetching] and redesigned the API's data-access pattern and optimized the underlying SQL Server queries accordingly.
- Result: Cut load time by ~70%, directly improving the daily experience for enterprise clients depending on the module.

### EF Core migration consolidation (~40% faster builds)
**Source:** CV / LinkedIn - Software Engineer, GAMP
**What happened:** Consolidated 280+ EF Core migration files into one, speeding up local builds by ~40%.
**Why it matters:** Initiative, developer-experience tooling, "describe a time you improved a process nobody asked you to."
**S/T/A/R stub:**
- Situation: After two-plus years of active development, GapMap's MSSQL database had accumulated 280+ individual EF Core migration files, which slowed down every local build and onboarding for the whole engineering team - nobody had asked me to fix this, I noticed it as friction.
- Task: On my own initiative, I set out to consolidate the migration history without breaking existing environments or losing schema history.
- Action: Squashed the 280+ migrations into a single consolidated migration, validating it against existing databases so current environments stayed in sync.
- Result: Local builds got ~40% faster, benefiting every engineer on the team, not just me - the kind of system-level improvement my GAMP reference letter specifically calls out.

### Nx monorepo restructure (co-led, 2 months)
**Source:** CV / LinkedIn - Software Engineer, GAMP
**What happened:** Co-led a 2-month restructure consolidating two large Angular apps into a shared component library.
**Why it matters:** Technical leadership, collaboration, large refactor risk management.
**S/T/A/R stub:**
- Situation: GapMap and eZRRT had grown into two large, separately-maintained Angular applications (5 modules total) with duplicated components and inconsistent patterns, making shared changes slow and error-prone.
- Task: I co-led the effort to restructure both into a single Nx monorepo with a shared component library, without stopping feature work on either app.
- Action: Worked with a co-lead to plan the migration in stages, extracting shared UI into a common library and migrating each module incrementally over roughly 2 months, coordinating with the rest of the team to avoid merge conflicts and regressions.
- Result: Both apps now share one component library inside a single Nx monorepo, cutting duplication and making cross-app changes faster to ship - and I set up Playwright e2e testing alongside it to keep the migration safe.

### Solo ownership of mobile project (GapMap + eZRRT)
**Source:** CV / LinkedIn - Software Engineer, GAMP
**What happened:** Solely owned two Capacitor+Angular mobile apps with FCM, Fastlane CI/CD, and Google Play/App Store releases.
**Why it matters:** Autonomy, end-to-end delivery, "tell me about something you owned alone."
**S/T/A/R stub:**
- Situation: GAMP needed native mobile apps for both GapMap and eZRRT, but there was no dedicated mobile team - the work needed an owner.
- Task: I took sole ownership of both mobile apps end-to-end: build (Capacitor + Angular + Trapeze for multi-app native config), push notifications (FCM), CI/CD, and store releases.
- Action: Built out the Fastlane CI/CD pipeline for both apps and automated the release publish step so an approved build reaches users automatically after store review, instead of waiting on someone to notice and click "publish."
- Result: Both apps ship reliably to Google Play and the App Store with no manual bottleneck, run solely by me alongside my other Contractors-module work.

### Mentoring + knowledge-sharing + competency matrix
**Source:** CV / LinkedIn - Software Engineer, GAMP
**What happened:** Mentored 3 junior developers, delivered company-wide KS session recognized as best, co-authored engineering competency matrix.
**Why it matters:** Leadership, culture contribution, "how do you help others grow?"
**S/T/A/R stub:**
- Situation: As GAMP grew, junior developers needed structured support, and the team lacked a shared, explicit standard for what "senior" or "mid-level" competency actually looked like.
- Task: Beyond my own module work, I mentored 3 junior developers and conducted technical interviews, and co-authored the company's engineering competency matrix to make growth expectations explicit.
- Action: Ran regular mentoring and code-review sessions with the juniors, and worked with colleagues to define and document the competency matrix; also prepared and delivered a company-wide knowledge-sharing session, following on from an earlier developer-productivity talk.
- Result: My KS session was recognized as the best at the company; the competency matrix gave the team a shared, explicit growth framework instead of an implicit one.

### Vehicle-access hardware integration (LPR cameras, gate barriers, fiscal devices)
**Source:** Reference letter - COO, GAMP
**What happened:** Worked across GapMap's vehicle traffic control system, integrating LPR (license plate recognition) cameras, gate barriers, payment terminals, and fiscal devices for an agricultural trade market platform - business-critical infrastructure where a failure means lost revenue at the gate.
**Why it matters:** Hardware/IoT integration under real-world constraints, reliability engineering, "tell me about integrating with physical/external systems."
**S/T/A/R stub:**
- Situation: GapMap controls physical vehicle access to agricultural trade markets - real customers and real revenue depend on gate barriers, LPR cameras, and fiscal devices working correctly in dusty, high-traffic, on-site conditions.
- Task: I worked on integrating and maintaining this hardware layer (including the Pay-Station kiosk module) alongside the software stack, together with two colleagues, so vehicle entry/exit and on-site payment stayed reliable.
- Action: [Fill in: a specific integration you built or a failure mode you handled - e.g. handling LPR misreads, retry logic for payment terminal timeouts, or fiscal-device error recovery], applying the same discipline as pure software work but accounting for real-world hardware unreliability (dust, weather, constant use).
- Result: The kiosk/gate system kept processing real customer payments reliably on-site - a failure here means lost revenue at the gate, so the integration held up under production conditions.

### MFA implementation from scratch (Identity Server)
**Source:** CV / LinkedIn - Software Engineer, GAMP
**What happened:** Designed and shipped MFA with Identity Server and recovery codes.
**Why it matters:** Security awareness, complex feature delivery, "walk me through a technically challenging feature."
**S/T/A/R stub:**
- Situation: GapMap handled sensitive B2B account access and payments but had no multi-factor authentication layer, a gap for a platform enterprise clients depend on daily.
- Task: I was responsible for designing and shipping MFA end-to-end, including a safe account-recovery path.
- Action: Built MFA using Identity Server, including recovery codes so users weren't permanently locked out if they lost their second factor, and integrated it across the existing auth flow without disrupting current users.
- Result: GapMap gained a production MFA flow built from scratch, strengthening account security for enterprise clients.

### Fastlane release automation (removed manual publish step)
**Source:** Reference letter - COO, GAMP
**What happened:** Automated mobile releases with Fastlane, eliminating the manual publish step after store review - approved builds now reach users automatically instead of waiting on someone to notice and click "publish".
**Why it matters:** Process improvement, initiative beyond the ticket, "describe a time you removed friction from a process."
**S/T/A/R stub:**
- Situation: After store review approved a new mobile build, someone still had to notice and manually click "publish" before it reached users - an easy-to-forget manual step that delayed fixes and features reaching customers.
- Task: As sole owner of the mobile apps, I wanted releases to reach users as soon as they were approved, without relying on someone remembering a manual step.
- Action: Extended the existing Fastlane CI/CD pipeline to automate the publish step after store approval, removing the manual click entirely.
- Result: Approved builds now reach users automatically the moment they clear store review, instead of waiting on manual action - my reference letter calls this out directly as a habit of noticing friction and removing it for everyone, not just myself.

### Merge Polisher presented at internal Knowledge-Sharing session
**Source:** Reference letter - COO, GAMP
**What happened:** Built and open-sourced Merge Polisher on own initiative, then presented it at an internal KS session, following an earlier talk on developer productivity ("How to Work Smarter").
**Why it matters:** Initiative, developer tooling, public speaking/influence, "tell me about a time you influenced practices beyond your own work."
**S/T/A/R stub:**
- Situation: I'd noticed merge/pull request descriptions across the team (and in my own work) were often thin, making code review slower and less informed - a friction point nobody had assigned me to fix.
- Task: On my own initiative, following an earlier internal talk I gave on developer productivity ("How to Work Smarter"), I wanted to build something that actually raised MR/PR quality team-wide.
- Action: Built and open-sourced Merge Polisher - an AI-powered CI tool (Python, layered architecture, Gemini API, retry/fallback LLM handling, Docker deployment) that automatically polishes MR/PR descriptions, posts inline code review suggestions, and generates a confidence score based on critical-path coverage - then presented it at an internal Knowledge-Sharing session.
- Result: Raised merge request quality across the entire team, making code review faster and better for both human reviewers and GAMP's AI-assisted review tooling - a multiplier effect beyond my own work, per my reference letter.

### Earned senior-level trust as youngest engineer on the team
**Source:** Reference letter - COO, GAMP
**What happened:** Was the youngest engineer on the GAMP team, yet within months was trusted with work typically given to senior developers, including production systems clients depend on daily.
**Why it matters:** Fast ramp-up, trust-building, "tell me about a time you had to prove yourself quickly."
**S/T/A/R stub:**
- Situation: I joined GAMP as the youngest engineer on the team, working on GapMap, business-critical infrastructure that real clients in Poland depend on every day.
- Task: I needed to earn the team's trust quickly enough to be handed real ownership, not just supervised tasks, despite being the least experienced person on the team by tenure.
- Action: Took full ownership of the Contractors module end-to-end (API design through UI), communicated daily and clearly with Polish stakeholders in English, and consistently shipped beyond what was assigned - the migration consolidation, Fastlane automation, and Merge Polisher all happened on my own initiative during this period.
- Result: Within months I was trusted with work typically given to senior developers, including production systems clients depend on daily - confirmed directly in my GAMP reference letter from the COO.
- Result:

## Common Tough Questions

### "Why did you leave [previous company]?"
> [PREPARE YOUR ANSWER - be honest, forward-looking, no negativity about former employer]

### "You don't have [specific skill/experience]."
> [PREPARE YOUR ANSWER - acknowledge the gap, bridge to adjacent experience, show willingness to learn]

### "Where do you see yourself in 5 years?"
> [PREPARE YOUR ANSWER - show ambition aligned with the role's growth path]

### "What's your biggest weakness?"
> [PREPARE YOUR ANSWER - genuine weakness with concrete mitigation strategy]

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
