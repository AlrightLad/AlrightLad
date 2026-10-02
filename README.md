## Zach Boogher

Senior Infrastructure & Integrations Engineer — York, PA

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
- **Veeam v13 fleet upgrade** — convergent state machine for upgrading a Veeam
  B&R estate across mixed source builds: preflight gating, config backup,
  restore-point baselining, checksum-verified ISO staging, and deferred reboot.
  Detects Windows servicing corruption that blocks the upgrade path rather than
  failing silently mid-run.
- **On-call rotation scheduler** — rotation and coverage-pod scheduling in
  Windmill, writing live call-queue presence through the RingCentral API.
- **Dormant remote-access reconciliation** — cross-system identity matching
  between an RMM and a PSA to surface stale privileged accounts across
  several hundred tenants.
- Upstream contributions to
  [DTC-Inc/msp-script-library](https://github.com/DTC-Inc/msp-script-library/pulls?q=author%3AAlrightLad).

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/zachb1303/) · [zboogher@gmail.com](mailto:zboogher@gmail.com)

---

*"And let us not grow weary of doing good, for in due season we will reap,
if we do not give up."* — Galatians 6:9
