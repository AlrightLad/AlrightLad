## Zach Boogher

Infrastructure & Integrations Engineer — York, PA

I build the automation that keeps a multi-thousand-endpoint managed fleet
running: RMM tooling, PSA integrations, workflow orchestration, and the
server lifecycle work underneath it. Most of what I write exists because
something was being done by hand several hundred times a week.

### What I work on

**Automation & orchestration** — PowerShell at fleet scale against NinjaOne
RMM, Halo PSA integrations, and scheduled workflow orchestration in Windmill.
Idempotent, single-instance, transcript-logged, exit-code-correct.

**Windows infrastructure** — Hyper-V host builds and standards, Server
2016→2025 lifecycle and P2V migration, Active Directory upgrade paths,
Dell PowerEdge provisioning and bare-metal deployment pipelines.

**Backup & disaster recovery** — Veeam Backup & Replication design,
fleet-wide upgrade waves, and verified restore testing.

**Compliance-adjacent engineering** — building and documenting controls for
HIPAA-regulated and CMMC L2 / NIST 800-171 environments, where the evidence
trail matters as much as the implementation.

**Documentation** — I own the internal knowledge base as document controller.
An automation nobody can operate is a liability, not an asset.

### How I work

- Evidence before conclusions. Hypotheses get labeled as hypotheses and
  tested before anything is called a root cause.
- Every commit GPG-signed. Every PR through PSScriptAnalyzer and Pester
  before it is opened.
- Fix by class, not by instance.
- Placeholders and sanitized examples by default in anything reusable.

### Selected work

- **[msp-automation](https://github.com/AlrightLad/msp-automation)** — production
  PowerShell for managed Windows fleets. RMM-safe by construction: no interactive
  prompts, single-instance locking, transcript rotation, explicit exit codes.
  Sanitized from scripts running against a multi-thousand-endpoint fleet.
- **[Veeam v13 fleet upgrade](https://github.com/AlrightLad/msp-automation/tree/main/backup-veeam)** — convergent state machine for upgrading a Veeam
  B&R estate across mixed source builds: preflight gating, config backup,
  restore-point baselining, checksum-verified ISO staging, and deferred reboot.
  Detects Windows servicing corruption that blocks the upgrade path rather than
  failing silently mid-run.
- **[stale-access-audit](https://github.com/AlrightLad/stale-access-audit)** —
  dormant privileged-account reconciliation between an RMM and a PSA, joined on
  an organization-owned GUID pair instead of vendor ids. An evidence model that
  tells "no login observed" from "no evidence below a floor", and a feed walker
  that either proves continuity or says it could not.
- **[ringcentral-queue-presence](https://github.com/AlrightLad/ringcentral-queue-presence)** —
  a small client that makes exactly one member of a RingCentral call queue the
  enabled one and proves it did: every member written explicitly under the
  API's partial-update semantics, protected members never touched, one cached
  bearer, read-back verification that fails loudly. Pairs with the rotation
  scheduler reference implementation in msp-automation.
- Upstream contributions to
  [DTC-Inc/msp-script-library](https://github.com/DTC-Inc/msp-script-library/pulls?q=author%3AAlrightLad).

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/zachb1303/) · [zboogher@gmail.com](mailto:zboogher@gmail.com)

---

*"And let us not grow weary of doing good, for in due season we will reap,
if we do not give up."* — Galatians 6:9
