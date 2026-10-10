
---
name: pm-spec
description: Produce a one-page product spec or PRD.
  Use for product specs, feature briefs,
  feature documentation, and requirements documents.
---

# Product Spec Skill

Produce a one-page product spec / PRD.

## Workflow

1. Read the active DESIGN.md.
2. Identify the feature + audience from the brief.
3. Layout:
   - Header strip: title, status pill (Draft / Review / Approved), date, owner.
   - Three-line summary at the top — what, who, why now.
   - "Problem" panel with one paragraph and a quote from a customer or internal partner.
   - "Goals & non-goals" two-column block.
   - "Success metrics" table with metric / target / measurement.
   - "User stories" list with as-a / I-want / so-that format.
   - "Scope" milestone tracker (3–4 phases).
   - "Open questions" with assignee chips.
4. One inline &lt;style&gt;, semantic HTML, accent used twice max.

## Output contract

&lt;artifact identifier="spec-name" type="text/html" title="Spec Title"&gt; &lt;!doctype html&gt;...&lt;/artifact&gt;
  
