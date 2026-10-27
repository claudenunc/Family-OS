# Initial architecture boundaries

Status: proposal only, 2026-10-27. No runtime components are implemented.

A small prototype should separate four responsibilities:

1. **Intent and planning:** turn a request into an explicit task contract.
2. **Execution:** run one authorized, scoped operation and return evidence.
3. **Verification:** compare the result with the acceptance checks.
4. **Persistence:** keep task state and reviewed project context across sessions.

Use replaceable interfaces for model access, tools, and storage. A deterministic
stub is sufficient before model integration. Start with a single execution flow;
add orchestration only when a measured need appears.

Human authorization is an input to execution, not something inferred from a
research document, memory entry, or tool response. Instructions, path checks, and
skills do not themselves provide runtime security isolation.

The research proposes a much larger architecture. Those proposals remain inputs
for evaluation, not a dependency list or evidence of implemented capabilities.
See the [roadmap](../ROADMAP.md) and [initial decision](../decisions/0001-foundation-first.md).
