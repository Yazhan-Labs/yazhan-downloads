# Yazhan Downloads — Project Master

Last updated: 2026-08-24

## Project identity

- Project repository: `Yazhan-Labs/yazhan-downloads`
- Stable GitHub repository ID: `1329118286`
- Historical/superseded path: `balajibj/yazhan-downloads`
- Default branch: `main`
- Purpose: shared public binary downloads for Yazhan Labs products.
- Repository role: public distribution/release repository only.
- Do not commit product source, secrets, private keys, credentials, customer data, or owner-only material here.

## CENTRAL ADOPTION RECEIPT — 1.11.7

- Project repository: `Yazhan-Labs/yazhan-downloads`
- Project identity resolution: `PROVEN FROM DURABLE/AUTHORITATIVE EVIDENCE`
- Central repository: `Yazhan-Labs/Yazhan-Labs-Central`
- Central stable repository ID: `1331787973`
- Historical Central path: `balajibj/Yazhan-Labs-Central`
- Central adopted: `1.11.7`
- Central ref: `main`
- Central commit checked: `b492f1eaa3754d7ee03d291b002ef2fced4ea92a`
- Active manifest: `1.11.7`
- Adoption date: `2026-08-24`
- Previous adopted version: `1.11.6`
- Refresh reason: Central version changed from `1.11.6` to `1.11.7` before protected release execution.
- Project main state inspected before receipt update: `2590e4befd09eaeb9035c324bcaa4443b4609e4c`
- Result: `CENTRAL COMPLIANCE: PASS`

Universal/core files read for this refresh:

1. `STANDARD_VERSION`
2. `CHANGELOG.md` — 1.11.6 -> 1.11.7 delta
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

Applicable platform/conditional files read:

- `WINDOWS_DESKTOP_APP_STANDARD.md` — applicable to the Windows distributable context.
- `ORGANIZATION_SHARED_RUNNER_STANDARD.md` — applicable to confirm the public Downloads repository remains excluded from shared self-hosted runners.
- `LOCAL_BUILD_ARTIFACT_STANDARD.md` — applicable to the source-artifact/distribution boundary and narrow handoff exception.

Not operationally applicable to this Downloads repository execution:

- `ANDROID_APP_STANDARD.md` — no Android product implementation here.
- `WEB_PROJECT_STANDARD.md` — no web application implementation here.
- `SELF_HOSTED_RUNNER_STANDARD.md` — Downloads publication uses GitHub-hosted `ubuntu-latest`; this public repository remains excluded from the shared self-hosted pool.
- `SHARED_HOST_TOOLCHAIN_STANDARD.md` — no Downloads self-hosted toolchain execution.
- `GPT_RUNNER_VERIFICATION_LOOP_STANDARD.md` — no Downloads self-hosted verification loop.
- `GPT_VISIBLE_RUNNER_RESULT_RECEIPT_STANDARD.md` — no Downloads self-hosted runner receipt surface.
- `CENTRAL_LICENSING_INTEGRATION_STANDARD.md` and `CENTRAL_LICENSING_AUTOMATION_STANDARD.md` — licensing is not owned or modified by this distribution repository.

1.11.7 reconciliation:

- New owner-interruption/workflow-autonomy rules adopted.
- Direct connector workflow dispatch is unavailable; the repository GPT Workflow Controller + `/yl-run` bridge is the required dispatch path when present.
- Protected release approval requirements are unchanged.
- Owner supplied fresh exact approval on 2026-08-24 for the Chat Cleaner 2.1.1 public release.
- No unresolved owner-level conflict exists.
- Fresh-instance recovery rule adopted: no redundant repository confirmation, broad re-audit, reinstall or unchanged validation solely because a GPT instance changes.
- Continuous-execution rule adopted: no owner wake message is required; READY-work scan, queue auto-drain and protected-operation follow-through remain active.
- Public `Yazhan-Labs/yazhan-downloads` remains excluded from `YL-ORG-01`/`YL-ORG-02`/`YL-ORG-03` shared self-hosted runner access.

## Owner release architecture decision — 2026-08-24

The owner explicitly chose a centralized release model:

- Source application repositories build and validate their software.
- Source application GPTs do NOT publish directly to `yazhan-downloads`.
- Source application GPTs provide a validated release artifact + release handoff.
- `Yazhan-Labs/yazhan-downloads` is the only public release publisher.
- Source app repositories do NOT need `YAZHAN_DOWNLOADS_TOKEN`.
- The previous Chat Cleaner cross-repository direct publisher architecture is historical/superseded for future publication.

## Credential model

Owner-confirmed on 2026-08-24:

- secret name: `YAZHAN_SOURCE_ARTIFACT_READ_TOKEN`
- stored in: `Yazhan-Labs/yazhan-downloads`
- scope: 9 selected Yazhan application repositories
- permission: `Actions: Read-only`
- expiration: `2026-11-22`
- secret value was not exposed in chat

Purpose:

- read approved source Actions artifacts only
- no write permission to source application repositories

Public release publication uses the Downloads repository's own GitHub Actions `GITHUB_TOKEN` with `contents: write`.

## Downloads-owned publication workflow

Workflow:

`.github/workflows/publish-approved-release.yml`

Current workflow provenance-fix commit:

`142949dccb5111aac60b49ae9477211dfadfe56f`

The workflow:

- runs on GitHub-hosted `ubuntu-latest`
- requires a manual approved release request
- requires fresh owner release approval marker
- verifies the source handoff run is successful and belongs to the stated source repository
- independently verifies the source tag resolves to the approved source commit
- downloads the exact named source artifact using the read-only source token
- requires `RELEASE_NOTES.md`
- requires `SHA256SUMS.txt`
- verifies every public asset against `SHA256SUMS.txt`
- verifies the approved primary asset SHA-256
- refuses to replace an existing public release
- refuses to reuse/move an existing public tag
- publishes using the Downloads repository's own `GITHUB_TOKEN`
- downloads the published assets again and verifies byte/hash equality

## Standard source handoff

Template:

`docs/RELEASE_HANDOFF_TEMPLATE.md`

Required source artifact contents:

- approved public release asset(s)
- `SHA256SUMS.txt`
- `RELEASE_NOTES.md`

## ACTIVE JOB

`Publish Yazhan Chat Cleaner 2.1.1 through the Downloads-only release path.`

Approved public release identity:

- source repository: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source/tag commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- public repository: `Yazhan-Labs/yazhan-downloads`
- public release tag: `yazhan-chat-cleaner-v2.1.1`
- public release title: `Yazhan Chat Cleaner 2.1.1`
- primary asset: `YazhanChatCleaner-2.1.1-Setup.exe`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- public assets expected: installer + `SHA256SUMS.txt`
- release notes: `RELEASE_NOTES.md` from the approved source handoff

Verified original tagged build evidence:

- tagged validation run: `32640759815`
- source ref: `v2.1.1`
- source commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- build-and-package job: `PASS`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- old direct source-owned publish job failed because its old publishing token was absent; it did not complete public publication

Verified centralized source handoff evidence:

- handoff run: `32701462168`
- handoff job: `create-handoff-artifact` — `PASS`
- artifact name: `Yazhan-Chat-Cleaner-v2.1.1-release-handoff`
- artifact ID: `9510705106`
- artifact size: `63308039` bytes
- artifact ZIP SHA-256: `937b234cc8a94746d0943941f8f64a24ff1e1d08ba6ca4dd71f9b09fb61d4e5f`
- artifact expires: `2026-09-23T07:26:24Z`
- artifact contains exactly:
  - `YazhanChatCleaner-2.1.1-Setup.exe`
  - `SHA256SUMS.txt`
  - `RELEASE_NOTES.md`
- installer SHA-256 independently rechecked: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- handoff workflow checked out exact approved source commit and verified `v2.1.1` resolves to that exact commit before staging the retained tagged build
- no Downloads publication was attempted by the source handoff run

### Current block states

- Block 1 — owner selects Downloads-only publisher architecture: `COMPLETE`
- Block 2 — create/save source artifact read-only secret: `OWNER-CONFIRMED COMPLETE`
- Block 3 — create Downloads-owned fail-closed publisher workflow: `VERIFIED / COMPLETE`
- Block 4 — create standard release handoff format: `VERIFIED / COMPLETE`
- Block 5 — obtain and independently verify Chat Cleaner v2.1.1 source handoff artifact: `VERIFIED / COMPLETE`
- Block 6 — fresh owner approval immediately before public publication: `COMPLETE — APPROVED 2026-08-24`
- Block 7 — publish + verify public release: `READY — DISPATCH THROUGH GPT WORKFLOW CONTROLLER`

PENDING JOB queue: `EMPTY`

Interrupted/suspended jobs: `NONE`

## Exact next action

Reconcile the Downloads GPT Workflow Controller and any equivalent prior dispatch. If no equivalent publication is already in progress/completed, post the approved `/yl-run publish-approved-release.yml` command on the controller issue with the exact verified handoff inputs. Reconcile the resulting run, verify release tag/title/assets/public byte hashes, record the public release URL, then close this ACTIVE JOB.

## Protected release guardrails

- Do not invent release URLs, assets, checksums, versions, or publication state.
- Do not delete existing releases.
- Do not replace unrelated release assets.
- Do not move or reuse an existing tag.
- Do not publish without exact verified source provenance and fresh owner approval.
- Do not expose credentials.
- Do not touch Chat Cleaner licensing, Central Licensing production data, Stripe, pricing, customers, subscriptions, licences, device bindings, or shared runner infrastructure.
