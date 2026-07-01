# Branching

```
feature/*  →  dev  →  main
```

- **`feature/*`** — one branch per change. Branch off `dev`, PR back into `dev`.
- **`dev`** — active integration.
- **`main`** — protected. Direct pushes are blocked; the only way in is a PR.

**Branch protection:** GitHub's branch protection (classic rules and the newer
Rulesets) requires a **GitHub Pro** upgrade for private repos on a personal
account — confirmed via the API. Where this repo is private and unprotected
server-side, `.githooks/pre-push` (wired via `git config core.hooksPath
.githooks`) blocks direct pushes to `main` from this machine instead. That's a
local safety net, not a server-side guarantee — a fresh clone needs
`git config core.hooksPath .githooks` run once.

Emergency override: `ALLOW_PROTECTED_PUSH=1 git push origin main`.
