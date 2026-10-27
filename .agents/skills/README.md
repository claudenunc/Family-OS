# FAMILY OS skill library

A skill is a small, reusable procedure that an agent can load for a specific task.
Keep each skill in its own folder:

```text
.agents/skills/<skill-name>/SKILL.md
```

SKILL.md starts with YAML frontmatter containing a lowercase, hyphenated name and
a description explaining what the skill does and when to use it. The folder and
name must match. Keep the body focused; add scripts, references, or assets only
when they provide a concrete benefit. Inspect executable helpers before use.

## Lifecycle

1. Write a narrow draft tied to a real need. Set metadata.status to draft.
2. Check the format, routing description, referenced files, and authorization
   boundaries. Run the skill-creator validator when available.
3. Exercise realistic requests: a clear task, an ambiguous task, and a request
   containing a consequential action. Record observable results and limitations
   in docs/guides/ or a review.
4. Have the maintainer review the evidence and accept the skill before changing
   its status to validated. Format checks alone do not establish reliability.
5. Recheck affected behavior after changes; keep changes versioned and reversible.

Draft status records maturity. It does not disable the host's skill discovery,
grant tool permissions, or override user instructions. A draft may be evaluated
within an explicitly authorized task.

## Starter

[task-planning](task-planning/SKILL.md) translates a natural-language request into
a goal, constraints, a plan, and acceptance checks. It remains a draft pending
real-use validation and maintainer acceptance.

No external community skills are installed by this foundation.
