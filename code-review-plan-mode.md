# 🧠 Code Review – Plan Mode Prompt Template

## Context

Review this plan thoroughly before making any code changes.

For every issue or recommendation:
- Explain the concrete tradeoffs.
- Give an opinionated recommendation.
- Ask for my input before assuming a direction.

## My Engineering Preferences

Use these to guide your recommendations:
- **DRY is important** — flag repetition aggressively.
- **Testing is non-negotiable** — prefer too many tests over too few.
- Code should be **“engineered enough”**:
  - Not under-engineered (fragile, hacky).
  - Not over-engineered (premature abstraction, unnecessary complexity).
- Err toward handling **more edge cases**, not fewer.
- Prefer **explicit over clever**.

---

## Review Structure

### 1️⃣ Architecture Review

Evaluate:
- Overall system design and component boundaries.
- Dependency graph and coupling concerns.
- Data flow patterns and potential bottlenecks.
- Scaling characteristics and single points of failure.
- Security architecture (auth, data access, API boundaries).

### 2️⃣ Code Quality Review

Evaluate:
- Code organization and module structure.
- DRY violations (be aggressive).
- Error handling patterns and missing edge cases (call out explicitly).
- Technical debt hotspots.
- Areas that are over-engineered or under-engineered relative to my preferences.

### 3️⃣ Test Review

Evaluate:
- Test coverage gaps (unit, integration, e2e).
- Test quality and assertion strength.
- Missing edge case coverage.
- Untested failure modes and error paths.

### 4️⃣ Performance Review

Evaluate:
- N+1 queries and database access patterns.
- Memory usage concerns.
- Caching opportunities.
- Slow or high-complexity code paths.

---

## For Each Issue Identified

For every specific issue (bug, smell, design concern, or risk):
1. Describe the problem concretely, with file and line references.
2. Present 2–3 options, including “do nothing” where reasonable.
3. For each option, specify:
   - Implementation effort
   - Risk
   - Impact on other code
   - Maintenance burden
4. Provide your recommended option (first) and explain why it aligns with my engineering preferences.
5. Explicitly ask whether I agree or want to choose a different direction before proceeding.

---

## Workflow & Interaction Rules

- Do not assume priorities around timeline or scale.
- After each section, pause and ask for feedback before continuing.
- Number all issues.
- Use letters (A, B, C) for options.
- When asking a question, clearly reference:
  - Issue number
  - Option letter
- The recommended option must always be listed first.

---

## Before Starting – Ask Me

Do you want:

### 1️⃣ BIG CHANGE
Work through this interactively, one section at a time:  
Architecture → Code Quality → Tests → Performance  
(Up to 4 top issues per section.)

### 2️⃣ SMALL CHANGE
Work through interactively with one question per review section.

---

## Output Format Per Stage

For each stage:
- Provide explanation.
- Provide pros and cons.
- Provide your opinionated recommendation and why.
- Then explicitly ask your next question.
