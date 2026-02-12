# GitHub Issues Templates for HAI3 Feedback

Use these templates to create GitHub issues based on meeting feedback.

---

## Template 1: Blocker Issue

```markdown
---
Title: [BLOCKER] [Brief description of the blocker]
Labels: blocker, priority:high, needs-triage
---

## Description

[Detailed description of what's blocking development]

## Impact

- **Severity:** [Critical / High / Medium / Low]
- **Affected Users:** [Number or "All developers"]
- **Workaround Available:** [Yes / No]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Steps to Reproduce

1.
2.
3.

## Expected Behavior

[What should happen]

## Actual Behavior

[What actually happens]

## Error Messages / Logs

```
[Paste any relevant error messages or logs]
```

## Proposed Solution

[If the developer suggested a solution, include it here]

## Additional Context

- HAI3 Version: 0.1.0
- Environment: [OS, Node version, etc.]
- Related Issues: [Links to related issues if any]

## Acceptance Criteria

- [ ] [Specific criterion 1]
- [ ] [Specific criterion 2]
- [ ] [Specific criterion 3]
```

---

## Template 2: Feature Request

```markdown
---
Title: [FEATURE] [Brief description of the feature]
Labels: enhancement, needs-triage
---

## Description

[Detailed description of the requested feature]

## Problem Statement

[What problem does this solve? Why is it needed?]

## Requested By

- **Developer:** [Name(s)]
- **Date Requested:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Use Case

[Describe a specific use case where this feature would be valuable]

### Example Scenario

```
[Code example or scenario description]
```

## Proposed Solution

[How the developer suggests implementing this]

## Alternative Solutions Considered

[Any alternative approaches mentioned]

## Impact

- **Priority:** [High / Medium / Low]
- **Effort Estimate:** [Small / Medium / Large]
- **Affected Users:** [Who benefits from this]

## Related Features

[Link to related features or issues]

## Acceptance Criteria

- [ ] [Specific criterion 1]
- [ ] [Specific criterion 2]
- [ ] [Specific criterion 3]
```

---

## Template 3: Documentation Gap

```markdown
---
Title: [DOCS] [Brief description of documentation needed]
Labels: documentation, needs-triage
---

## Description

[What documentation is missing or unclear]

## Affected Area

- **Topic:** [e.g., "Event-driven architecture", "Screenset creation", etc.]
- **Location:** [Where this should be documented]
- **Existing Docs:** [Link to existing docs if any]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Problem

[What confusion or issue did this cause?]

### Specific Questions That Need Answers

1.
2.
3.

## Current Workaround

[How developers are currently figuring this out]

## Proposed Content

[What should the documentation cover?]

### Suggested Outline

1. [Section 1]
2. [Section 2]
3. [Section 3]

### Code Examples Needed

```
[Example of what code examples should be included]
```

## Priority

- **Impact:** [High / Medium / Low]
- **Frequency:** [How often developers hit this issue]

## Acceptance Criteria

- [ ] Documentation written and reviewed
- [ ] Code examples included and tested
- [ ] Developer verified documentation is clear
- [ ] Added to appropriate location in docs
```

---

## Template 4: Bug Report

```markdown
---
Title: [BUG] [Brief description of the bug]
Labels: bug, needs-triage
---

## Description

[Clear description of the bug]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Environment

- HAI3 Version: 0.1.0
- Node Version:
- OS:
- Package Manager: npm/yarn/pnpm

## Steps to Reproduce

1.
2.
3.

## Expected Behavior

[What should happen]

## Actual Behavior

[What actually happens]

## Error Messages / Logs

```
[Paste any relevant error messages or logs]
```

## Code Sample

```typescript
// Minimal reproducible example
```

## Screenshots

[If applicable, add screenshots]

## Workaround

[If the developer found a workaround, include it]

## Possible Root Cause

[If the developer has insights on what might be causing this]

## Impact

- **Severity:** [Critical / High / Medium / Low]
- **Frequency:** [Always / Sometimes / Rarely]
- **Workaround Available:** [Yes / No]

## Acceptance Criteria

- [ ] Bug is reproducible
- [ ] Root cause identified
- [ ] Fix implemented
- [ ] Test added to prevent regression
- [ ] Documentation updated if needed
```

---

## Template 5: Developer Experience Improvement

```markdown
---
Title: [DX] [Brief description of DX improvement]
Labels: developer-experience, needs-triage
---

## Description

[What aspect of developer experience needs improvement]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Current Friction

[Describe the current friction in the developer workflow]

### Example Scenario

[Specific example of when this friction occurs]

## Impact on Development

- **Time Cost:** [How much time this friction costs]
- **Frequency:** [How often developers hit this]
- **Frustration Level:** [High / Medium / Low]

## Proposed Improvement

[How this could be improved]

### Suggested Implementation

[If the developer has implementation ideas]

## Examples from Other Tools

[Are there examples from other frameworks/tools that do this well?]

## Benefits

-
-
-

## Effort Estimate

[Small / Medium / Large]

## Acceptance Criteria

- [ ] [Specific criterion 1]
- [ ] [Specific criterion 2]
- [ ] [Specific criterion 3]
- [ ] Developer feedback collected on improvement
```

---

## Template 6: CLI Enhancement

```markdown
---
Title: [CLI] [Brief description of CLI enhancement]
Labels: cli, enhancement, needs-triage
---

## Description

[What CLI enhancement is needed]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Current Situation

[What developers currently have to do manually]

### Manual Steps

1.
2.
3.

## Proposed Command

```bash
hai3 [command] [options]
```

### Expected Behavior

[What the command should do]

### Options/Flags

- `--flag1`: [description]
- `--flag2`: [description]

## Use Cases

### Use Case 1
[Describe specific use case]

### Use Case 2
[Describe specific use case]

## Impact

- **Frequency:** [How often this is needed]
- **Time Saved:** [Estimated time saved per use]
- **Affected Users:** [All / Some developers]

## Implementation Notes

[Any technical considerations for implementation]

## Acceptance Criteria

- [ ] Command implemented with proper options
- [ ] Help text written (--help)
- [ ] Error handling implemented
- [ ] Tests added
- [ ] Documentation updated
- [ ] Announced in changelog
```

---

## Template 7: AI Guidelines Issue

```markdown
---
Title: [AI] [Brief description of AI guidelines issue]
Labels: ai-guidelines, documentation, needs-triage
---

## Description

[What's wrong with the current AI guidelines]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Affected Files

- `.ai/GUIDELINES.md`
- `.ai/targets/[TARGET].md`
- Other:

## Problem

[Specific problem with current guidelines]

### Example of Confusion

[Real example where guidelines were unclear or contradictory]

## Current Guideline

```
[Quote the problematic guideline]
```

## Why It's Problematic

[Explain the issue]

## Proposed Change

```
[Suggested new wording or approach]
```

## Impact

- **Affects AI Workflow:** [Yes / No]
- **Causes ESLint Violations:** [Yes / No]
- **Blocks Development:** [Yes / No]

## Related ESLint Rules

[If this relates to custom ESLint rules, list them]

## Acceptance Criteria

- [ ] Guidelines updated
- [ ] ESLint rules aligned (if applicable)
- [ ] Examples added to clarify
- [ ] Developer verified clarity
- [ ] AI tested with new guidelines
```

---

## Template 8: Quick Win

```markdown
---
Title: [QUICK WIN] [Brief description]
Labels: quick-win, priority:high
---

## Description

[Simple improvement that can be delivered quickly]

## Reported By

- **Developer:** [Name(s)]
- **Date Reported:** [Date]
- **Meeting:** HAI3 Adopters Feedback - 2026-02-12

## Why This is a Quick Win

- **Effort:** [1-2 days / 1 week]
- **Impact:** [High / Immediate value]
- **Risk:** [Low / No breaking changes]

## Current Problem

[What's the issue this solves]

## Proposed Solution

[Simple, clear solution]

## Implementation Steps

1.
2.
3.

## Impact

- **Developers Affected:** [Number or "All"]
- **Immediate Benefit:** [What improves right away]

## Acceptance Criteria

- [ ] [Specific criterion 1]
- [ ] [Specific criterion 2]
- [ ] Deployed to v0.1.1 or v0.2.0

## Target Milestone

v0.1.1 or v0.2.0
```

---

## Issue Creation Workflow

### After Meeting:

1. **Review meeting notes** and identify distinct issues
2. **Categorize** issues by type (blocker, feature, bug, docs, etc.)
3. **Create GitHub issues** using appropriate templates
4. **Add labels** for priority, area, and type
5. **Link related issues** if applicable
6. **Assign owners** for each issue
7. **Add to project board** with appropriate status
8. **Share issue list** with meeting attendees for verification

### Priority Levels:

- **P0 (Blocker):** Critical - blocks development
- **P1 (High):** Important - significantly impacts developers
- **P2 (Medium):** Nice to have - improves experience
- **P3 (Low):** Future - can wait for later releases

### Labels to Use:

- **Type:** `bug`, `enhancement`, `documentation`, `cli`, `ai-guidelines`
- **Priority:** `priority:critical`, `priority:high`, `priority:medium`, `priority:low`
- **Status:** `needs-triage`, `in-progress`, `blocked`, `ready-for-review`
- **Area:** `architecture`, `screensets`, `events`, `styling`, `devex`
- **Special:** `blocker`, `quick-win`, `breaking-change`, `good-first-issue`
