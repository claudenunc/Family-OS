# Initial roadmap

Status: proposed development sequence, 2026-10-27. Only the repository foundation
exists. The [research index](../research/README.md) identifies the two local reports;
their technology, price, benchmark, and security claims are not adopted as facts.

## 0. Foundation (this setup)

Create and verify the repository, instructions, draft skill, documentation, and
private-data exclusions. Preserve existing research and publish only reviewed
foundation files. No application or dependency installation is included.

## 1. Prove one useful task by hand

Use the draft task-planning skill in the existing assistant to turn one founder
request into a clear task contract: goal, inputs, constraints, permissions,
deliverables, and acceptance checks. Use synthetic or non-sensitive inputs.

Suggested first case: "Turn these three project notes into a plan and a handoff."
Success means the result identifies assumptions, has testable acceptance checks,
and survives a fresh-session handoff without invented completion.
Validate the skill in actual use before maintainer acceptance.

## 2. Build a small local task runner

Proposed first implementation: a Python command-line program using the standard
library, JSON task records, and one deterministic tool for approved project notes.
Keep the planning interface separate from storage and execution. Start with a
manual task contract or a stub model adapter; no paid service is required.

Acceptance checks: a valid contract produces the expected new artifact; invalid
input fails clearly; paths outside the configured workspace, traversal, links
escaping the workspace, and attempts to overwrite existing files are rejected.
A restart recovers task state. A failed operation is recorded as failed.

A browser-first TypeScript prototype is the second option if a visual interaction
is the immediate requirement. It adds interface and persistence decisions before
proving execution. Choose it only when the first user workflow needs that UI.

## 3. Add one conversational path and persistent context

Choose one available, authorized model interface after checking current primary
documentation, access, cost, and Windows compatibility. Existing interactive
assistant access does not establish permission or feasibility for a programmatic
API or gateway. Keep deterministic fixtures as the offline development fallback.

Persist small task records and reviewed summaries locally; separate human-authored
context from generated observations. Start with JSON; consider SQLite when actual
query needs justify it. No vector database is needed for the first workflow.

Acceptance checks: known requests yield valid contracts; ambiguous or unauthorized
requests do not silently execute; restart preserves state; provider unavailability
produces a clear failure; task limits stop further work. Measure actual usage
before adding routing, caching, or a second model.

## 4. Harden execution, then add capabilities

Establish and test an appropriate Windows-compatible isolation mechanism before
allowing third-party executable tools. Path checks and approval prompts are only
application controls, not an isolation boundary. Verify escape and cancellation
cases using harmless fixtures.

Add one reviewed skill or MCP integration at a time with scoped permissions,
failure checks, an adoption decision, and a rollback path. Introduce a simple
conversational UI only after the complete workflow is useful.

## 5. Expand when evidence justifies it

Consider model routing, specialist collaboration, capability discovery, and
automated update proposals after measuring completion quality, cost, latency,
and recovery. Keep adoption and deployment under human control.

## Constraints and failure modes

- New spending budget for the prototype is zero unless the founder changes it.
  Existing subscriptions and local hardware have limits; do not promise unlimited use.
- Frameworks, cloud services, external skills, and background discovery are deferred.
- Ambiguous requests can cause wrong work: make assumptions and checks visible.
- Research can be stale or unsupported: verify primary sources before adopting a tool.
- Memory can leak personal data: keep raw inputs and runtime state outside Git.
- A tool may partially fail: retain evidence, distinguish failure from success, and
  avoid retrying consequential actions without checking their actual state.

Next deliverable: one real task contract and its observed skill-validation result.
