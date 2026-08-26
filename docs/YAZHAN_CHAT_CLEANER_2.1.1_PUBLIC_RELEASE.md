# Yazhan Chat Cleaner 2.1.1 — Public Release

Last updated: 2026-08-26

## Status

`STATUS: VERIFIED / COMPLETE`

Yazhan Chat Cleaner `2.1.1` was successfully published through the current Downloads-owned release architecture on 2026-08-24.

The earlier 2026-08-23 `BLOCKED` state and cross-repository `YAZHAN_DOWNLOADS_TOKEN` publication path recorded in this file are historical and superseded. They are not the current release architecture and must not be used as a retry path.

## Proven source/tag provenance

- source repository: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source/tag commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- original tagged validation run: `32640759815`
- original build-and-package result: `PASS`
- installer filename: `YazhanChatCleaner-2.1.1-Setup.exe`
- installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`

## Current centralized handoff architecture

The current architecture, established on 2026-08-24, is:

- source application repositories build and validate only;
- source application GPTs do not publish directly to `Yazhan-Labs/yazhan-downloads`;
- source applications produce one verified GitHub Actions handoff artifact;
- `Yazhan-Labs/yazhan-downloads` is the only public publisher;
- source application repositories do not need a Downloads publishing token.

Standard source handoff workflow:

`.github/workflows/release-handoff-artifact.yml`

Verified Chat Cleaner 2.1.1 handoff:

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

## Downloads-owned publisher

Publisher workflow:

`.github/workflows/publish-approved-release.yml`

GPT workflow bridge:

`.github/workflows/gpt-workflow-bridge.yml`

Controller issue:

`#1 — GPT Workflow Controller — GPTs dispatch here`

Credential model:

- source handoff retrieval uses `YAZHAN_SOURCE_ARTIFACT_READ_TOKEN` stored only in `Yazhan-Labs/yazhan-downloads`;
- the source-reader credential is scoped to approved source repositories with `Actions: Read-only`;
- source application repositories do not receive a Downloads publishing credential;
- final publication uses the Downloads workflow's own `GITHUB_TOKEN` with `contents: write`.

No secret value is stored in this document.

## Protected release approval

Fresh exact owner approval for this public release was received on `2026-08-24`.

Approved public release scope:

- source project: `Yazhan-Labs/Yazhan-Chat-Cleaner`
- source tag: `v2.1.1`
- source commit: `5d7d84bc0551a97a1bc098a90f6b254ed2a1a797`
- public release repository: `Yazhan-Labs/yazhan-downloads`
- public release tag: `yazhan-chat-cleaner-v2.1.1`
- public release title: `Yazhan Chat Cleaner 2.1.1`
- primary asset: `YazhanChatCleaner-2.1.1-Setup.exe`
- primary SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`

This approval was action-specific and does not authorize future releases.

## Downloads release execution

The publisher failed safely three times before the successful publication. These failures did not publish or replace a public release:

1. run `32707533358` — Actions-only source reader could not use a Contents endpoint; no public write occurred.
2. run `32707747627` — GitHub job-log retrieval required escape-sequence handling; no public write occurred.
3. run `32707876500` — Windows CRLF checksum lines required normalization; no public write occurred.

The workflow was corrected without widening the source-reader credential beyond `Actions: Read-only`.

Successful publication:

- run: `32708070651`
- job: `97373363003`
- workflow: `.github/workflows/publish-approved-release.yml`
- workflow event: `workflow_dispatch`
- workflow source commit: `0060725fb0ad4f6baf6e4c8e0e147191b9a99158`
- final conclusion: `SUCCESS`

## Public release proof

- repository: `Yazhan-Labs/yazhan-downloads`
- tag: `yazhan-chat-cleaner-v2.1.1`
- title: `Yazhan Chat Cleaner 2.1.1`
- draft: `false`
- prerelease: `false`
- public URL: `https://github.com/Yazhan-Labs/yazhan-downloads/releases/tag/yazhan-chat-cleaner-v2.1.1`
- published assets:
  - `YazhanChatCleaner-2.1.1-Setup.exe`
  - `SHA256SUMS.txt`
- published installer SHA-256: `6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0`

The successful publisher downloaded the published assets again and verified byte/hash equality after publication.

## Superseded historical publication path

On 2026-08-23 this document described an older blocked architecture in which the Chat Cleaner tagged workflow would publish directly into Downloads using a source-repository secret named `YAZHAN_DOWNLOADS_TOKEN`.

That path is `SUPERSEDED` by the Downloads-owned publisher architecture established and proven on 2026-08-24.

Do not:

- configure or recreate `YAZHAN_DOWNLOADS_TOKEN` in the Chat Cleaner repository for this release;
- re-run the old direct cross-repository publication job;
- rebuild or retag `v2.1.1` to reproduce an already completed release;
- replace or move the existing public tag/release.

Historical failed-run evidence remains useful only as history explaining why the architecture changed.

## Final release block states

- source/tag validation: `VERIFIED / COMPLETE`
- standardized source handoff artifact: `VERIFIED / COMPLETE`
- fresh exact owner release approval: `COMPLETE`
- Downloads publisher verification: `VERIFIED / COMPLETE`
- public publication: `VERIFIED / COMPLETE`
- published-byte/hash verification: `VERIFIED / COMPLETE`
- continuity reconciliation: `VERIFIED / COMPLETE`

## Exact next action

No further action is required for Yazhan Chat Cleaner `2.1.1`.

For the next Yazhan application release, wait for a verified standard source handoff, obtain fresh exact owner approval immediately before the protected public-release action, dispatch the Downloads publisher through the approved workflow/controller path, and verify the published bytes before recording completion.
