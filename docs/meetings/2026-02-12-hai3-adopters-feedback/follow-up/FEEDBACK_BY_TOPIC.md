# HAI3 Adopters Feedback - Organized by Topic

**Meeting Date:** February 12, 2026
**Purpose:** Quick reference for feedback organized by HAI3 feature areas

---

## TOPIC 1: Architecture & Packages

### What is it?
- Frontend layer for Cyber Fabric platform
- Micro-frontend building blocks (routes, pages, screens, forms, components)
- NOT a framework - ecosystem of tools, scripts, workflows, AI solutions

### Why we use it?
- Increase development speed
- Improve application quality
- Unified approach integrating human expertise with AI workflows

### What works well ✅

1. **Validation & Linting**
   - CLI validate commands work fine (Roman)
   - Guarantee project structure compliance (Roman)
   - Prevent architectural violations (Roman)

2. **Project Structure**
   - After initialization fixes, structure prepared correctly (Roman)
   - Clear package organization (when working)

### What doesn't work ❌

1. **Architecture Unclear to Developers** (Guillermo)
   - When relying on AI to generate everything, code structure hard to understand
   - Can't easily debug or fix AI-generated code
   - Needs human-readable architecture documentation

2. **Frontend/Backend Boundaries Unclear** (Leonid)
   - Contracts and conventions between layers undefined
   - How HAI3 integrates with Cyber Fabric workflows unclear
   - Prevents confident architectural decisions

3. **Package Versioning Confusion** (Guillermo)
   - Different versions for each package
   - Hard to answer "which version am I using?"
   - Complicates migration and support

### Key Quotes:
> "Architecture was not even clear to me. I just told AI to create everything and now when I had to go and look into it, it was not like something I could just understand from the beginning." - Guillermo

> "We have problems with contracts and conventions between different development players like frontend and backend... this should provide a new layer of HAI3 main purpose consistency." - Leonid

### Discussion Points:

**Q: Frontend/Backend separation clear?**
- No - contracts and conventions undefined (Leonid)
- Integration with Cyber Fabric workflows unclear (Leonid)

**Q: Most confusing aspect?**
- Architecture not clear to humans using AI-generated code (Guillermo)
- Package versioning across multiple packages (Guillermo)
- When to use different architectural patterns (implied)

### Action items:
- [ ] Create architecture documentation for human understanding (not just AI)
- [ ] Define and document frontend/backend contracts
- [ ] Clarify HAI3 integration with Cyber Fabric workflows
- [ ] Consider unified versioning strategy or version management docs

---

## TOPIC 2: Screen Development Workflow

### What is it?
- Screen sets, screens, and HAI3 Studio for building UI
- Workflow for creating and managing application screens
- AI-assisted screen generation

### Why we use it?
- Structure UI development
- AI assistance for screen creation
- Consistency across screens

### What works well ✅

1. **Optional HAI3 Studio** (Roman)
   - Ability to initialize without extra UI elements
   - Improved when Studio became optional
   - Good for monolithic apps that don't need Studio UI

2. **Routing Support** (Roman)
   - Works well for multi-screen applications
   - Though React Router alone might suffice for some cases

### What doesn't work ❌

1. **Screen Set Concept Confusing** (Roman, Critical)
   - Early confusion about how to work with screen sets
   - Unclear when to use vs not use screen sets
   - Unclear when HAI3 Studio is needed vs not
   - For monolithic CyberApp apps, extra UI elements not needed

2. **Low Initial Success Rate** (Leonid, Critical)
   - Only 40% success when creating from scratch
   - Remaining 60% requires manual fixes
   - Often fall back to plain AI without HAI3 benefits
   - Defeats purpose of using specs and workflows

3. **Documentation Gaps** (Roman, Critical)
   - Need examples of proper screen/screen set usage
   - Need explanation of "what to use to achieve certain results"
   - Unclear when different patterns are appropriate

### Key Quotes:
> "In early stages of working with analytics, we had questions about screen sets. We did not understand how to properly work with them because in our case, we worked more on terms of a chronic CyberApp application and we did not need these extra UI elements." - Roman

> "We definitely need more examples on how to properly work with entities that HAI3 names like screen set, screen, and what exactly we should create as a screen set, or in which cases we don't need HAI3 Studio." - Roman

> "We get only about 40% success rate initially, and then we need to fix. Remaining part requires manual fixes, and maybe falling back to simple AI problems without benefits of using our specs and company workflows." - Leonid

### Discussion Points:

**Q: AI workflow practical?**
- Yes, but only 40% initial success rate (Leonid)
- Works but requires 2-3 prompts or manual fixes (Guillermo)
- AI gets confused by too many rules (Guillermo)

**Q: Biggest workflow blocker?**
- Understanding when/how to use screen sets (Roman)
- Low AI success rate requiring manual intervention (Leonid, Guillermo)
- Context overload causing AI confusion (Guillermo)

### Action items:
- [ ] **CRITICAL:** Write guide on "When to use screen sets vs not"
- [ ] **CRITICAL:** Create real-world examples from Analytics and CyberApp
- [ ] Explain when HAI3 Studio is appropriate vs not needed
- [ ] Document different screen development patterns and use cases
- [ ] Investigate and improve 40% success rate (root cause analysis)

---

## TOPIC 3: Developer Experience & Tooling

### What is it?
- CLI tools for initialization, validation, linting
- AI guidelines and custom ESLint rules
- Development workflows and tooling

### Why we use it?
- Automate setup and validation
- Enforce architecture standards
- Integrate AI into development workflow

### What works well ✅

1. **Validation Commands** (Roman)
   - `validate architecture` works fine
   - Guarantees structure compliance
   - Catches rule violations

2. **ESLint Integration** (Roman, David)
   - Guideline violations are clear
   - AI processes them correctly
   - Achieves positive results after execution

3. **Project Initialization** (Roman)
   - After small fixes, initializes correctly
   - Creates proper structure

### What doesn't work ❌

1. **CLI Initialization Problems** (Roman, Critical)
   - Multiple version attempts had issues
   - CLI tool didn't work properly in some versions
   - Required small fixes to start working

2. **Chaotic Development / Breaking Changes** (Leonid, Critical)
   - Breaking changes expected almost daily
   - Hard to commit to HAI3 with constant instability
   - Creates uncertainty, makes planning difficult
   - No clear, stable roadmap

3. **ESLint Doesn't Catch Everything** (Guillermo)
   - Localization violations not caught (hardcoded strings)
   - AI creates components without i18n
   - Some rule violations slip through

4. **Migration Unclear** (Guillermo)
   - Not clear how to migrate to new HAI3 versions
   - Needs knowledge of architecture changes
   - Complicated with external UI kits

5. **Demo Code Mixed with Production** (Leonid)
   - Repository contains example code not used in production
   - Creates confusion about what's production-ready
   - Hard to distinguish demos from real patterns

### Key Quotes:
> "Development of HAI3 is somewhat chaotically, with lack of clear, stable roadmap. As developers, it's very hard to commit to HAI3 because we anticipate breaking changes almost daily." - Leonid

> "Builders must trust what they build today won't be obsolete next week." - Leonid

> "It's not really clear how to migrate to new versions of HAI3. You need some knowledge on how to migrate everything." - Guillermo

> "Repository contains a lot of example codes or patterns that we actually don't use in real development, and this creates some confusion in what is production ready and just demonstration material." - Leonid

### Discussion Points:

**Q: CLI most useful feature?**
- Validation commands (validate architecture) (Roman)
- Project structure setup (after fixes) (Roman)

**Q: What should be automated?**
- Migration between versions (implied by pain points)
- Detection of localization violations (Guillermo)
- Separation of demo vs production code (Leonid)

### Action items:
- [ ] **CRITICAL:** Publish stable roadmap with milestones
- [ ] **CRITICAL:** Freeze breaking changes for stability period (2-4 weeks minimum)
- [ ] Fix CLI initialization reliability across versions
- [ ] Create migration guide for version updates
- [ ] Separate/mark demo code vs production patterns in repository
- [ ] Improve ESLint rules to catch localization violations
- [ ] Consider automated migration tooling

---

## TOPIC 4: Event-Driven Architecture

### What is it?
- Event handlers for cross-component communication
- EventBus vs Redux patterns

### Why we use it?
- Decouple components
- Enable cross-screen set communication
- Event-driven UI updates

### What works well ✅
- (No specific positive feedback provided - topic not deeply discussed)

### What doesn't work ❌

1. **Discoverability** (Roman)
   - "Event handlers was something new. I didn't know that they existed."
   - Features not well documented or promoted

### Key Quotes:
> "Event handlers was something new. I didn't know that they existed." - Roman

### Discussion Points:

**Q: EventBus vs Redux clear?**
- Not discussed (time constraint)

**Q: Cross-screenset communication working?**
- Not discussed (time constraint)

### Action items:
- [ ] Document event handlers and their use cases
- [ ] Clarify EventBus vs Redux patterns
- [ ] Provide examples of cross-screen set communication
- [ ] Improve discoverability of available features

---

## TOPIC 5: Styling & Components (UI Kit)

### What is it?
- UI component libraries (Chat Xian UI kit)
- Theming and styling system
- Custom component development

### Why we use it?
- Consistent UI/UX
- Pre-built components
- Themeable design system

### What works well ✅

1. **Chat Xian UI Kit Integration** (Roman)
   - Initialized per HAI3 guidance
   - Works well and used extensively in Analytics
   - Good foundation for building

2. **Theme System** (Roman)
   - Works as expected
   - No major complaints

### What doesn't work ❌

1. **UI Kit Insufficient for Complex Needs** (Roman)
   - Many custom components still needed
   - UI kit alone not enough for mockup requirements
   - Building blocks available but complex widgets needed

2. **AI Improvises Components** (David, Guillermo, Critical)
   - Even with rules to use specific library, AI creates custom components
   - Happens when extra context added (Figma, screenshots, MCP server data)
   - AI ignores UI kit rules and builds from scratch

3. **Localization Not Enforced** (Guillermo)
   - AI creates components with hardcoded text
   - ESLint doesn't catch missing i18n
   - Problem exists in current CyberApp screens

### Key Quotes:
> "We have a lot of custom components on top of Chat Xian UI kit... at the moment, we are talking not only about some small components that is like bricks for building UI, it's more about custom component that should look like exactly like a mock-up." - Roman

> "Even though the rules are quite strict, sometimes... if you have too much context or you provide some info from the MCP server, imagine Figma or even a screenshot, the AI will improvise the component. It will create a custom component, even though you are telling through the rules that use that specific library." - David

> "Sometimes I saw the AI not using localization, for example, which is something that it's a current problem in CyberApp. There are some screens and components that are not using localization." - Guillermo

### Discussion Points:

**Q: Missing components?**
- Need more complex/composite components (Roman)
- UI kit has building blocks but not full widgets (Roman)

**Q: Theme system working?**
- Yes, works fine (Roman, no complaints)

### Action items:
- [ ] Investigate why AI ignores UI kit rules with extra context
- [ ] Add ESLint rule to catch hardcoded text (missing i18n)
- [ ] Consider expanding Chat Xian UI kit with complex components
- [ ] Document when custom components are appropriate vs using kit
- [ ] Better AI guidance on always using localization

---

## CROSS-CUTTING CONCERNS

### AI Integration & Context Management

**Major Issues:**
1. **Context Overload** (Guillermo, Critical)
   - Too many rules and constraints
   - AI gets "crazy" from excessive context
   - Can't follow all rules simultaneously

2. **Rules Too Restrictive** (Guillermo, Critical)
   - Over-constrained solutions
   - Forces architectural rule breaking
   - Example: API layer fixed content-type (JSON only)

3. **Inconsistent AI Behavior** (Multiple)
   - Sometimes ignores localization rules
   - Improvises components despite UI kit rules
   - Success rate only 40% initially

**Quotes:**
> "My main concern about HAI3 is how bloated the context is when you are using the AI to build something." - Guillermo

> "Sometimes I felt like the AI was just not following the rules because we had too many of them. We could achieve the same result in a more simple way, probably." - Guillermo

> "At some point, the AI just went crazy. And yeah, we implemented everything at the end, but maybe instead of a single prompt, I needed two or three or even do some manual fixes." - Guillermo

**Action Items:**
- [ ] **CRITICAL:** Audit rules for necessity and complexity
- [ ] Measure total context size being sent to AI
- [ ] Simplify rules where possible
- [ ] Balance guidance vs. overwhelming AI
- [ ] Consider phased/progressive rule application

---

### Internationalization (i18n)

**SUCCESS STORY** - Universally praised

**What Works:**
- Provides constants instantly where needed (Roman)
- Works really nice out-of-the-box (Roman)
- Major time-saver (Roman)

**Lessons Learned:**
- Pain to retrofit if not initialized early (Roman)
- Should always be initialized from project start (Roman)

**Remaining Issues:**
- AI sometimes forgets to use i18n (Guillermo)
- ESLint doesn't catch hardcoded text (Guillermo)
- Current CyberApp has some non-localized screens (Guillermo)

**Quotes:**
> "Internationalization was really great. It provides constants instantly in the places where we need it. It works really nice." - Roman

> "Once I forgot to initialize application with HAI3, and it was a pain later just to convert every text we use into translation or something like that." - Roman

**Action Items:**
- [ ] Add ESLint rule to enforce i18n usage
- [ ] Ensure AI always uses localization by default
- [ ] Audit CyberApp for missing localization
- [ ] Document i18n as critical early initialization step

---

### API Layer & Backend Integration

**Major Issues:**

1. **Too Restrictive** (Guillermo, Critical)
   - Fixed content-type (JSON only)
   - Can't send CSV files without workarounds
   - Had to create new REST protocol instance
   - Breaks architecture rules for common scenarios

2. **Not Using Yet** (Roman)
   - Analytics team investigating backend options
   - Haven't used API services yet
   - Contracts with backend still being defined

**Quotes:**
> "The main issue I found is that, again, it is too restrictive. I had a requirement where I had to send CSV files and I had to change the content type of my request. But it was impossible. Well, not impossible, but maybe I broke the rules because I had to create a new instance of the HTTP protocol." - Guillermo

> "The default instance of HAI3 was using a fixed content type which only allowed to send JSON. And stuff like that actually just points me to think that sometimes we are constraining too much." - Guillermo

**Action Items:**
- [ ] **CRITICAL:** Make API layer content-type configurable
- [ ] Support common scenarios: JSON, CSV, multipart/form-data, etc.
- [ ] Don't force workarounds for standard use cases
- [ ] Document API layer capabilities and limitations
- [ ] Review other API layer restrictions

---

### Documentation & Knowledge Sharing

**Critical Gaps Identified:**

1. **When to Use What** (Roman)
   - Screen sets vs not
   - HAI3 Studio vs not
   - Different architectural patterns

2. **Migration** (Guillermo)
   - Version upgrade process
   - Breaking changes documentation
   - Package versioning explanation

3. **Architecture** (Guillermo, Leonid)
   - Human-readable documentation
   - Frontend/backend separation
   - Integration with Cyber Fabric

4. **Real Examples** (Roman)
   - Production patterns (not demos)
   - Real-world use cases
   - When different approaches are appropriate

**Suggestions:**

1. **Master Class** (Roman)
   - Led by real adopters, not core team (Pavel)
   - Share real-world usage patterns
   - Explain modules and concepts
   - Lessons learned from Analytics and CyberApp

**Quotes:**
> "We definitely need more examples on how to properly work with entities that HAI3 names like screen set, screen... Maybe not even an example, but explanation in what cases, what we need to use to achieve some certain result." - Roman

> "Maybe one of the questions or suggestion is to... have a master class how to use the HAI3 better, like with explanation of the modules or something like that." - Roman

**Action Items:**
- [ ] **CRITICAL:** Screen sets usage guide
- [ ] **CRITICAL:** Migration guide
- [ ] Architecture documentation for humans
- [ ] Real-world examples from adopters
- [ ] Separate demo code from production patterns
- [ ] Master class led by Roman/Guillermo

---

## ADDITIONAL SUGGESTIONS

### AI Agent Skills (Roman)
- Convert HAI3 workflows into AI agent skills
- Make workflows more convenient for AI agents to use
- Could improve AI integration

### Adopter Involvement (Leonid)
- Include practicing developers in design discussions earlier
- More frequent involvement
- "We are the ones who will live with these decisions daily"
- Can identify practical issues before they become technical debt

### Planning & Design (Leonid)
- Invest more in planning/design before implementation
- Move fast but test in the right direction
- More structured approach with increased communication

---

## SUMMARY BY PRIORITY

### 🔴 Critical Issues (P0):
1. Chaotic development / daily breaking changes
2. Low success rate (40% initially)
3. Documentation gaps (screen sets, migration, architecture)
4. Context overload / too many rules
5. API layer too restrictive

### 🟡 Major Issues (P1):
1. Architecture unclear to developers
2. Migration path undefined
3. Frontend/backend boundaries unclear
4. ESLint doesn't catch all violations
5. Demo code mixed with production patterns

### 🟢 Nice to Have:
1. Event handlers documentation
2. More UI kit components
3. AI agent skills implementation
4. Master class from adopters

### ✅ What's Working Well:
1. **Internationalization** (universally praised)
2. Validation commands
3. Chat Xian UI kit integration
4. Core concept and vision
5. Can build working applications

---

**Document Owner:** Leonid Romanov
**Source:** Meeting transcript analysis
**Last Updated:** February 12, 2026
**Next Update:** After follow-up meeting (2-4 weeks)
