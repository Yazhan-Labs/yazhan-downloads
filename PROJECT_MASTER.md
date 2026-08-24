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

## Central adoption

- CENTRAL REPOSITORY: `Yazhan-Labs/Yazhan-Labs-Central`
- Central stable repository ID: `1331787973`
- Central adopted: `1.11.6`
- Current Central check for this work: `1.11.6`
- Durable full adoption receipt was completed on 2026-08-23.
- Current status: `CENTRAL COMPLIANCE: PASS`
- No repeat full Central refresh is required while Central remains `1.11.6` and this receipt remains valid.

Universal/core adoption covered:

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

Relevant conditional review:

- `WINDOWS_DESKTOP_APP_STANDARD.md`
- `ORGANIZATION_SHARED_RUNNER_STANDARD.md`
- `LOCAL_BUILD_ARTIFACT_STANDARD.md`

This public repository remains excluded from the Yazhan Labs shared self-hosted runner pool.

## Owner release architecture decision — 2026-08-24

The owner explicitly chose a centralized release model.

Current rule:

- Source application repositories build and validate their software.
- Source application GPTs do NOT publish directly to `yazhan-downloads`.
- Source application GPTs provide a validated release artifact + release handoff.
- `Yazhan-Labs/yazhan-downloads` is the only public release publisher.
- Source app repositories do NOT need `YAZHAN_DOWNLOADS_TOKEN`.
- The previous Chat Cleaner cross-repository publisher architecture is historical/superseded for future publication.

## Credential model

Owner-confirmed on 2026-08-24:

- secret name: `YAZHAN_SOURCE_ARTIFACT_READ_TOKEN`
- stored in: `Yazhan-Labs/yazhan-downloads`
- scope: 9 selected Yazhan application repositories
- permission: `Actions: Read-only`
- expiration: 2026-11-22
- secret value was not exposed in chat

Purpose:

- read approved source Actions artifacts only
- no write permission to source application repositories

Public release publication uses the Downloads repository's own GitHub Actions `GITHUB_TOKEN` with `contents: write`.

## Downloads-owned publication workflow

Workflow:

`.github/workflows/publish-approved-release.yml`

Created and read back on 2026-08-24.

The workflow:

- runs on GitHub-hosted `ubuntu-latest`
- requires a manual approved release request
- requires fresh owner release approval marker
- verifies source repository/run/tag/commit provenance
- requires the source run to be successful
- downloads the exact named source artifact using the read-only source token
- requires `RELEASE_NOTES.md`
- requires `SHA256SUMS.txt`
- verifies every public asset present in the artifact against `SHA256SUMS.txt`
- verifies the approved primary asset SHA-256
- refuses to replace an existing public release
- refuses to reuse/move an existing public tag
- publishes using the Downloads repository's own `GITHUB_TOKEN`
- downloads the published assets again and verifies byte/hash equality

This workflow does not use the shared self-hosted Yazhan runner pool.

## Standard source handoff

Template:

`docs/RELEASE_HANDOFF_TEMPLATE.md`

Required handoff fields:

- source repository
- source version
- source tag
- source commit
- successful source workflow run ID
- exact source artifact name
- public release tag
- public release title
- primary asset filename
- primary asset SHA-256
- owner release approval state

Required source artifact contents:

- approved public release asset(s)
- `SHA256SUMS.txt`
- `RELEASE_NOTES.md`

## ACTIVE JOB

`Publish Yazhan Chat Cleaner 2.1.1 through the new Downloads-only release path.`

Approved identity from the owner-supplied handoff:

- source repository: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source/tag commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- public repository: `Yazhan-Labs/yazhan-downloads`
- public release tag: `yazhan-chat-cleaner-v2.1.1`
- public release title: `Yazhan Chat Cleaner 2.1.1`
- primary asset: `YazhanChatCleaner-2.1.1-Setup.exe`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- public assets expected: installer + `SHA256SUMS.txt`
- release notes source: `RELEASE_NOTES.md` at `v2.1.1`

Verified historical tagged run evidence:

- tagged run: `32640759815`
- source ref: `v2.1.1`
- source commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- build-and-package job: PASS
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- old direct publish job: FAIL because its old publishing token was absent
- tagged Actions artifact upload in that run: skipped
- overall historical run conclusion: failure because the old direct-publication job failed

### Current block states

- Block 1 — owner selects Downloads-only publisher architecture: `COMPLETE`
- Block 2 — create/save source artifact read-only secret: `OWNER-CONFIRMED COMPLETE`
- Block 3 — create Downloads-owned fail-closed publisher workflow: `VERIFIED / COMPLETE`
- Block 4 — create standard release handoff format: `VERIFIED / COMPLETE`
- Block 5 — obtain a successful Chat Cleaner v2.1.1 source handoff artifact at the same `v2.1.1` / commit: `BLOCKED — SOURCE APP HANDOFF REQUIRED`
- Block 6 — fresh owner approval immediately before public publication: `WAITING UNTIL BLOCK 5`
- Block 7 — publish + verify public release: `READY AFTER BLOCKS 5-6`

PENDING JOB queue: `EMPTY`

Interrupted/suspended jobs: `NONE`

## Exact next action

The Chat Cleaner project must create a successful handoff-only/tagged Actions run for the already-approved `v2.1.1` commit `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797` and upload one release artifact containing:

- `YazhanChatCleaner-2.1.1-Setup.exe`
- `SHA256SUMS.txt`
- `RELEASE_NOTES.md`

It must not rebuild to a different commit, retag `v2.1.1`, publish directly to Downloads, or receive a Downloads publishing token.

Once the source artifact/run handoff is available, Downloads verifies it, obtains fresh exact owner release approval, publishes, verifies the public bytes, and closes the ACTIVE JOB.

## Protected release guardrails

- Do not invent release URLs, assets, checksums, versions, or publication state.
- Do not delete existing releases.
- Do not replace unrelated release assets.
- Do not move or reuse an existing tag.
- Do not publish without exact verified source provenance and fresh owner approval.
- Do not expose credentials.
- Do not touch Chat Cleaner licensing, Central Licensing production data, Stripe, pricing, customers, subscriptions, licences, device bindings, or shared runner infrastructure.
