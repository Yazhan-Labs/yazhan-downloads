# WhatsApp Approved Batch Assistant 3.0.1 — Public Release

Last updated: 2026-08-27

## Status

`STATUS: BLOCKED — SOURCE WORKFLOW PERMISSION FIX REQUIRES OWNER APPROVAL`

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

## ACTIVE JOB — Publish WhatsApp Approved Batch Assistant 3.0.1

### BLOCK MAP

1. Verify release identity + source handoff content — `VERIFIED / COMPLETE`
2. Fresh exact owner public-release approval — `COMPLETE`
3. Initial Downloads publisher attempt — `FAIL-CLOSED / COMPLETE`
4. Standard source handoff correction run — `FAIL-CLOSED / COMPLETE`
5. Source workflow minimum permission correction (`actions: read`) — `BLOCKED BY OWNER CROSS-PROJECT WRITE APPROVAL`
6. Re-run and verify new standard handoff receipt/artifact — `BLOCKED BY BLOCK 5`
7. Re-dispatch already-approved Downloads publisher with successful standard source run — `BLOCKED BY BLOCK 6`
8. Verify public release assets + published bytes/hash — `BLOCKED BY BLOCK 7`
9. Durable continuity closeout — `READY AFTER BLOCK 8`

`PENDING JOB queue: EMPTY`

## Exact next action

Obtain explicit one-time owner permission to modify only `.github/workflows/release-handoff-artifact.yml` in `Yazhan-Labs/whatsapp-approved-batch-assistant` by adding `actions: read` to its existing `permissions:` block. After approval, make that minimum source-workflow-only change, re-run the standard handoff, verify its new artifact/receipt, then automatically resume the already-approved Downloads publication without asking for another public-release approval unless the release identity/scope changes.
