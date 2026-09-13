<p align="center">
  <img src="./assets/profile-hero.gif" width="100%" alt="Ike Shanto systems engineering profile" />
</p>

<div align="center">
  <h2>Ike Shanto</h2>
  <p><strong>Systems Engineering · AI Runtimes · Product Infrastructure · Android Control</strong></p>
  <p>
    I build software as an operating system of decisions, state, tools, permissions, recovery, and proof.<br/>
    The interface matters. The machinery behind it matters more.
  </p>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/SYSTEMS-0B1118?style=for-the-badge&logoColor=white" alt="Systems" />
  <img src="https://img.shields.io/badge/AI_RUNTIME-0B1118?style=for-the-badge&logoColor=white" alt="AI Runtime" />
  <img src="https://img.shields.io/badge/PRODUCT_INFRA-0B1118?style=for-the-badge&logoColor=white" alt="Product Infrastructure" />
  <img src="https://img.shields.io/badge/ANDROID_CONTROL-0B1118?style=for-the-badge&logoColor=white" alt="Android Control" />
</p>

<p align="center">
  <img src="./assets/profile-divider.gif" width="100%" alt="Animated system signal" />
</p>

<p align="center">
  <img src="./assets/profile-command-deck.svg" width="100%" alt="Detailed engineering command deck" />
</p>

## Engineering surface

I am interested in the point where a polished interface stops being a mockup and becomes a **real operational system**.

**Product systems** — authentication, ownership, persistence, workflows, recovery, verification, and the state transitions that make the product behave correctly outside the happy path.

**AI runtimes** — tool-using assistants, provider routing, approvals, memory, typed execution, and boundaries that keep model reasoning separate from deterministic actions.

**Android + device control** — phone-first software where known device operations stay local and predictable, while reasoning is used only where it actually adds value.

**Web intelligence** — retrieval, extraction, parsing, structured analysis, provenance, and reusable research pipelines that remain inspectable instead of turning into an opaque scraper pile.

<br/>

<p align="center">
  <img src="./assets/profile-runtime-map.svg" width="100%" alt="Runtime architecture map" />
</p>

## What sits behind the interface

A system becomes interesting when the visible UI is backed by explicit control.

- **State has an owner.** Important transitions should not depend on accidental component behavior.
- **Permissions are part of the architecture.** Capability should be granted deliberately, not implied by convenience.
- **Tools return evidence.** An action is not complete because a model says it probably worked.
- **Providers can fail.** Routing, fallback, retries, and degraded states are product behavior.
- **Recovery is designed early.** Checkpoints, rollback, and diagnosable failure are easier to build before everything becomes tangled.
- **Verification closes the loop.** The real runtime path is the source of truth.

<details>
<summary><strong>Deeper runtime principles</strong></summary>
<br/>

### Models reason; systems govern

Reasoning is useful for ambiguity, planning, interpretation, and choosing between valid paths. Deterministic operations should still live behind explicit tools, schemas, permission checks, and observable results.

### Failure should become state, not mystery

External APIs, databases, authentication, device operations, networks, and model providers will fail eventually. A good runtime turns those failures into named states that can be inspected, retried, recovered, or surfaced honestly.

### Product architecture is interaction design too

Loading, retries, stale state, permissions, partial success, recovery, and background execution all shape what the product feels like. Backend behavior is part of UX.

</details>

<br/>

## Toolchain

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,python,go,kotlin,react,nextjs,nodejs" alt="Languages and runtimes" />
</p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=postgres,prisma,supabase,vercel,git,github,linux" alt="Infrastructure and tooling" />
</p>

<details>
<summary><strong>How I think about the stack</strong></summary>
<br/>

**Interface**  
React · Next.js · Android UI · terminal surfaces · information architecture

**Runtime**  
TypeScript / Node · Python · Go · Kotlin · workers · command execution · provider orchestration

**State**  
PostgreSQL · Prisma · durable workflows · memory · checkpoints · event/evidence records

**Control**  
Authentication · permission boundaries · approvals · provider health · verification · recovery · auditability

</details>

<br/>

<p align="center">
  <img src="./assets/profile-build-loop.svg" width="100%" alt="Engineering build loop" />
</p>

## Build discipline

I prefer a smaller coherent system that survives real use over a larger system that only looks complete in screenshots.

1. **Define** what observable state actually counts as done.
2. **Map** ownership, dependencies, permissions, and failure modes.
3. **Build** the smallest complete end-to-end path.
4. **Observe** what the runtime really does.
5. **Verify** with fresh evidence instead of assumption.
6. **Recover** cleanly when the path breaks.
7. **Ship** when the real path survives contact with reality.

### Current vector

`products → agents → tools → controlled execution → evidence → reliable systems`

The direction is simple: **less demo behavior, more systems that can explain what happened and keep working when conditions stop being perfect.**

<p align="center">
  <img src="./assets/profile-divider.gif" width="100%" alt="Animated system signal" />
</p>

<div align="center">
  <strong>BUILD · OBSERVE · VERIFY · RECOVER · SHIP</strong><br/>
  <sub>Designed interfaces. Controlled capability. Recoverable state. Provable completion.</sub>
</div>

<br/>

<p align="center">
  <img src="./assets/profile-footer.gif" width="100%" alt="Animated profile footer" />
</p>

<!--
PUBLIC PROFILE NOTES
- Keep personal-identifying details off the public profile.
- Keep project-specific private architecture out of this README.
- No repository showcase section here; the profile should communicate engineering identity, not become a project index.
-->
