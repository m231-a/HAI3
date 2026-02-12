# GitHub Issues to Create - From Adopters Feedback

**Meeting Date:** February 12, 2026
**Purpose:** Structured list of issues to create in HAI3 repository

---

## Priority 0 - Critical Blockers

### Issue #1: [P0] Establish Stable Development Roadmap

**Title:** [P0] Establish stable roadmap with milestones and commit to stability periods

**Labels:** `P0`, `process`, `roadmap`, `blocker`

**Description:**
Adopters report breaking changes expected "almost daily" making it impossible to commit to HAI3 long-term. Teams need trust that their work won't be obsolete next week.

**Problem:**
- No clear, stable roadmap
- Breaking changes happening daily
- Hard for developers to commit to HAI3
- Creates uncertainty and prevents long-term planning
- Core team acknowledges "basic version not ready yet"

**Impact:**
- Prevents adoption by risk-averse teams
- Blocks long-term planning
- Reduces developer confidence
- Teams stuck on old versions to avoid churn

**Requested Solution:**
1. Publish concrete roadmap with version milestones and dates
2. Commit to stability periods (minimum 2-4 weeks between breaking changes)
3. Clearly communicate breaking change policy
4. Define what "stable" and "ready" means

**Quotes:**
> "Development of HAI3 is somewhat chaotically, with lack of clear, stable roadmap. As developers, it's very hard to commit to HAI3 because we anticipate breaking changes almost daily." - Leonid

> "Builders must trust what they build today won't be obsolete next week." - Leonid

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Leonid Romanov (Analytics), Guillermo Gil (CyberApp)
**Affects:** All teams using or considering HAI3

---

### Issue #2: [P0] Improve AI-generated code success rate (currently 40%)

**Title:** [P0] Investigate and improve AI-generated code success rate from 40% to 70%+

**Labels:** `P0`, `ai-integration`, `developer-experience`, `blocker`

**Description:**
Only 40% of AI-generated code works initially. Remaining 60% requires manual fixes or multiple iterations, defeating the purpose of AI assistance.

**Problem:**
- Initial success rate: 40%
- Remaining 60% requires:
  - Manual fixes
  - Multiple prompt iterations (2-3 instead of 1)
  - Falling back to plain AI without HAI3 benefits
- Defeats purpose of using specs and company workflows

**Impact:**
- Wastes developer time on fixes
- Reduces value proposition of HAI3
- Teams fall back to plain AI prompts
- Loses benefits of HAI3 specs and workflows

**Requested Solution:**
1. Analyze root causes of failures
2. Audit rules for complexity and conflicts
3. Measure context size being sent to AI
4. Simplify where possible without losing benefits
5. Target: 70%+ initial success rate

**Related Issues:**
- Context overload (too many rules)
- Over-restrictive constraints
- Rule conflicts

**Quotes:**
> "We get only about 40% success rate initially, and then we need to fix. Remaining part requires manual fixes, and maybe falling back to simple AI problems without benefits of using our specs and company workflows." - Leonid

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Leonid Romanov, Guillermo Gil
**Success Metric:** Track success rate improvement over time

---

### Issue #3: [P0] Create documentation: "When to use Screen Sets"

**Title:** [P0][Docs] When to use Screen Sets vs not - decision guide with examples

**Labels:** `P0`, `documentation`, `blocker`, `screen-sets`

**Description:**
Multiple teams confused about when to use screen sets, when HAI3 Studio is needed, and what patterns are appropriate for different application types.

**Problem:**
- Early confusion about screen set usage
- Unclear when to use vs not use screen sets
- Unclear when HAI3 Studio is needed vs optional
- For monolithic CyberApp apps, extra UI elements weren't needed
- No examples of appropriate use cases

**Impact:**
- Teams can't make informed architectural decisions
- Wrong patterns chosen for use cases
- Wasted effort on inappropriate features
- Blocks effective usage

**Requested Solution:**
Create guide covering:
1. What are screen sets? (clear definition)
2. When to use screen sets (with criteria)
3. When NOT to use screen sets
4. When HAI3 Studio is appropriate vs not
5. Real examples from Analytics (uses screen sets) and CyberApp (different pattern)
6. Decision tree/flowchart

**Examples to Include:**
- Analytics: 2 screen sets (Dashboard, Reports) with multiple screens each - GOOD use case
- CyberApp Chat: Monolithic app, didn't need screen sets initially - GOOD decision
- Different patterns and when each is appropriate

**Quotes:**
> "In early stages of working with analytics, we had questions about screen sets. We did not understand how to properly work with them because in our case, we worked more on terms of a chronic CyberApp application and we did not need these extra UI elements." - Roman

> "We definitely need more examples on how to properly work with entities that HAI3 names like screen set, screen, and what exactly we should create as a screen set, or in which cases we don't need HAI3 Studio." - Roman

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Roman Shumsky (Analytics)
**Owner:** Leonid (coordination) + Core team (writing)
**Due:** 2 weeks

---

### Issue #4: [P0] Audit and simplify AI context/rules to prevent overload

**Title:** [P0] AI context overload - audit rules for necessity and simplify

**Labels:** `P0`, `ai-integration`, `rules`, `blocker`

**Description:**
Too many rules and constraints cause AI to get "crazy" and not follow all guidelines. Success rate suffering due to context overload.

**Problem:**
- AI receives too many rules/constraints
- Can't follow all rules simultaneously
- Gets confused and makes unexpected decisions
- Success rate only 40% due partly to this
- Rules are overly restrictive in some areas

**Impact:**
- AI doesn't follow rules (too many to process)
- Inconsistent results
- Requires 2-3 prompts instead of 1
- Manual fixes needed
- Defeats purpose of structured approach

**Requested Solution:**
1. Audit all rules/guidelines for necessity
2. Measure total context size sent to AI
3. Identify redundant or conflicting rules
4. Simplify where possible
5. Prioritize essential rules only
6. Consider phased/progressive rule application
7. Balance guidance vs overwhelming AI

**Examples of Over-Restriction:**
- API layer fixed content-type (JSON only) - see related issue
- Architecture rules that conflict
- Too many constraints at once

**Quotes:**
> "My main concern about HAI3 is how bloated the context is when you are using the AI to build something." - Guillermo

> "Sometimes I felt like the AI was just not following the rules because we had too many of them. We could achieve the same result in a more simple way, probably." - Guillermo

> "At some point, the AI just went crazy. Maybe instead of a single prompt, I needed two or three or even do some manual fixes." - Guillermo

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Guillermo Gil (CyberApp)
**Related:** Issue #2 (success rate)

---

## Priority 1 - Major Issues

### Issue #5: [P1] Make API layer content-type configurable (not JSON-only)

**Title:** [P1] API layer too restrictive - support configurable content-types

**Labels:** `P1`, `api-layer`, `enhancement`, `flexibility`

**Description:**
API layer currently uses fixed content-type (JSON only), forcing developers to break architecture rules for common scenarios like CSV uploads.

**Problem:**
- Default HAI3 REST protocol instance has fixed content-type
- Only allows JSON
- Can't send CSV files, multipart/form-data, etc.
- Forces creating new protocol instances (breaks architecture)
- Over-restrictive for real-world use cases

**Impact:**
- Developers break architecture rules to accomplish requirements
- Workarounds needed for common scenarios
- Reduces trust in HAI3 guidance
- "Sometimes we are constraining too much"

**Requested Solution:**
- Make content-type configurable per endpoint
- Support common scenarios out-of-box:
  - application/json (current)
  - text/csv
  - multipart/form-data
  - application/x-www-form-urlencoded
- Don't force workarounds for standard HTTP scenarios
- Document how to configure

**Real Use Case:**
- CyberApp needed to send CSV files
- Had to create new REST protocol instance
- Felt like breaking rules, but no other way

**Quotes:**
> "The main issue I found is that, again, it is too restrictive. I had a requirement where I had to send CSV files and I had to change the content type of my request. But it was impossible... I had to create a new instance of the HTTP protocol." - Guillermo

> "The default instance of HAI3 was using a fixed content type which only allowed to send JSON. Sometimes we are constraining too much." - Guillermo

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Guillermo Gil (CyberApp)
**Priority:** P1 (blocks real use cases)
**Quick Win:** Yes (configuration option)

---

### Issue #6: [P1] Create migration guide for version upgrades

**Title:** [P1][Docs] Create migration guide for upgrading HAI3 versions

**Labels:** `P1`, `documentation`, `migration`, `developer-experience`

**Description:**
Unclear how to migrate between HAI3 versions, blocking teams from upgrading and getting bug fixes.

**Problem:**
- Not clear how to migrate to new HAI3 versions
- Requires deep knowledge of architecture changes
- Complicated further with external UI kits
- Per-package versioning adds confusion
- No documented breaking changes
- Teams stuck on old versions

**Impact:**
- Teams stuck on outdated versions
- Can't get bug fixes or improvements
- Can't answer "which version are we using?"
- Fear of upgrade prevents trying new features

**Requested Solution:**
Create guide covering:
1. Version numbering explanation
2. How to identify current versions (per-package)
3. Breaking changes documentation (per version)
4. Step-by-step migration instructions
5. Special considerations (UI kits, external libraries)
6. Migration checklist
7. Consider: Automated migration tooling

**Quotes:**
> "It's not really clear how to migrate to new versions of HAI3. You need some knowledge on how to migrate everything, because sometimes not only the architecture, but if you are also using external UI kits, the thing is even more complicated." - Guillermo

> "Since we have a different version for each package, well, it's not really easy to say which version I am using right now." - Guillermo

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Guillermo Gil (CyberApp)
**Related:** Issue #1 (stability/breaking changes)

---

### Issue #7: [P1] Separate demo/example code from production patterns

**Title:** [P1] Separate demo code from production patterns to reduce confusion

**Labels:** `P1`, `documentation`, `repository-cleanup`, `developer-experience`

**Description:**
Repository contains demonstration code and patterns not used in real development, creating confusion about what's production-ready.

**Problem:**
- Example/demo code mixed with production patterns
- Hard to distinguish demos from real usage
- Creates confusion: "Is this production-ready?"
- Developers unsure what to follow
- Some patterns are for illustration only

**Impact:**
- Teams follow inappropriate patterns
- Confusion about best practices
- Reduced trust in documentation
- Time wasted on wrong approaches

**Requested Solution:**
1. Audit repository for demo vs production code
2. Clearly mark/label demonstration code
3. Move demos to separate directory or repo
4. Document what's production-ready vs educational
5. Consider "examples" vs "templates" distinction

**Quotes:**
> "Repository contains a lot of example codes or patterns that we actually don't use in real development, and this creates some confusion in what is production ready and just demonstration material." - Leonid

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Leonid Romanov
**Quick Win:** Yes (marking/labeling)

---

### Issue #8: [P1] Add ESLint rule to catch missing internationalization

**Title:** [P1] ESLint doesn't catch hardcoded strings - add i18n enforcement rule

**Labels:** `P1`, `eslint`, `i18n`, `developer-experience`

**Description:**
AI sometimes creates components with hardcoded text instead of using localization. Current ESLint rules don't catch this violation.

**Problem:**
- AI creates components without i18n
- Hardcoded text in components
- ESLint doesn't catch violation
- Current CyberApp has screens missing localization
- Discovered only in manual review

**Impact:**
- Localization violations slip through
- Manual effort to find and fix
- Production code with hardcoded strings
- Reduces benefits of i18n system

**Requested Solution:**
- Add ESLint rule to detect hardcoded strings in components
- Enforce use of translation functions
- Make configurable (some strings OK to hardcode)
- Add to default HAI3 ESLint config

**Context:**
- Internationalization is a SUCCESS STORY (universally praised)
- But AI sometimes forgets to use it
- Need automated enforcement

**Quotes:**
> "Sometimes I saw the AI not using localization, for example, which is something that it's a current problem in CyberApp. There are some screens and components that are not using localization." - Guillermo

> "Internalization issues I found were not caught. I'm using like fixed text in the components." - Guillermo

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Guillermo Gil (CyberApp)
**Related:** i18n feature (success story)

---

### Issue #9: [P1] Document architecture for human understanding

**Title:** [P1][Docs] Create architecture documentation for human developers (not just AI)

**Labels:** `P1`, `documentation`, `architecture`, `developer-experience`

**Description:**
When relying on AI to generate code, architecture is not clear to developers who need to debug or modify the generated code.

**Problem:**
- Architecture documentation optimized for AI consumption
- Human developers can't understand generated code structure
- Hard to debug AI-generated code
- Manual fixes difficult when architecture unclear
- Frontend/backend boundaries undefined

**Impact:**
- Developers can't effectively work with AI-generated code
- Debugging difficult
- Manual fixes take longer
- Can't make informed architectural decisions

**Requested Solution:**
Create human-readable documentation covering:
1. Overall architecture principles
2. Package structure and responsibilities
3. Frontend/backend separation and contracts
4. How components communicate
5. State management approach
6. Routing and navigation
7. Event flow
8. Integration with Cyber Fabric workflows
9. Diagrams and visual aids

**Quotes:**
> "The architecture was not even clear to me. I just told AI to create everything and now when I had to go and look into it, it was not like something I could just understand from the beginning." - Guillermo

> "We have problems with contracts and conventions between different development players like frontend and backend." - Leonid

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Guillermo Gil, Leonid Romanov

---

### Issue #10: [P1] Fix CLI initialization reliability across versions

**Title:** [P1] CLI initialization fails in some versions - ensure reliability

**Labels:** `P1`, `cli`, `bug`, `developer-experience`

**Description:**
Multiple attempts to initialize projects with different versions resulted in CLI failures. After fixes, initialization worked, but reliability is concerning.

**Problem:**
- CLI tool didn't work properly in some 0.2 alpha versions
- Initialization failed
- Required "small fixes" to start working
- Inconsistent across versions
- Most problems during project initialization phase

**Impact:**
- First impression is broken
- Blocks new project setup
- Wastes time troubleshooting
- Reduces confidence in tooling

**Requested Solution:**
1. Ensure CLI works reliably across all published versions
2. Add automated tests for initialization
3. Validate before publishing new versions
4. Document known issues and workarounds if any

**Quotes:**
> "A couple of times, CLI tool didn't work properly and initialised application didn't work, but after some small fixes, it started." - Roman

> "In analytics, in the early stages... the most problem was with initialization of the project." - Roman

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Roman Shumsky (Analytics)
**Versions affected:** 0.2 alpha series

---

## Priority 2 - Improvements

### Issue #11: [P2] AI ignores UI kit rules when given extra context

**Title:** [P2] AI creates custom components instead of using UI kit when given Figma/screenshots

**Labels:** `P2`, `ai-integration`, `ui-kit`, `bug`

**Description:**
Even with strict rules to use specific UI library, AI improvises custom components when extra context is provided (Figma designs, screenshots, MCP server data).

**Problem:**
- Rules specify: use Chat Xian UI kit
- When Figma/screenshots added to context, AI ignores rules
- Creates custom components from scratch
- Happens even with "quite strict" rules

**Impact:**
- Inconsistent UI components
- Custom code instead of reusable components
- Defeats purpose of UI kit
- More code to maintain

**Requested Solution:**
1. Investigate why extra context overrides UI kit rules
2. Strengthen UI kit enforcement in prompts
3. Consider separate phase: match design to existing components first
4. Document workaround if unfixable

**Quotes:**
> "Even though the rules are quite strict, sometimes... if you have too much context or you provide some info from the MCP server, imagine Figma or even a screenshot, the AI will improvise the component. It will create a custom component, even though you are telling through the rules that use that specific library." - David

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** David Alcala (Analytics)

---

### Issue #12: [P2] Document Event Handlers (low discoverability)

**Title:** [P2][Docs] Document Event Handlers - developers don't know they exist

**Labels:** `P2`, `documentation`, `events`, `discoverability`

**Description:**
Event handlers exist but developers aren't aware of them. Low discoverability of features.

**Problem:**
- Event handlers not documented or promoted
- Developers don't know they exist
- Features hidden or under-documented

**Impact:**
- Useful features not used
- Developers implement workarounds
- Value of HAI3 not fully realized

**Requested Solution:**
1. Document event handlers and use cases
2. Clarify EventBus vs Redux patterns
3. Provide examples of cross-screen set communication
4. Improve feature discoverability overall
5. Consider features index/catalog

**Quotes:**
> "Event handlers was something new. I didn't know that they existed." - Roman

**Source:** Adopters feedback meeting Feb 12, 2026
**Reported by:** Roman Shumsky (Analytics)

---

### Issue #13: [P2] Create AI agent skills from HAI3 workflows

**Title:** [P2][Feature Request] Convert HAI3 workflows into AI agent skills format

**Labels:** `P2`, `enhancement`, `ai-integration`, `feature-request`

**Description:**
Suggestion to make HAI3 workflows more convenient for AI agents by converting to skills format.

**Problem:**
- Current workflows not optimized for AI agent consumption
- Could be more convenient as skills

**Requested Solution:**
- Convert HAI3 workflows into AI agent skills
- Make workflows callable as skills
- More convenient API for AI agents

**Quotes:**
> "Maybe one of the questions or suggestion is to enrich HAI3 with some skills for AI agents. Convert some workflows that we have in HAI3 into skills that will be more convenient to AI agent to use." - Roman

**Source:** Adopters feedback meeting Feb 12, 2026
**Suggested by:** Roman Shumsky (Analytics)
**Status:** Proposal, needs scoping

---

## Process Improvements

### Issue #14: [Process] Involve adopters in design discussions earlier and more often

**Title:** [Process] Include practicing developers in design discussions earlier

**Labels:** `process`, `feedback`, `collaboration`

**Description:**
Request to involve real adopters in design discussions before implementation to catch practical issues early.

**Problem:**
- Design decisions made without adopter input
- Practical issues discovered late (after implementation)
- Becomes technical debt

**Impact:**
- Rework needed
- Features don't match real needs
- Adopters feel disconnected from roadmap

**Requested Solution:**
- Include practicing developers in design discussions
- Involve earlier in process (before implementation)
- More frequent involvement
- "We are the ones who will live with these decisions daily"

**Quotes:**
> "Involve practicing developers and adopters in design discussions earlier and more often. We are the ones who will live with these decisions daily and we can identify practical issues before they become technical depth [debt]." - Leonid

**Source:** Adopters feedback meeting Feb 12, 2026
**Suggested by:** Leonid Romanov
**Adoption:** Feedback sessions now established (first success)

---

### Issue #15: [Process] Organize master class led by real adopters

**Title:** [Process] Master class on HAI3 usage led by real adopters (not core team)

**Labels:** `process`, `documentation`, `training`, `knowledge-sharing`

**Description:**
Request for training session on HAI3 usage, but led by real adopters sharing practical experience rather than core team.

**Rationale:**
- Real-world usage patterns more valuable than theory
- Adopters know practical pain points and workarounds
- More relatable than core team perspective

**Proposed Content:**
- How we actually use HAI3 (Analytics and CyberApp)
- Explanation of modules and concepts
- Real-world patterns and workarounds
- Lessons learned
- What works, what doesn't

**Proposed Presenters:**
- Roman Shumsky (Analytics team)
- Guillermo Gil (CyberApp team)

**Quotes:**
> "Maybe one of the questions or suggestion is to... have a master class how to use the HAI3 better, like with explanation of the modules or something like that." - Roman

> "This will be best, actually, if not German as part of the core team... but actually someone who uses it, right?" - Pavel

**Source:** Adopters feedback meeting Feb 12, 2026
**Suggested by:** Roman Shumsky, endorsed by Pavel Kozemirov
**Status:** To be scheduled
**Timeline:** Next month (after docs improvements)

---

## Issue Creation Checklist

For each issue above:
- [ ] Create in HAI3 repository
- [ ] Apply appropriate labels
- [ ] Set priority
- [ ] Assign owner (if known)
- [ ] Link related issues
- [ ] Reference meeting notes
- [ ] Add to project board/milestone
- [ ] Notify relevant stakeholders

---

## Issue Dependencies

**Must be done first:**
1. Issue #1 (Roadmap) - Establishes foundation
2. Issue #3 (Screen Sets docs) - Unblocks teams
3. Issue #7 (Separate demo code) - Reduces confusion

**Can be parallel:**
- Issue #4 (Rule audit) + Issue #2 (Success rate)
- Issue #5 (API flexibility) - Independent
- Issue #6 (Migration guide) - Independent
- Issue #8 (ESLint i18n) - Independent

**Should wait for others:**
- Issue #15 (Master class) - Wait for docs improvements
- Issue #13 (AI skills) - Needs design/scoping first

---

## Labels to Use

**Priority:**
- `P0` - Critical blocker
- `P1` - Major issue
- `P2` - Improvement

**Type:**
- `bug` - Something broken
- `enhancement` - Improvement to existing
- `feature-request` - New capability
- `documentation` - Docs needed
- `process` - How we work

**Area:**
- `ai-integration` - AI behavior/rules
- `cli` - CLI tooling
- `api-layer` - Backend integration
- `ui-kit` - Components/styling
- `architecture` - Structure/design
- `developer-experience` - DX improvements
- `screen-sets` - Screen set functionality
- `i18n` - Internationalization
- `eslint` - Linting rules

**Status:**
- `blocker` - Blocks adoption/usage
- `quick-win` - Can deliver in 1-2 weeks

---

**Created by:** Leonid Romanov
**Date:** February 12, 2026
**Source:** Adopters feedback meeting transcript
**Total Issues:** 15 (6 P0, 6 P1, 2 P2, 1 Process)
