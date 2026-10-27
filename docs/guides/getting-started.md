# Getting started

The working repository is the Desktop folder named Family OS. The similarly named
ChatGPT project folder is conversation context; it is not a second checkout.

Open the repository root in your editor or coding agent. Read AGENTS.md, README.md,
and docs/ROADMAP.md. No Python environment, Node packages, API keys, or installation
commands are required for the current foundation. There is no app to launch yet.

For a new checkout, use Git to clone
https://github.com/claudenunc/Family-OS.git and open that checkout. The original
research reports are intentionally local and will not be included.

Before beginning a change:

1. Check the branch, origin, and working tree with the verification guide.
2. State the smallest useful outcome and observable acceptance checks.
3. Use the draft task-planning skill for a multi-step or ambiguous request.
4. Save non-sensitive decisions and continuity notes in the documented locations.
5. Keep raw inputs, credentials, runtime records, and original research outside Git.
6. Inspect the staged file list and content before a commit or publication.

Use .local/ for private scratch work in this checkout. Ignoring a file does not
encrypt it or prevent tools from reading it. Check for secrets in any file you
intend to share, including environment examples and documentation.

There is no selected application test command or dependency manager yet. Introduce
them with the first implementation, document their purpose, and test observable
behavior. See [verification](verification.md) for the foundation checks.
