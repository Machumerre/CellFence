# Contributing

CellFence changes should keep the implementation narrow and the specification honest.

Before submitting a change, run:

```bash
npm ci
npm run lint
npm run typecheck
npm test
npm run build
npm run cellfence:self-check
```

Do not relax fixture expectations to hide implementation defects. If a fixture reveals an ambiguity, record the ambiguity in the change description and update the protocol only when the intended rule is clear.

Publishing is intentionally not automated in v0.x. Future npm publishing should use GitHub OIDC trusted publishing rather than long-lived package tokens.

## Lightweight contributor workflow

If you’re new to the project or just want to tackle a small issue, follow this short path:

1. **Pick an issue** – look for issues labeled `good first issue` or `help wanted`.  
2. **Comment before you start** – add a comment on the issue stating you’re working on it. This keeps the maintainer aware and prevents duplicate work.  
3. **Keep the PR focused** – the pull request should address only the acceptance criteria of the issue. Avoid adding unrelated changes or generated output.  
4. **Run the minimal validation** – execute the smallest relevant CI checks (e.g., `make test` or `pytest -q`).  
5. **Report skipped slow checks** – if you skip a longer check (e.g., mutation testing, full linting), mention it explicitly in the PR body and explain why.  
6. **Include validation results** – paste the output or a link to the CI run in the PR description so reviewers can verify the changes.  

This workflow keeps the review cycle short and encourages quick, high‑quality contributions.
