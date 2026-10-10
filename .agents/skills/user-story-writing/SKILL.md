---
name: user-story-writing
description: Write or revise product user stories with testable acceptance criteria, error and edge cases, and open questions. Use when a user shares feature context, screenshots, designs, requirements, or stakeholder feedback and requests user stories or development-ready tickets.
---

# User Story Writing

Turn supplied product context into clear requirements for developers, QA, and stakeholders. Use plain language suitable for junior developers and non-technical readers.

## Workflow

1. Read the repository's MEMORY.md, ORCHESTRATION.md, AGENTS.md, and required bootstrap rules when not already loaded. Confirm the files actually read.
2. Read the user's feature brief, screenshots, and explicitly referenced requirements or decisions. Load relevant existing initiative context when available.
3. Identify the feature, user roles, intended benefit, entry point, main journey, and scope. Reuse answers already supplied. Ask concise questions only when missing information materially changes the behavior.
4. Separate confirmed requirements, visible UI observations, recommendations, and unresolved business rules. Treat screenshots as evidence of visible UI, not proof of hidden permissions or backend behavior. Flag contradictions instead of silently choosing a rule.
5. Split the journey into independently understandable stories, each covering a meaningful user goal. Preserve the supplied roles and terminology.
6. Write acceptance criteria for each story, then link its error and edge cases to the relevant criteria.
7. Record unresolved decisions as open questions. Draft supported portions while marking affected criteria as pending clarification.
8. Run the quality check below before presenting the result.

## Evidence and Missing Rules

- Do not invent business rules, metrics, targets, limits, dates, prices, permissions, eligibility, retry counts, notification intervals, or technical implementation.
- Include exact values only when supplied by the user or a relevant source. Identify the source when a value or decision could be disputed.
- If expected behavior is not specified, mark it "Pending clarification" and add a linked open question. Put suggested behavior under "Recommendation — requires confirmation."
- Distinguish UI copy suggestions from confirmed copy. Do not turn suggestions into acceptance criteria.
- Preserve unresolved conflicts and explain which stories they affect.
- Use DESIGN.md only when relevant and available, especially for a requested visual artifact. Do not require it for ordinary Markdown user stories.
- Do not add success metrics or a full PRD unless requested.

## Output Format

Default to Markdown. Follow a different format if the user explicitly requests one.

### Feature Context

Briefly state the feature, audience, purpose, and confirmed scope. List source files or screens used. Mark missing context as unspecified.

### User Stories

| Story ID | Title | User story |
|---|---|---|
| US-01 | [User goal] | As a [role], I want to [action], so that [benefit]. |

### Acceptance Criteria

| AC ID | Story ID | Given | When | Then |
|---|---|---|---|---|
| AC-01 | US-01 | [Initial state or precondition] | [User action or system event] | [Observable, testable outcome] |

- Use unique IDs throughout the deliverable.
- Keep each criterion focused on one behavior. Split alternative conditions into separate rows.
- Cover the main journey and any confirmed validation, state changes, saved data, configuration logic, or permissions.
- State observable results; avoid vague phrases such as "works correctly" or "user-friendly."
- For unresolved criteria, identify the open-question ID and mark the outcome pending.

### Error and Edge Cases

| Case ID | Story / AC ID | Scenario or trigger | Expected behavior | Status / source |
|---|---|---|---|---|
| EC-01 | US-01 / AC-01 | [Failure or boundary condition] | [Confirmed response, or pending with question ID] | [Confirmed / Pending clarification / Recommendation] |

Consider relevant cases such as invalid or missing input, empty results, network or service failure, repeated actions, stale state, interrupted journeys, and confirmed permission boundaries. Include only cases relevant to the feature. Do not assert support for a case or invent recovery behavior.

### Open Questions

| Question ID | Missing rule or decision | Affected story / criterion | Why it matters |
|---|---|---|---|
| Q-01 | [Specific decision needed] | US-01 / AC-01 | [Effect on implementation or QA] |

Write "None identified from the supplied context" when no material questions remain. Do not invent assignees, deadlines, or answers.

### Recommendations

Include this section only when useful. Clearly label each proposal as requiring confirmation, separate from confirmed requirements.

## Quality Check

- Check that each story expresses a user goal and benefit.
- Check that each confirmed criterion is traceable to supplied context and testable.
- Check that error and edge cases link to the affected story or criterion.
- Check that configuration values, boundary behavior, and permissions use confirmed rules.
- Check that unresolved behavior is marked pending and linked to an open question.
- Remove unsupported rules, invented numbers, duplicated criteria, and unnecessary implementation detail.
- Confirm that wording and statuses are consistent across all tables.
- Report material gaps; do not call a draft development-ready when blocking decisions remain.

## Delivery

Present the stories, acceptance criteria, error and edge cases, and open questions together. Include a concise "Files read" note with only verified paths. Save or update a deliverable only in the destination authorized by the user or required by the environment. Do not commit generated stories or alter repository instructions merely because GitHub is connected.
