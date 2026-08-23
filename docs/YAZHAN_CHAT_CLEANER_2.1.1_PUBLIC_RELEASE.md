# Yazhan Chat Cleaner 2.1.1 — Public Release Handoff

Last updated: 2026-08-23

## Status

`STATUS: BLOCKED`

The public release is fully validated up to the target GitHub release write, but the established cross-repository publisher cannot execute because `YAZHAN_DOWNLOADS_TOKEN` is absent from `Yazhan-Labs/Yazhan-Chat-Cleaner`.

No public release write has been performed by the Yazhan Downloads GPT.

## Owner approval

The owner supplied the release handoff on 2026-08-23 with explicit approval for merge + public release of Yazhan Chat Cleaner v2.1.1.

Approved public release scope:

- source project: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- public release repository: `Yazhan-Labs/yazhan-downloads`
- public release tag: `yazhan-chat-cleaner-v2.1.1`
- public release title: `Yazhan Chat Cleaner 2.1.1`
- assets:
  - `YazhanChatCleaner-2.1.1-Setup.exe`
  - `SHA256SUMS.txt`

Protected scope explicitly excludes changes to Chat Cleaner application code, Central Licensing, Stripe, pricing, customer data, licences, device bindings, shared runner infrastructure, and unrelated public releases.

## Proven source/tag provenance

- `VERSION.txt` at `v2.1.1`: `2.1.1`
- tagged release-validation run: `32640759815`
- ref: `refs/tags/v2.1.1`
- build-and-package job ID: `97197383637` — PASS
- publish-public-release job ID: `97197672129` — FAIL only at target release publication
- tag/checkout commit observed in the tagged publish job: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`

Validated hashes from the exact tagged run:

- standalone app SHA-256: `8f4b476cd3df1cd2787274a7d2f823e0b5d0824cdad8d12f729a220b41bef68d`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`
- installer filename: `YazhanChatCleaner-2.1.1-Setup.exe`

The tagged build job retained the latest verified build under the approved project artifact area and the publish job successfully prepared the exact local release handoff before failing.

Run-specific preserved release handoff reported by the failed tagged publish job:

`E:\YazhanLabs\Build_Artifacts\Yazhan-Chat-Cleaner\.release-handoff-32640759815`

The cleanup step was skipped after publication failure, preserving the handoff for recovery.

## Established release architecture

The established architecture is **cross-repository publication from the tagged Yazhan Chat Cleaner workflow**.

The tagged publish job executes:

- source publisher: `scripts/publish-github-release.ps1`
- target repository: `Yazhan-Labs/yazhan-downloads`
- release tag: `yazhan-chat-cleaner-v<version>`
- release title: `Yazhan Chat Cleaner <version>`
- notes source: `RELEASE_NOTES.md`
- release assets: installer + `SHA256SUMS.txt`
- credential input: Chat Cleaner repository secret `YAZHAN_DOWNLOADS_TOKEN`, exposed to the publisher only as `GH_TOKEN`

The publisher validates every non-checksum asset against `SHA256SUMS.txt` before performing a GitHub API write. It is tag-ref gated and creates the target release when absent. If a same-name asset already exists on that exact release, it removes that asset before uploading the validated replacement.

Yazhan Downloads itself currently has no `.github/workflows` release publisher and remains excluded from the shared self-hosted runner pool. Do not invent a second Downloads-owned publishing mechanism while the established cross-repo path exists.

## Exact blocker

Tagged run `32640759815`, publish job `97197672129`, failed at:

`Publish validated installer to public Yazhan downloads repo`

Exact error:

`Repository secret YAZHAN_DOWNLOADS_TOKEN is required for tagged public releases.`

The job log showed `GH_TOKEN` empty. Failure occurred before the GitHub release API write.

## Minimum required credential

Configure a fine-grained GitHub credential that can act only on:

`Yazhan-Labs/yazhan-downloads`

Minimum repository permission required by the established publisher:

- `Contents: Read and write`

Metadata read access is implicit/required by GitHub. No permission to Chat Cleaner source contents is required for this cross-repo token because source checkout uses the workflow's separate normal `GITHUB_TOKEN`.

Store the credential only as this Actions repository secret in `Yazhan-Labs/Yazhan-Chat-Cleaner`:

`YAZHAN_DOWNLOADS_TOKEN`

Never record or expose the secret value in issues, logs, commits, continuity files, chat, workflow output, or release notes.

## Exact retry path after secret configuration

1. Confirm `YAZHAN_DOWNLOADS_TOKEN` exists in `Yazhan-Labs/Yazhan-Chat-Cleaner` with the target-only permission above.
2. Reconcile that no equivalent publication has already completed for `yazhan-chat-cleaner-v2.1.1`.
3. Re-run failed publish job ID `97197672129` from run `32640759815` rather than rebuilding or retagging.
4. Verify the rerun remains on `refs/tags/v2.1.1` / commit `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`.
5. Verify public release tag/title exactly match the approved values.
6. Verify assets are exactly `YazhanChatCleaner-2.1.1-Setup.exe` and `SHA256SUMS.txt`.
7. Verify the published installer SHA-256 is exactly `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`.
8. Verify release notes match `RELEASE_NOTES.md` at source tag `v2.1.1`.
9. Record the final GitHub release URL and public-release proof here and in `PROJECT_MASTER.md`.

Do not move or recreate source tag `v2.1.1`, do not rebuild merely to bypass the missing credential, and do not weaken tagged release validation.

## Exact next action

Owner-only credential action required: securely create/configure `YAZHAN_DOWNLOADS_TOKEN` in `Yazhan-Labs/Yazhan-Chat-Cleaner` with target repository `Yazhan-Labs/yazhan-downloads` and minimum `Contents: Read and write` permission. The connected GitHub capability available to this GPT does not expose Actions-secret creation/update.

After that exact blocker is removed, the Downloads GPT should immediately re-run failed job `97197672129`, verify the public release, update continuity, and report final PASS/COMPLETE.
