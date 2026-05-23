# `$ems-commands` — Effort Management System command bindings

> **Sibling of:** `kitelev/exocortex-ems-ontology` (ems TBox — class + property declarations)
> **Distinct from:** `kitelev/exocortex-ems-commands-test` (test fixtures + acceptance assets)

## Purpose

Houses the **ABox command bindings** for the `ems__` domain — `exocmd__Command` + `exocmd__Grounding` + `exocmd__InheritanceRule` assets that target ems classes (Task, Area, Project, Effort).

The pilot for homoiconic plugin testing (RFC `aaaa2dea`) — `bb00efed` "Create Task Instance" + grounding `a6ef8fda` + 3 inheritance rules — lives here as of Phase 2 (2026-05-23).

## Import chain

```
ems-commands  ──imports──▶  ems  (target class wikilinks: ems__Task, ems__Area, etc.)
              ──imports──▶  exocmd  (command/grounding meta-classes via exo)
              ──imports──▶  exo  (core types)
```

Submodules wired in:

```
assetspaces/ems   ← kitelev/exocortex-ems-ontology
```

## Conventions

- All assets UUID-named (RFC-004 UUID-canon).
- `exo__Asset_isDefinedBy` points to `$ems-commands` root (`be2c3f06-48db-4a38-a21d-a81ce1836815`).
- Cross-repo wikilinks resolved at vault-clone time via `git clone --recurse-submodules`.

## Peer repositories

- `kitelev/exocortex-ems-ontology` (ems TBox)
- `kitelev/exocortex-exocmd-ontology` (exocmd meta-TBox)
- `kitelev/exocortex-test-ontology` (test__ namespace TBox for homoiconic testing)
- `kitelev/exocortex-ems-commands-test` (acceptance fixtures for ems-commands)
