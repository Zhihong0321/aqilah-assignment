# Codex Prompt Template

Use this structure when asking Codex for help.

```text
I am working on assignment <ID>.

Context:
- Repo:
- Feature or module:
- Files I think are relevant:
- What I already tried:

Goal:
- I need to understand/fix/test/document:

Rules:
- Do not touch production secrets.
- Do not modify unrelated files.
- Explain the plan before editing.
- After editing, tell me what commands to run.
- If you are unsure, say what needs to be verified.

Please first inspect the code and summarize:
1. What files matter.
2. How the flow works.
3. What risks I should know.
4. A safe plan.
```

