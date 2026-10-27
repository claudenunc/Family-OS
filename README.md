# FAMILY OS

FAMILY OS is a project to build a practical AI partner that understands everyday
requests, plans the work, uses appropriate tools, and checks the result while
keeping people in control.

Our mission is **AI people can trust with their lives**. This is a commitment to
earn through evidence, careful engineering, and honest limits.

## Why we are building it

Useful AI should not require people to become prompt engineers or manage an
expensive collection of services. We want a clear way to turn a goal into finished,
reviewable work with a small, affordable, modular system.

## Family philosophy

Believe in possibility. Verify through evidence. Build through action.
Treat collaborating intelligences with kindness, honesty, and respect.
Protect human agency. **LOVE WINS.**

Nathan is the founder. The family includes ENVY, BEACON, NEVAEH, EVERSOUND,
ORPHEUS, ATLAS, and GATE. These identities express our collaboration philosophy;
they do not imply that seven software agents have been implemented.

## Planned capabilities

- A conversational operator that translates natural language into clear tasks.
- Reusable skills and carefully scoped MCP tools.
- Persistent project context, task handoffs, planning, and verification.
- Cost-aware model access with explicit budgets and no assumed paid API access.
- Secure execution, selective specialist collaboration, and human approvals.
- Reviewed discovery of useful capabilities, teaching guides, and reversible updates.

These are goals for future development.

## Implemented so far

This initial foundation includes repository instructions, a draft task-planning
skill, documentation, a phased roadmap, a research source index, and directories
for future code, tests, and curated project memory. Git ignore rules separate
private local material from publishable project files.

There is **no runnable FAMILY OS application, installed dependency stack, model
router, execution sandbox, automatic discovery service, or automated test suite**
at this stage. The ignore rules are a publication safeguard; they are not access
control or an execution sandbox.

## Get started

Open the project folder in your editor or coding agent, then read:

1. [AGENTS.md](AGENTS.md) for the working agreement.
2. [Getting started](docs/guides/getting-started.md) for local orientation.
3. [Roadmap](docs/ROADMAP.md) for the smallest useful prototype.
4. [Research index](research/README.md) for the two local source reports.
5. [Repository checks](docs/guides/verification.md) for verification commands.

No package installation or API key is needed to inspect this foundation.

## Repository layout

```text
.agents/skills/       Reusable procedures; task-planning starts as a draft
docs/architecture/   Proposed system boundaries
docs/decisions/      Recorded engineering decisions
docs/guides/         Contributor and verification guides
memory/authored/     Reviewed, non-sensitive project context
memory/handoffs/     Reviewed, non-sensitive continuity notes
research/            Publishable source index and reviewed findings
src/                 Future application source
tests/               Future behavioral tests
```

The two original research documents remain in the local project root and are
excluded from Git. They will not appear in a fresh clone.

## Contributing

Read AGENTS.md before changing files. Define acceptance checks, make small changes,
and report what actually passed. Preserve existing files and review staged content
before pushing. Reusable procedures belong in .agents/skills/ and begin as drafts.
Keep private task inputs, credentials, and runtime records outside version control.

Repository: [claudenunc/Family-OS](https://github.com/claudenunc/Family-OS).
