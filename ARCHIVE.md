# CIVILIZATION ZERO // SYSTEM ARCHIVE

> A technical index of the systems represented by this repository. This file documents architecture, boundaries, recurring patterns, and the engineering problems each archive is meant to solve.

---

## 00 / CLASSIFICATION MODEL

| Class | Meaning |
|---|---|
| `CORE` | End-to-end product/runtime with real state and operational behavior |
| `ACTIVE` | Current development surface with meaningful iteration |
| `ALPHA` | Functional architecture with unfinished edges explicitly labelled |
| `LAB` | Focused environment for testing a systems/product hypothesis |
| `PRIVATE` | Real system whose source is intentionally not exposed publicly |

---

# 01 / RECHARZA

**Classification:** `CORE / PRIVATE`  
**Domain:** game-commerce infrastructure  
**Primary concern:** transaction correctness across customer, product, provider, payment, order, and support state

## Problem

A top-up storefront is easy to imitate visually. A reliable commerce runtime is not. The difficult part begins after a customer presses a button: account validation, package compatibility, price ownership, authentication, payment state, order persistence, supplier behavior, duplicate attempts, support recovery, and private tracking all have to agree on what happened.

## System shape

```text
CATALOG
  ↓
PRODUCT SELECTION
  ↓
PLAYER / ACCOUNT VALIDATION
  ↓
CART
  ↓
CHECKOUT
  ↓
PAYMENT BOUNDARY
  ↓
ORDER COMMIT
  ↓
FULFILMENT / PROVIDER
  ↓
TRACKING + SUPPORT
```

## Important boundaries

- **Catalog vs fulfilment:** something being visible does not mean supplier writes are enabled.
- **Displayed price vs committed price:** checkout owns the final price state.
- **Authentication vs order access:** identity and private tracking must remain distinct concerns.
- **Payment attempt vs payment confirmation:** external initiation is not completion.
- **Provider response vs customer-visible order state:** upstream behavior is normalized before reaching the user.
- **Support visibility vs sensitive data:** diagnostics must help recovery without exposing customer or provider secrets.

## Engineering pattern

```text
VALIDATE → COMMIT INTENT → EXTERNAL ACTION → VERIFY → FINALIZE
                         │
                         └──── failure → RECOVERABLE STATE
```

---

# 02 / NEXUS FORGE

**Classification:** `ACTIVE / ALPHA`  
**Domain:** governed engineering-agent runtime  
**Public repository:** [nexus-forge](https://github.com/sphangcho203-afk/nexus-forge)  
**Current public release line:** `0.5.0-alpha.34`

## Problem

Modern coding models are capable, but capability alone does not create an engineering system. Users still have to manage provider setup, permissions, retries, raw logs, incomplete changes, context loss, and uncertainty about whether the requested work is actually finished.

NEXUS moves those responsibilities into the runtime.

## Mission lifecycle

```text
REQUEST
  → CONTRACT
  → STRATEGY + BUDGET
  → ORIENT
  → PLAN
  → CAPABILITY / CRITIC GATE
  → ACT
  → OBSERVE
  → VERIFY
  → REFLECT / RECOVER
  → EVIDENCE REPORT
```

## Runtime responsibilities

- convert requests into observable done conditions;
- maintain dependency-aware mission state;
- enforce specialist and tool capability boundaries;
- route providers without making provider health invisible;
- preserve evidence and checkpoints across failures;
- detect repetition/no-progress loops;
- verify fresh state after mutation;
- block completion when proof is missing;
- report what changed and what remains uncertain.

## Architectural split

| Layer | Responsibility |
|---|---|
| Python core | mission contracts, cognition, tools, providers, permissions, evidence, recovery |
| Go UI | terminal rendering and operator interaction |
| Event ledger | append-only durable mission history |
| Tool fabric | typed workspace/shell/network/repository operations |
| Provider mesh | APIs, official agent bridges, local/mock routes |
| Evidence gate | observable completion proof |

## Design invariant

> **The model may choose a candidate action. The runtime still decides whether it is allowed, how it executes, what is persisted, and what proves completion.**

---

# 03 / NOVA COMMAND

**Classification:** `LAB`  
**Domain:** operational mission control  
**Public repository:** [nova-command](https://github.com/sphangcho203-afk/nova-command)

## Problem

Project tools often split planning from execution. Tasks live in one place, ideas in another, project state somewhere else, and the actual work happens in a terminal or browser with no shared operational picture.

Nova Command explores a tighter control surface.

## Desired information hierarchy

```text
NOW
├── active mission
├── blockers
└── next executable action

PROJECTS
├── current state
├── risk / drift
└── milestones

INBOX
├── ideas
├── unresolved items
└── captured context
```

## Constraint

A mission-control dashboard fails when maintaining the dashboard becomes more expensive than doing the work. The interface therefore has to compress state rather than reproduce every underlying tool.

---

# 04 / JARVIS APP

**Classification:** `ACTIVE`  
**Domain:** phone-first Android assistant runtime  
**Public repository:** [JarvisApp](https://github.com/sphangcho203-afk/JarvisApp)  
**Current public line:** `Phase 9.2B / System Control Bridge`

## Problem

An assistant that can answer questions but cannot reliably act on the device is limited. An assistant that lets a language model directly improvise device actions is unsafe and difficult to verify.

Jarvis separates reasoning from deterministic Android execution.

## Routing model

```text
VOICE / TEXT COMMAND
        │
        ▼
LOCAL INTENT KERNEL
   │             │
known action     reasoning required
   │             │
   ▼             ▼
ANDROID API    PROVIDER MESH
   │             │
   ▼             ▼
VERIFIED        STRUCTURED
ACTION STATE    RESPONSE
```

## Local execution surface

- app launch and discovery;
- battery and network state;
- flashlight;
- media controls and volume;
- brightness and rotation;
- timers and memory;
- Quick Settings system-control bridge after explicit user enablement;
- bounded state verification when Android/SystemUI exposes it.

## Provider boundary

Cloud reasoning is used only after the deterministic local kernel declines a command. Provider configuration is encrypted with Android Keystore and failover is bounded rather than unlimited.

## Design invariant

> **Known device actions should be executed by deterministic Android code, not reconstructed from free-form model prose.**

---

# 05 / RECURRING SYSTEM PATTERNS

## Contract-first execution

```text
INTENT → OBSERVABLE DONE STATE → PLAN → ACTION → EVIDENCE
```

If the done state cannot be observed, the system cannot reliably know that it succeeded.

## Explicit control planes

A control plane usually owns some combination of:

- permissions;
- authentication;
- provider selection;
- state transitions;
- retries;
- evidence;
- audit history;
- recovery.

## Failure as state

Failures should be classifiable and actionable rather than flattened into generic errors.

```text
FAILURE
  ├─ invalid input
  ├─ permission denied
  ├─ unavailable dependency
  ├─ provider failure
  ├─ verification mismatch
  ├─ timeout / uncertain result
  └─ internal invariant violation
```

Each class should imply a different recovery path.

## Verification after mutation

```text
WRITE / ACTION
   ↓
READ FRESH STATE
   ↓
COMPARE AGAINST CONTRACT
   ↓
PASS / RECOVER
```

The write response itself is not enough when the system can observe the resulting state directly.

---

# 06 / STACK MAP

| Surface | Typical technology |
|---|---|
| Product UI | React, Next.js, Kotlin/Android, terminal UI |
| Runtime | TypeScript/Node, Python, Go, Android APIs |
| Data | PostgreSQL, Prisma, durable ledgers, structured local state |
| Intelligence | model APIs, provider meshes, agents, tool protocols |
| Control | auth, permissions, scopes, policy, capability gates |
| Reliability | health checks, retries, checkpoints, rollback, recovery |
| Proof | tests, observed state, evidence records, completion reports |

---

# 07 / ARCHIVE RULE

A project belongs in this archive when it demonstrates at least one serious systems problem: state ownership, constrained execution, provider boundaries, recoverability, operational control, device integration, evidence, or end-to-end product behavior.

Decorative prototypes can exist elsewhere. The archive is for systems that have something to prove.
