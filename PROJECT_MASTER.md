# Yazhan Downloads — Project Master

Last updated: 2026-08-23

## Project identity

- Project repository: `Yazhan-Labs/yazhan-downloads`
- Stable GitHub repository ID: `1329118286`
- Historical/superseded path: `balajibj/yazhan-downloads`
- Default branch: `main`
- Purpose: shared public binary downloads for Yazhan Labs products.
- Repository role: public distribution/release repository only. Do not commit product source, secrets, private keys, credentials, customer data, or owner-only material here.

## Current repository state

- Central adoption bootstrap completed and verified previously.
- Continuity closeout commit: `5cfb629158ec5e1c4a2ddd3eaf4ecc9ae9dd007f`.
- New release-handoff checkpoint: `74b542ed5f09f073d97572911a44455c032117a5`.
- `.github/workflows` is not established in this repository.
- This public repository remains excluded from the Yazhan Labs shared self-hosted runner pool.
- Existing public releases/tags/assets are protected release state and must not be deleted or replaced outside an exact approved release task.

## CENTRAL ADOPTION RECEIPT

- CENTRAL REPOSITORY: `Yazhan-Labs/Yazhan-Labs-Central`
- Central stable repository ID: `1331787973`
- Historical/superseded Central path: `balajibj/Yazhan-Labs-Central`
- Project identity resolution: `PROVEN FROM DURABLE/AUTHORITATIVE EVIDENCE`
- Owner repository confirmation: YES — 2026-08-23
- Central adopted: `1.11.6`
- Central ref: `main`
- Active manifest: Central `1.11.6`
- Full refresh completed because no prior valid adoption receipt existed.

Universal/core files read for adoption:

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

Platform/conditional review:

- `WINDOWS_DESKTOP_APP_STANDARD.md` — reviewed for Windows distributable context.
- `ORGANIZATION_SHARED_RUNNER_STANDARD.md` — reviewed; `yazhan-downloads` is explicitly excluded from shared self-hosted runners.
- `LOCAL_BUILD_ARTIFACT_STANDARD.md` — reviewed for artifact/distribution boundary.
- Android/Web/self-hosted runner/toolchain/runner-receipt/Central-Licensing standards are not operationally applicable to this repository's current execution state.

`CENTRAL COMPLIANCE: PASS`

Central is still `1.11.6` as of the current work-start check, matching this valid receipt. No repeat full refresh is required solely for this new release task.

## ACTIVE JOB

`Publish Yazhan Chat Cleaner 2.1.1 to Yazhan-Labs/yazhan-downloads using the established cross-repository release path.`

Owner supplied a release handoff on 2026-08-23 with explicit merge + public-release approval for this exact v2.1.1 scope.

Durable detailed handoff:

`docs/YAZHAN_CHAT_CLEANER_2.1.1_PUBLIC_RELEASE.md`

### Approved public release identity

- source repository: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source/tag commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- public repository: `Yazhan-Labs/yazhan-downloads`
- public release tag: `yazhan-chat-cleaner-v2.1.1`
- public release title: `Yazhan Chat Cleaner 2.1.1`
- assets: `YazhanChatCleaner-2.1.1-Setup.exe`, `SHA256SUMS.txt`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- standalone app SHA-256: `8f4b476cd3df1cd2787274a7d2f823e0b5d0824cdad8d12f729a220b41bef68d`
- release notes source: `RELEASE_NOTES.md` at source tag `v2.1.1`

### Verified source/tag release evidence

- `VERSION.txt` at `v2.1.1`: `2.1.1`
- tagged validation run: `32640759815`
- build-and-package job `97197383637`: `PASS`
- publish-public-release job `97197672129`: `FAIL` at publication only
- tagged publish checkout: `refs/tags/v2.1.1` at `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- exact validated local release handoff prepared before failure: `E:\YazhanLabs\Build_Artifacts\Yazhan-Chat-Cleaner\.release-handoff-32640759815`
- failed publish cleanup: skipped, so the handoff was preserved

### Established release architecture

The actual established path is cross-repository publication from the tagged `Yazhan-Labs/Yazhan-Chat-Cleaner` workflow using `scripts/publish-github-release.ps1`.

The publisher targets `Yazhan-Labs/yazhan-downloads`, validates release assets against `SHA256SUMS.txt`, is tag-ref gated, and uses the Chat Cleaner Actions repository secret `YAZHAN_DOWNLOADS_TOKEN` as `GH_TOKEN` for target GitHub Release API operations.

Do not create a second Downloads-owned release workflow merely to bypass this established architecture.

### Current block states

- Block 1 — current Central/Downloads continuity check: `VERIFIED / COMPLETE`
- Block 2 — source v2.1.1 tag/version/release-notes verification: `VERIFIED / COMPLETE`
- Block 3 — tagged run/build/hash/publication-failure verification: `VERIFIED / COMPLETE`
- Block 4 — release architecture + minimum token-permission audit: `VERIFIED / COMPLETE`
- Block 5 — configure `YAZHAN_DOWNLOADS_TOKEN`: `BLOCKED — OWNER-ONLY CREDENTIAL ACTION / TOOL CAPABILITY UNAVAILABLE`
- Block 6 — rerun failed publish job `97197672129`: `READY AFTER BLOCK 5`
- Block 7 — verify public release tag/title/assets/hash/URL and close continuity: `READY AFTER BLOCK 6`

PENDING JOB queue: `EMPTY`

Interrupted/suspended jobs: `NONE`

## Exact blocker

The established tagged publisher failed before any target release write because `GH_TOKEN` was empty:

`Repository secret YAZHAN_DOWNLOADS_TOKEN is required for tagged public releases.`

The connected GitHub capability available to this GPT exposes workflow retry/read and repository content operations, but does not expose GitHub Actions repository-secret creation/update or direct GitHub Release creation/upload.

Minimum safe credential:

- fine-grained credential limited to `Yazhan-Labs/yazhan-downloads`
- repository permission: `Contents: Read and write`
- stored only in `Yazhan-Labs/Yazhan-Chat-Cleaner` as Actions secret `YAZHAN_DOWNLOADS_TOKEN`
- never expose the value in chat, logs, issues, commits, files, workflow output, or release notes

## Exact next action

Owner securely configures `YAZHAN_DOWNLOADS_TOKEN` in `Yazhan-Labs/Yazhan-Chat-Cleaner` with target-only `Yazhan-Labs/yazhan-downloads` and `Contents: Read and write` permission.

Once that exact blocker is removed, the next safe action is to reconcile no equivalent publication has already completed, then re-run failed publish job ID `97197672129` from tagged run `32640759815` without rebuilding or retagging. Verify the rerun remains on `refs/tags/v2.1.1` / commit `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`, then verify the exact public release identity and installer SHA-256 before marking COMPLETE.

Do not change Chat Cleaner application code, Central Licensing, Stripe, USD 10/year pricing, customer/subscription/licence/device state, shared runner infrastructure, source tag `v2.1.1`, or unrelated public releases.
