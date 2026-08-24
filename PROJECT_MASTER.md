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

- Central repository: `Yazhan-Labs/Yazhan-Labs-Central`
- Central stable repository ID: `1331787973`
- Historical Central path: `balajibj/Yazhan-Labs-Central`
- Project identity resolution: `PROVEN FROM DURABLE/AUTHORITATIVE EVIDENCE`
- Central adopted: `1.11.7`
- Central ref: `main`
- Central commit checked: `b492f1eaa3754d7ee03d291b002ef2fced4ea92a`
- Active manifest: `1.11.7`
- Adoption date: `2026-08-24`
- Previous adopted version: `1.11.6`
- Refresh reason: Central changed before protected release execution.
- Result: `CENTRAL COMPLIANCE: PASS`

Universal/core files read for the 1.11.7 refresh:

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

Applicable conditional files read:

- `WINDOWS_DESKTOP_APP_STANDARD.md`
- `ORGANIZATION_SHARED_RUNNER_STANDARD.md`
- `LOCAL_BUILD_ARTIFACT_STANDARD.md`

Not operationally applicable to Downloads execution: Android, Web, Downloads self-hosted runner/toolchain/runner-receipt standards, and Central Licensing integration/automation standards.

1.11.7 reconciliation:

- owner-interruption/workflow-autonomy rules adopted;
- protected release approval gates preserved;
- public `yazhan-downloads` remains excluded from shared self-hosted runners;
- no unresolved owner-level conflict exists;
- fresh-instance recovery and continuous-execution behavior adopted.

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

Central 1.11.7 workflow bridge:

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

### Final block states

- Block 1 — Downloads-only publisher architecture: `COMPLETE`
- Block 2 — Actions read-only source artifact secret: `COMPLETE`
- Block 3 — Downloads publisher workflow: `COMPLETE`
- Block 4 — standard source handoff: `COMPLETE`
- Block 5 — Chat Cleaner 2.1.1 source handoff artifact: `VERIFIED / COMPLETE`
- Block 6 — fresh owner release approval: `COMPLETE`
- Block 7 — public release publication + byte verification: `VERIFIED / COMPLETE`

`ACTIVE JOB: NONE — YAZHAN CHAT CLEANER 2.1.1 PUBLIC RELEASE COMPLETE`

`PENDING JOB queue: EMPTY`

Interrupted/suspended jobs: `NONE`

## Exact next action

Await the next owner-approved Yazhan application release handoff. Source app GPTs should prepare the standard handoff artifact only. Downloads verifies the handoff, obtains the required fresh protected-release approval, dispatches through Controller issue #1, publishes with the Downloads repository token, and verifies the public bytes before closing the job.

## Protected release guardrails

- Do not invent release URLs, assets, checksums, versions, or publication state.
- Do not delete existing releases.
- Do not replace unrelated release assets.
- Do not move/reuse an existing release tag.
- Do not publish without verified provenance and fresh owner approval.
- Do not expose credentials.
- Do not touch product licensing, Stripe, pricing, customer/subscription/licence/device state, or shared runner infrastructure from this repository.
