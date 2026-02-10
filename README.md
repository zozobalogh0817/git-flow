# git-flow

A concise reference implementation of the **Git Flow branching model**, demonstrating clear and predictable workflows
for feature development, releases, and hotfixes.

This repository is intended for teams and developers who want a **practical, easy-to-understand Git Flow setup** that
can be used as a baseline for real projects.

---

## What this repository shows

* Standard Git Flow branch roles
* Feature-based development
* Release preparation and stabilization
* Hotfix handling for production issues
* Clean, readable Git history

---

## Branching model

```
main ──────────────────────────────▶ production
   ▲            ▲
   │            │
   │            └──── hotfix/*
   │
develop ────────┼──────────────────▶ integration
   ▲            │
   │            └──── release/*
   │
   └──── feature/*
```

---

## Branch roles

### `main`

* Production-ready code only
* Always deployable
* Tagged with release versions

### `develop`

* Integration branch for ongoing development
* Contains completed features for the next release

### `feature/*`

* New features or improvements
* Branched from `develop`
* Merged back into `develop`

### `release/*`

* Release stabilization
* Bug fixes, version bumps, documentation
* Merged into `main` and `develop`

### `hotfix/*`

* Critical production fixes
* Branched from `main`
* Merged into both `main` and `develop`

---

## Typical workflows

### Feature development

1. Create `feature/my-feature` from `develop`
2. Implement feature
3. Merge back into `develop`

---

### Release preparation

1. Create `release/1.2.0` from `develop`
2. Stabilize and finalize
3. Merge into `main` and `develop`
4. Tag release

---

### Hotfix

1. Create `hotfix/fix-critical-bug` from `main`
2. Apply fix
3. Merge into `main` and `develop`
4. Tag patch release

---

## When to use Git Flow

* Versioned releases
* Long-running projects
* Teams with structured release cycles
* Projects requiring clear production control

---

## License

MIT — free to use and adapt.