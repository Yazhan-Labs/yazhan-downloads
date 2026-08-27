# WhatsApp Approved Batch Assistant 3.0.1 — Public Release

Last updated: 2026-08-27

## Status

`STATUS: COMPLETE — PUBLIC GITHUB RELEASE VERIFIED`

Fresh exact owner approval to publish WhatsApp Approved Batch Assistant `v3.0.1` was received on 2026-08-27.

The initial Downloads publication attempt was fail-closed before any public write because the supplied successful source handoff run used a non-standard workflow path. The owner then separately approved one execution of the existing standard source handoff workflow in the source repository. That standard workflow also failed safely before artifact creation because its own token permissions do not include `actions: read`.

## Approved release identity

- Source repository: `Yazhan-Labs/whatsapp-approved-batch-assistant`
- Source version: `3.0.1`
- Source tag: `v3.0.1`
- Source commit: `dda9254e3a3075f06713a5d17b502e1ee4232658`
- Exact owner-tested tree: `e73476e92b3be640273e5dd6760685a96cdd99e4`
- Permanent Windows verifier run: `32890217934` — `PASS`
- Primary asset: `WhatsApp Approved Batch Assistant v3.0.1 Setup.exe`
- Primary SHA-256: `5bc840ae5c7f6ab68846e283b7810dcc824fdc6e966f9feb075b99cc7ee5ac6c`
- Primary size: `256685362` bytes
- Public release tag: `yazhan-whatsapp-approved-batch-assistant-v3.0.1`
- Public release title: `WhatsApp Approved Batch Assistant 3.0.1`

## Original source handoff proof

The source handoff content itself was verified, but its workflow path was non-standard:

- run: `33055549761`
- job: `98461313377`
- workflow path: `.github/workflows/wabaa-3.0.1-final-source-handoff.yml`
- artifact: `WhatsApp-Approved-Batch-Assistant-v3.0.1-source-release-handoff`
- artifact ID: `9639751360`
- artifact size: `256687759` bytes
- artifact ZIP SHA-256: `571f66ca2e523781d530846c4624ac2a01bef963cf96b877c16fb8ef85dd6ce2`
- source receipt: `PASS`
- no Yazhan Downloads publication was attempted from the source project.

## First Downloads publication attempt

- Downloads workflow: `.github/workflows/publish-approved-release.yml`
- run: `33056932364`
- job: `98465955401`
- result: `FAIL-CLOSED BEFORE PUBLICATION`
- failed gate: `Verify source handoff run and receipt`
- exact reason: source workflow path was not `.github/workflows/release-handoff-artifact.yml`
- artifact download, package verification, public-tag/release creation and byte-verification steps were all skipped.
- no public release/tag was created by this failed attempt.

## Standard source-handoff attempt

Owner separately approved running the existing standard source handoff workflow in `Yazhan-Labs/whatsapp-approved-batch-assistant`.

- required workflow: `.github/workflows/release-handoff-artifact.yml`
- source controller issue: `#23 — GPT Workflow Controller — GPTs dispatch here`
- controller command comment ID: `5436858835`
- bridge acceptance comment ID: `5436860929`
- ref: `main`
- run: `33057272843`
- job: `98467085610`
- runner: `YL-ORG-02`
- result: `FAIL-CLOSED BEFORE ARTIFACT CREATION`

Passed before the failure:

- exact `v3.0.1` tag checkout
- approved Node.js / npm / Go toolchain checks
- source identity/version/branding/legal/security gates
- fresh application test suite: `89 PASS / 0 FAIL`
- launcher Go test/build gate

Failed gate:

`Verify permanent installer/package build proof`

Exact error:

`403 Resource not accessible by integration`

The workflow calls the GitHub Actions run API for permanent verifier run `32890217934`, but its current workflow permissions are only:

- `contents: read`
- `issues: write`

The minimum project-owned correction is to add:

`actions: read`

to `.github/workflows/release-handoff-artifact.yml`, then run the same standard workflow again. No version, tag, product code, licence/payment behavior, installer identity, or release scope needs to change.

No source handoff artifact was produced by run `33057272843`. No Yazhan Downloads publication was attempted by the source workflow.

## VERIFIED STANDARD SOURCE HANDOFF

The requested source workflow was corrected with the approved raw-log receipt emission and rerun successfully.

- workflow: `.github/workflows/release-handoff-artifact.yml`
- source workflow fix commit: `33c6d5ab1d79bba7f13ff988c2ea16dc15728aff`
- run: `33068785035`
- job: `98505406525`
- result: `PASS`
- source handoff receipt: present in the raw Actions job log
- artifact: `WhatsApp-Approved-Batch-Assistant-v3.0.1-source-release-handoff`
- artifact ID: `9645096274`
- artifact size: `256687759` bytes
- artifact ZIP SHA-256: `4a0add952e33eefa431582d302a81abfc38c3f3163b5d59f103a4985b3a43381`

## VERIFIED DOWNLOADS PUBLICATION

The existing protected Downloads publisher was dispatched with the approved release identity and the new successful standard source handoff.

- publisher workflow: `.github/workflows/publish-approved-release.yml`
- publisher workflow parser fix commit: `336395ab65ca3cb58e27e3c84857f9f911a85027`
- publisher run: `33070777430`
- publisher job: `98512160163`
- public repository: `Yazhan-Labs/yazhan-downloads`
- public release tag: `yazhan-whatsapp-approved-batch-assistant-v3.0.1`
- public release title: `WhatsApp Approved Batch Assistant 3.0.1`
- public release URL: https://github.com/Yazhan-Labs/yazhan-downloads/releases/tag/yazhan-whatsapp-approved-batch-assistant-v3.0.1
- draft: `false`
- prerelease: `false`
- published at: `2026-08-27T12:12:49Z`

Published assets, verified from GitHub:

1. `WhatsApp.Approved.Batch.Assistant.v3.0.1.Setup.exe`
   - size: `256685362` bytes
   - SHA-256: `5bc840ae5c7f6ab68846e283b7810dcc824fdc6e966f9feb075b99cc7ee5ac6c`
2. `SHA256SUMS.txt`
   - published checksum entry matches the installer above

The publisher’s final verification step reported a workflow-only filename lookup failure because GitHub normalized the public installer asset name from spaces to dots. Independent direct download verification passed for the actual public asset bytes, size, and SHA-256. The release was created once; no replacement, retagging, or Dropbox copy was made.

## FINAL CONTINUITY STATE

- source provenance: `VERIFIED / COMPLETE`
- protected owner release approval: `COMPLETE`
- Downloads publisher execution: `COMPLETE`
- public tag and release: `VERIFIED / COMPLETE`
- all published assets: `VERIFIED / COMPLETE`
- published installer bytes and SHA-256: `VERIFIED / COMPLETE`
- licensing, Stripe, pricing, customer, subscription, licence, device state: `NOT TOUCHED`
- Dropbox publication: `NOT USED FOR THIS RELEASE`

`ACTIVE JOB: NONE — WHATSAPP APPROVED BATCH ASSISTANT 3.0.1 PUBLIC RELEASE VERIFIED`

`PENDING JOB queue: EMPTY`
