# Yazhan Downloads — Project Master

Last updated: 2026-08-28

## Project identity

- Project repository: `Yazhan-Labs/yazhan-downloads`
- Stable GitHub repository ID: `1329118286`
- Historical/superseded path: `balajibj/yazhan-downloads`
- Default branch: `main`
- Purpose: shared public binary downloads for Yazhan Labs products.
- Repository role: public distribution/release repository only.
- Do not commit product source, secrets, private keys, credentials, customer data, or owner-only material here.

## CENTRAL ADOPTION RECEIPT — 1.13.3

- Central repository: `Yazhan-Labs/Yazhan-Labs-Central`
- Central stable repository ID: `1331787973`
- Historical Central path: `balajibj/Yazhan-Labs-Central`
- Owner repository confirmation: `APPROVED 2026-08-26`; owner selected current canonical Central path after GitHub proved the historical path redirects to the same stable repository ID.
- Project identity resolution: `OWNER CONFIRMED AFTER GENUINE AMBIGUITY`, with current project and Central stable repository IDs verified from GitHub.
- Central adopted: `1.13.3`
- Previous adopted version: `1.11.7`
- Central ref: `main`
- Central commit checked: `dfe0a31d7b43d7641e29eab6d6ee8a0e3c04a04f`
- Active manifest checked: `ACTIVE_STANDARD_MANIFEST.md` for Central `1.13.3`
- Adoption/check date: `2026-08-26`
- Refresh reason: Central changed from `1.11.7` to `1.13.3`.
- Result: `CENTRAL COMPLIANCE: PASS`

Universal/core files read for the 1.13.3 refresh:

1. `STANDARD_VERSION`
2. `CHANGELOG.md` — delta from the previously adopted `1.11.7` through current `1.13.3`
3. `ACTIVE_STANDARD_MANIFEST.md`
4. `HYBRID_EXECUTION_RELIABILITY_STANDARD.md`
5. `LOCAL_PC_BRIDGE_STANDARD.md`
6. `FRESH_INSTANCE_BOOTSTRAP_STANDARD.md`
7. `REPOSITORY_IDENTITY_TRANSFER_STANDARD.md`
8. `CONTINUOUS_EXECUTION_STANDARD.md`
9. `MANDATORY_GPT_WORK_GATE.md`
10. `GPT_COMPLIANCE_EVIDENCE_STANDARD.md`
11. `COMMON_PROJECT_STANDARD.md`
12. `UNIVERSAL_GITHUB_PROJECT_WORKFLOW_INSTRUCTIONS.md`
13. `SEQUENTIAL_WORK_QUEUE_STANDARD.md`
14. `ACTIVE_JOB_MESSAGE_QUEUE_STANDARD.md`
15. `PROJECT_CONTINUITY_STANDARD.md`
16. `SECURITY_DATA_STANDARD.md`
17. `UI_UX_STANDARD.md`
18. `BRANDING_STANDARD.md`
19. `DEPENDENCY_RUNTIME_STANDARD.md`
20. `RELEASE_VERSIONING_STANDARD.md`
21. `LEGAL_HELP_ABOUT_STANDARD.md`

Applicable/relevant platform and conditional files read:

- `WINDOWS_DESKTOP_APP_STANDARD.md` — read because Downloads distributes verified Windows installer assets; it does not authorize changes to source-application architecture.
- `GPT_WORKFLOW_BRIDGE_GUIDE.md` — applicable because the Downloads publisher is a `workflow_dispatch` workflow and the repository has the GPT Workflow Controller bridge.
- `CURRENT_RUNNER_INFRASTRUCTURE_STATE.md` — read to reconcile the current trust/routing boundary; it explicitly excludes public `Yazhan-Labs/yazhan-downloads` from the Organization self-hosted runner pool.
- `LOCAL_BUILD_ARTIFACT_STANDARD.md` — read/reconciled because prior adoption treated it as relevant; operationally Downloads does not locally build/package source products, so source-app retained-build behavior remains owned by source projects and Downloads receives approved handoff artifacts.

Not operationally applicable to this repository at this adoption:

- `ANDROID_APP_STANDARD.md` — Downloads is not an Android application project.
- `WEB_PROJECT_STANDARD.md` — Downloads is not a web application/service/UI project; it is a GitHub public release repository.
- `ORGANIZATION_SHARED_RUNNER_STANDARD.md`, `SELF_HOSTED_RUNNER_STANDARD.md`, runner receipt/verification standards, and `SHARED_HOST_TOOLCHAIN_STANDARD.md` — Downloads is public and explicitly excluded from the Organization self-hosted runner trust boundary; current workflows use `ubuntu-latest`.
- `LOCAL_PC_MAINTENANCE_STANDARD.md` — no elevated owner-PC maintenance is part of current Downloads work.
- `CENTRAL_LICENSING_INTEGRATION_STANDARD.md` and `CENTRAL_LICENSING_AUTOMATION_STANDARD.md` — Downloads is not a Central Licensing integration owner and must not mutate licensing/payment/customer state.

Project continuity and current GitHub state inspected:

- `PROJECT_MASTER.md`
- `docs/RELEASE_HANDOFF_TEMPLATE.md`
- `docs/YAZHAN_CHAT_CLEANER_2.1.1_PUBLIC_RELEASE.md`
- `.github/workflows/gpt-workflow-bridge.yml`
- `.github/workflows/publish-approved-release.yml`
- repository controller issue `#1 — GPT Workflow Controller — GPTs dispatch here`
- current public release `yazhan-chat-cleaner-v2.1.1`
- successful Downloads publication run `32708070651`
- project branch: `main`
- project commit inspected before adoption mutation: `3df79fba5671ba2c1228cc19dec3bf39ca8232d5`
- Central-adoption checkpoint commit: `9ed3b153332dcffe804e5752c0b53582125deb9f`
- continuity-repair commit inspected: `b06f40569208c598e6f63f728ca62c46e500f5f3`

1.13.3 reconciliation / migrations found:

- Adopted `FASTEST RELIABLE AVAILABLE PATH`; no fixed Bridge-first or runner-first preference.
- Adopted Local PC Bridge controller issue `#67` and Central infrastructure incident issue `#75` with report-and-continue behavior.
- Independent safe blocks may use Bridge and eligible runners concurrently without equivalent duplicate work, but Downloads itself remains excluded from the Organization self-hosted runner pool.
- Downloads workflows remain on `ubuntu-latest`; no runner migration is required or authorized.
- Existing protected public-release gate remains unchanged: fresh exact owner release approval is still required before publication.
- Existing centralized release architecture remains: source application repositories prepare/validate one handoff artifact; `Yazhan-Labs/yazhan-downloads` is the only public publisher.
- The stale continuity contradiction in `docs/YAZHAN_CHAT_CLEANER_2.1.1_PUBLIC_RELEASE.md` was repaired on 2026-08-26. It now records the proven completed Downloads-owned publication and explicitly marks the older blocked cross-repository token path as historical/superseded.
- Central changelog currently jumps from `1.11.7` to `1.13.0` while `1.13.0` references the superseded `1.12.0` Bridge-first policy. Current `1.13.3` manifest/gate/standards explicitly supersede that historical policy, so no owner decision is required.
- Owner decisions required after canonical Central selection: `NONE`.

Fresh-instance / execution behavior adopted:

- Proven repository identity is reused without redundant owner reconfirmation.
- Unchanged valid Central adoption does not trigger another full refresh.
- No broad PC/runner/toolchain audit, reinstall, or unchanged verification is repeated solely because a GPT instance changed.
- Async work triggers READY-work scan; no owner wake message is required to continue already-authorized work.
- Queue auto-drain and urgent-job auto-resume behavior are adopted.

### Central refresh block map — COMPLETE

1. Repository identity + current GitHub state — `VERIFIED / COMPLETE`
2. Full manifest-controlled Central 1.13.3 refresh — `VERIFIED / COMPLETE`
3. Workflow/controller/public-release proof reconciliation — `VERIFIED / COMPLETE`
4. Durable continuity repair (`PROJECT_MASTER.md` + stale Chat Cleaner release continuity) — `VERIFIED / COMPLETE`
5. Post-write GitHub re-read + final compliance closeout — `VERIFIED / COMPLETE`

`ACTIVE JOB: NONE — CENTRAL 1.13.3 REFRESH + CONTINUITY RECONCILIATION COMPLETE`

`PENDING JOB queue: EMPTY`

Interrupted/suspended jobs: `NONE`

Current execution channels:

- GitHub connector: available for repository read/write and continuity work.
- Repository GPT Workflow Controller issue `#1`: verified open and available for future approved `workflow_dispatch` release execution.
- Local PC Bridge: Central-approved complementary channel when technically relevant.
- Organization self-hosted runners: not available to this public repository by policy; Downloads workflows currently use GitHub-hosted `ubuntu-latest`.
- Outstanding Bridge jobs: `NONE`.
- Outstanding Downloads workflow/run jobs: `NONE`.

## Exact next action

Await the next owner-approved Yazhan application release handoff. Source app GPTs prepare the standard verified handoff artifact only. Downloads verifies the handoff, obtains fresh exact protected-release approval, dispatches the Downloads publisher through the approved workflow/controller path, publishes with the Downloads repository token, and verifies the public bytes before recording completion.

## Centralized release architecture

Owner decision on 2026-08-24:

- Source application repositories build and validate only.
- Source application GPTs do NOT publish directly to `yazhan-downloads`.
- Source apps produce one verified Actions handoff artifact.
- `Yazhan-Labs/yazhan-downloads` is the only public release publisher.
- Source app repositories do NOT need a Downloads publishing token.

Source-reader credential:

- secret: `YAZHAN_SOURCE_ARTIFACT_READ_TOKEN`
- stored only in: `Yazhan-Labs/yazhan-downloads`
- scope: 9 selected Yazhan app repositories
- permission: `Actions: Read-only`
- expiration: `2026-11-22`
- secret value was never exposed in chat or repository content

Downloads publishing uses its own workflow `GITHUB_TOKEN` with `contents: write`.

## Release control surface

Downloads publisher:

`.github/workflows/publish-approved-release.yml`

Current workflow commit before successful release:

`0060725fb0ad4f6baf6e4c8e0e147191b9a99158`

GPT workflow bridge:

`.github/workflows/gpt-workflow-bridge.yml`

Bridge creation commit:

`c7fa1b6014047803601409da9a6d586fdb243320`

Controller issue:

`#1 — GPT Workflow Controller — GPTs dispatch here`

Standard handoff template:

`docs/RELEASE_HANDOFF_TEMPLATE.md`

Template standardization commit:

`3ca1f5455437dd9847a44358cd284084cce17062`

## Yazhan Chat Cleaner 2.1.1 — PUBLIC RELEASE COMPLETE

Source provenance:

- source repository: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source/tag commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- original tagged validation run: `32640759815`
- original build-and-package: `PASS`

Centralized handoff:

- handoff run: `32701462168`
- handoff job: `create-handoff-artifact` — `PASS`
- artifact: `Yazhan-Chat-Cleaner-v2.1.1-release-handoff`
- artifact ID: `9510705106`
- artifact size: `63308039` bytes
- artifact ZIP SHA-256: `937b234cc8a94746d0943941f8f64a24ff1e1d08ba6ca4dd71f9b09fb61d4e5f`
- artifact files:
  - `YazhanChatCleaner-2.1.1-Setup.exe`
  - `SHA256SUMS.txt`
  - `RELEASE_NOTES.md`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`

Protected release approval:

- fresh exact owner approval received: `2026-08-24`
- approved command: publish Chat Cleaner `2.1.1`

Downloads release execution:

- run `32707533358`: failed safely before publication because Actions-only reader could not use a Contents endpoint; no public write occurred.
- run `32707747627`: failed safely before publication because GitHub job logs required escape-sequence handling; no public write occurred.
- run `32707876500`: failed safely before publication because Windows CRLF checksum lines required normalization; no public write occurred.
- workflow corrected without widening the source-reader credential beyond `Actions: Read-only`.
- successful publication run: `32708070651`
- successful publication job: `97373363003`
- final job conclusion: `SUCCESS`

Public release:

- repository: `Yazhan-Labs/yazhan-downloads`
- tag: `yazhan-chat-cleaner-v2.1.1`
- title: `Yazhan Chat Cleaner 2.1.1`
- draft: `false`
- prerelease: `false`
- public URL: `https://github.com/Yazhan-Labs/yazhan-downloads/releases/tag/yazhan-chat-cleaner-v2.1.1`
- published assets:
  - `YazhanChatCleaner-2.1.1-Setup.exe`
  - `SHA256SUMS.txt`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- workflow downloaded the published assets again and verified byte/hash equality after publication.

### Final release block states

- Block 1 — Downloads-only publisher architecture: `COMPLETE`
- Block 2 — Actions read-only source artifact secret: `COMPLETE`
- Block 3 — Downloads publisher workflow: `COMPLETE`
- Block 4 — standard source handoff: `COMPLETE`
- Block 5 — Chat Cleaner 2.1.1 source handoff artifact: `VERIFIED / COMPLETE`
- Block 6 — fresh owner release approval: `COMPLETE`
- Block 7 — public release publication + byte verification: `VERIFIED / COMPLETE`

## Protected release guardrails

- Do not invent release URLs, assets, checksums, versions, or publication state.
- Do not delete existing releases unless the owner gives fresh explicit approval for an exact superseded-release retirement. Owner-approved exception on 2026-08-28 retired Chat Cleaner 2.0.0 release/tag while retaining Chat Cleaner 2.1.1 and WhatsApp Approved Batch Assistant 3.0.1.
- Do not replace unrelated release assets.
- Do not move/reuse an existing release tag.
- Do not publish without verified provenance and fresh owner approval.
- Do not expose credentials.
- Do not touch product licensing, Stripe, pricing, customer/subscription/licence/device state, or shared runner infrastructure from this repository.


## Superseded public release retirement — 2026-08-28

- Owner instruction: keep only the latest uploaded public version of WhatsApp Approved Batch Assistant and Yazhan Chat Cleaner so superseded installers cannot be downloaded.
- Fresh destructive approval: received in the project conversation on 2026-08-28.
- Scope resolved from current GitHub truth: no older WABAA public release existed; Chat Cleaner 2.0.0 was the only superseded public release.
- Deleted public release: `chat-cleaner-v2.0.0` (Yazhan Chat Cleaner v2.0.0).
- Deleted Git tag: `chat-cleaner-v2.0.0`.
- Retained current Chat Cleaner release: `yazhan-chat-cleaner-v2.1.1`.
- Retained current WABAA release: `yazhan-whatsapp-approved-batch-assistant-v3.0.1`.
- Result: `SUPERSEDED RELEASE RETIREMENT: PASS`.
- This is a specific owner-approved exception to the normal no-release-deletion guardrail; it is not blanket permission for future destructive release changes.
