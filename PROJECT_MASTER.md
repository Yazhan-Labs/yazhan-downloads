# Yazhan Downloads — Project Master

Last updated: 2026-08-23

## Project identity

- Project repository: `Yazhan-Labs/yazhan-downloads`
- Stable GitHub repository ID: `1329118286`
- Historical/superseded repository path: `balajibj/yazhan-downloads`
- Default branch: `main`
- Project baseline inspected before this continuity-only adoption commit: `7772547b6b2e6531bf203b7113050e4e827299b0`
- Baseline commit message: `Initial commit`
- Purpose: shared public binary downloads for Yazhan Labs products.
- Repository role: public distribution/release repository. It is not an application source repository and must not contain product source code, secrets, private keys, credentials, customer data, or owner-only material.

## Current GitHub state inspected

- Branches: `main` only.
- Baseline source content: `README.md` only, describing this repository as shared public binary downloads for Yazhan Labs products.
- `.github/workflows`: not present at the inspected baseline.
- Workflow runs for the inspected baseline commit: none.
- No runner/CI execution surface is currently established in this repository.
- Central adoption continuity commit read back and verified: `13a0767664b228d39871d22017678ed4c1e5c07d`.

Existing tags, GitHub Releases, and published customer-distribution assets are protected release state. This Central adoption/continuity update does not create, replace, republish, delete, or otherwise mutate any release/tag/asset.

## Repository transfer continuity

GitHub resolves both the historical path `balajibj/yazhan-downloads` and the current path `Yazhan-Labs/yazhan-downloads` to stable repository ID `1329118286`.

Result: this is the same repository continuity after transfer. Current-state references use `Yazhan-Labs/yazhan-downloads`; historical records may retain the old path as historical evidence.

## CENTRAL ADOPTION RECEIPT

### Repository and owner confirmation

- PROJECT REPOSITORY: `Yazhan-Labs/yazhan-downloads`
- CENTRAL REPOSITORY: `Yazhan-Labs/Yazhan-Labs-Central`
- Central stable GitHub repository ID: `1331787973`
- Historical/superseded Central path: `balajibj/Yazhan-Labs-Central`
- Project identity resolution method: `PROVEN FROM DURABLE/AUTHORITATIVE EVIDENCE`
- Owner repository-pair confirmation: YES — 2026-08-23. The owner-confirmed historical Central alias was reconciled to the current canonical Central path under the same stable repository identity.
- Central adoption/check date: 2026-08-23

### Central version/ref checked

- Central version adopted: `1.11.6`
- Central ref checked: `main`
- Latest Central commit observed during adoption: `194ca79df3524ab7b892db536ab2b97734df76ec`
- `STANDARD_VERSION` at current `main`: `1.11.6`
- Active standard manifest checked: `ACTIVE_STANDARD_MANIFEST.md`, Central `1.11.6`
- Active manifest blob SHA observed: `e3e968c63c09515ad61a35192f2fd6c49f688edf`
- No previous durable Central Adoption Receipt existed in this repository, so a full manifest-controlled refresh was performed.
- `CHANGELOG.md` was reviewed through the current lineage, including the current 1.11.x changes and the prior active-lineage summary back to Central 1.0.0.

### Universal/core Central files read

1. `STANDARD_VERSION`
2. `CHANGELOG.md`
3. `ACTIVE_STANDARD_MANIFEST.md`
4. `CURRENT_RUNNER_INFRASTRUCTURE_STATE.md`
5. `FRESH_INSTANCE_BOOTSTRAP_STANDARD.md`
6. `REPOSITORY_IDENTITY_TRANSFER_STANDARD.md`
7. `CONTINUOUS_EXECUTION_STANDARD.md`
8. `MANDATORY_GPT_WORK_GATE.md`
9. `GPT_COMPLIANCE_EVIDENCE_STANDARD.md`
10. `COMMON_PROJECT_STANDARD.md`
11. `UNIVERSAL_GITHUB_PROJECT_WORKFLOW_INSTRUCTIONS.md`
12. `GPT_WORKFLOW_BRIDGE_GUIDE.md`
13. `SEQUENTIAL_WORK_QUEUE_STANDARD.md`
14. `ACTIVE_JOB_MESSAGE_QUEUE_STANDARD.md`
15. `PROJECT_CONTINUITY_STANDARD.md`
16. `SECURITY_DATA_STANDARD.md`
17. `UI_UX_STANDARD.md`
18. `BRANDING_STANDARD.md`
19. `DEPENDENCY_RUNTIME_STANDARD.md`
20. `RELEASE_VERSIONING_STANDARD.md`
21. `LEGAL_HELP_ABOUT_STANDARD.md`

### Platform/conditional Central files reviewed

- `WINDOWS_DESKTOP_APP_STANDARD.md` — reviewed because this distribution repository currently serves Windows-software release use cases; the repository itself contains no Windows application source.
- `ORGANIZATION_SHARED_RUNNER_STANDARD.md` — applicable to repository ownership/routing reconciliation. Result: this public repository is explicitly excluded from the Yazhan Labs shared self-hosted runner pool.
- `LOCAL_BUILD_ARTIFACT_STANDARD.md` — reviewed for distribution/artifact boundary. Operational local self-hosted build retention is not established in this repository because it has no build workflow. Published GitHub Release assets are customer-distribution assets and are not routine Actions artifacts eligible for cleanup under that standard.

### Files/conditions not applicable to the current repository state

- `ANDROID_APP_STANDARD.md` — not an Android application source repository.
- `WEB_PROJECT_STANDARD.md` — not a web/web-service/web-UI source repository.
- `SELF_HOSTED_RUNNER_STANDARD.md` — no self-hosted workflow applies here; the public repository is explicitly excluded from the shared self-hosted runner trust boundary.
- `SHARED_HOST_TOOLCHAIN_STANDARD.md` — no shared-runner/toolchain execution applies here.
- `GPT_RUNNER_VERIFICATION_LOOP_STANDARD.md` — no project workflow/runner verification surface exists here.
- `GPT_VISIBLE_RUNNER_RESULT_RECEIPT_STANDARD.md` — no self-hosted runner result reconciliation applies here.
- `CENTRAL_LICENSING_INTEGRATION_STANDARD.md` — this distribution repository itself is not a Central Licensing consumer.
- `CENTRAL_LICENSING_AUTOMATION_STANDARD.md` — no Central Licensing production mutation/onboarding belongs to this repository.

### Project continuity/current-state files read

- `PROJECT_MASTER.md` — missing before this adoption; created by this continuity update and read back from GitHub.
- `README.md` — read and verified.
- `docs/DECISION_LOG.md` — not present.
- `docs/SESSION_LOG.md` — not present.
- `docs/BUILD_AND_RELEASE.md` — not present.
- `docs/FILE_AND_ASSET_MAP.md` — not present.
- Current repository metadata, branch list, baseline commit, baseline source diff, workflow-directory state, and baseline workflow-run state were inspected directly from GitHub.

### Conflicts, migrations, and owner decisions

- Repository owner/name transfer found: YES.
- Transfer continuity proof: PASS — historical and current paths resolve to the same stable repository ID.
- Central owner/name transfer found: YES.
- Central transfer continuity proof: PASS — historical and current paths resolve to the same stable repository ID.
- Missing durable project continuity found: YES — `PROJECT_MASTER.md` was absent and has now been created and verified.
- Shared-runner mismatch found: NO. Current Central explicitly excludes `Yazhan-Labs/yazhan-downloads` from the shared self-hosted runner pool.
- Product/source architecture conflict found: NO. The repository remains distribution-only.
- Release mutation required for Central adoption: NO.
- Owner decision required now: NONE.
- Protected release action approval: NOT GRANTED / NOT NEEDED for this documentation-only adoption. Any future release/tag/asset publication, replacement, deletion, or other protected release mutation requires the applicable fresh exact owner approval and verification gates.

### CENTRAL COMPLIANCE

`CENTRAL COMPLIANCE: PASS`

Basis: all manifest-required universal/core files were read; relevant platform/conditional rules were reviewed; current GitHub baseline was inspected; repository transfers were reconciled by stable ID; the public self-hosted-runner exclusion was preserved; no unresolved contradiction remains; and this durable adoption receipt is stored and verified in the project repository.

### Fresh-instance and continuous-execution adoption

- Fresh GPT recovery: adopt current durable GitHub/Central truth; do not ask the owner to repeat already-provable repository identity, runner exclusion, or unchanged project facts.
- Central unchanged + valid receipt: do not repeat a full Central refresh solely because the GPT instance changes.
- Continuous execution: no owner wake message is required while safe authorized work remains in the current turn.
- Runner READY-work scan: applicable whenever a future asynchronous runner/external block exists; currently no runner surface exists here.
- Queue auto-drain and urgent-job auto-resume: adopted.

## ACTIVE JOB / work blocks

ACTIVE JOB: `NONE — Central 1.11.6 full refresh + durable continuity bootstrap COMPLETE`

- Block 1 — repository identity/current GitHub baseline: `VERIFIED / COMPLETE`
- Block 2 — manifest-controlled Central 1.11.6 refresh: `VERIFIED / COMPLETE`
- Block 3 — transfer/runner/release-boundary reconciliation: `VERIFIED / COMPLETE`
- Block 4 — durable `PROJECT_MASTER.md` adoption receipt + GitHub read-back: `VERIFIED / COMPLETE`

PENDING JOB queue: `EMPTY`

Interrupted/suspended jobs: `NONE`

Runner state: `NOT APPLICABLE / EXCLUDED` — public `yazhan-downloads` must remain outside the Yazhan Labs shared self-hosted runner pool unless the owner separately approves a different trust model.

## Release/distribution guardrails

- Preserve existing public releases, tags, and customer-facing assets unless a future task explicitly targets them and all release/protected-action gates are satisfied.
- Do not invent download URLs, release assets, checksums, versions, or publication state.
- Before any future distribution change, inspect the actual current GitHub release/tag/asset state and the owning product project's verified release evidence.
- A green build or available installer does not by itself authorize publication.
- Final distributable filenames must preserve clear product + semantic-version identity where technically possible.
- Do not commit source code or secrets to this public distribution repository.

## Exact next action

No ACTIVE or PENDING project job remains. Await a specific owner-initiated distribution/release request. Before any future mutation, run the current Mandatory GPT Work Gate, synchronize this continuity with current GitHub, and verify the actual current release/tag/asset state relevant to that request. Do not mutate protected release state without the applicable fresh exact owner approval.
