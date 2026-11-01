# Yazhan Downloads — Project Control

PROJECT: Yazhan Downloads — public distribution/release assets only
REPOSITORY: Yazhan-Labs/yazhan-downloads
REPOSITORY_ID: 1329118286
STATUS: RESTORED / LIVE VERIFIED — both existing public installer releases restored 2026-11-01; GitHub Actions executable workflow definitions disconnected.
SOURCE_REF: main
SOURCE_HEAD: b8822552d525bc885a3db5357946d4c5f23d8518 (last verified before this control-file update; re-read main on resumption)
GOAL: Keep the owner's previously approved Yazhan releases publicly downloadable with exact verified provenance, original bytes, and intact tags/history.
CURRENT_WORK: Downloads-owned 2026-10-30 customer download outage repaired. Website owner live-site follow-up remains EXTERNAL_OWNER. No active local upload.
NEXT_ACTION: Await Website owner's live link recheck; do not alter Website's repo. For a future owner-approved release, accept only exact validated handoff and fresh approval, verify public bytes, and use current Central 7.6 owner-PC execution rules (mapped Slack Agent first, existing Central #312 for that technically blocked task only). Establish a verified mapped Downloads execution channel before future normal Owner-PC tasks; no channel has been found/READY-verified as of 2026-11-01.
COMPLETED_AND_PROTECTED: Original published release identities, tags and historical approved source/artifact provenance in PROJECT_MASTER.md and docs/*_PUBLIC_RELEASE.md; superseded Chat Cleaner 2.0.0 retirement on 2026-08-28; exact original releases restored below. Do not redo unrelated history.
DO_NOT_REDO: Historical source app release builds, owner approvals and release validation; do not rerun 2026-11-01 upload jobs. Their remote assets now exist.
CURRENT_DECISIONS: CENTRAL_VERSION=7.6.0 and AGENT_CONTRACT_VERSION=1.2; owner explicitly approved exact original installer/checksum reattachment on 2026-11-01 contingent on SHA-256 verification; no new tags or substitute artifacts. GitHub Actions/runners prohibited; archived legacy workflow source is non-executable. Auto-Wake PARKED. No source-app, licensing, payment or customer changes.
CANONICAL_SPECS: Central CENTRAL.md; docs/RELEASE_HANDOFF_TEMPLATE.md (historical Actions-based handoff needs adaptation before future use). PROJECT_MASTER.md and docs/*_PUBLIC_RELEASE.md preserve historical evidence, not newer operating rules.
ACTIVE_WORK:
- DOWNLOADS-RESTORE-20261101: DONE_VERIFIED — both original releases recovered, public unauthenticated HTTPS GET + SHA-256 and original checksum-file byte comparison PASS; original #complaints thread updated RESOLVED. Source: https://yazhan.slack.com/archives/C0C7L8LBQV9/p1793372089949909
- DOWNLOADS-NO-ACTIONS-20261101: DONE_VERIFIED — archived both unchanged legacy workflows under docs/legacy-github-actions/ with blob SHA readback, removed both executable .github/workflows/*.yml paths; read full main tree, zero executable workflow paths.
- WEBSITE-LIVE-CHECK: EXTERNAL_OWNER — Website project to recheck visitor links live; original complaint thread has Downloads-side verified restoration evidence. Do not change Yazhan-Labs/yazhan-net from Downloads.
- WABAA-SUMS-NAME: PARKED — restored original SHA256SUMS.txt contains the correct SHA-256 but refers to the pre-normalization filename with spaces while GitHub public installer basename uses dots. Exact original file was intentionally preserved under 2026-11-01 approval; changing its contents needs a separate scoped decision.
- DOWNLOADS-AGENT-MAPPING: BLOCKED for future local tasks — no verified mapped Slack Downloads Agent channel found; owner/Agent onboarding READY required. The existing protected Central #312 Bridge was used for this technically unconfigured restoration, not as a new default route.
LATEST_ARTIFACT:
- C:/Users/balaj/Dropbox/Yazhan Labs/Artifacts storage/yazhan-downloads/yazhan-chat-cleaner-v2.1.1/
- C:/Users/balaj/Dropbox/Yazhan Labs/Artifacts storage/yazhan-downloads/yazhan-whatsapp-approved-batch-assistant-v3.0.1/
BLOCKERS: No blocker to the repaired customer release files. Future normal Owner-PC execution needs mapped Slack Agent READY. Website live-page confirmation is outside Downloads ownership.
PROOF:
- Central #312 /yl-pc terminal downloads-restore-originals-preflight-20261101-001 COMPLETE exit=0: both retained 63,304,856 / 256,685,362 byte binary SHA-256 hashes match approved originals, both GitHub releases initially assets=[].
- Chat Cleaner release ID 375558905, original tag yazhan-chat-cleaner-v2.1.1: upload job downloads-restore-chatcleaner-20261101-002 terminal COMPLETE exit=0; assets installer 699028540 and checksum 699028537.
- WABAA release ID 377794540, original tag yazhan-whatsapp-approved-batch-assistant-v3.0.1: upload job downloads-restore-wabaa-20261101-003 terminal FAILED ONLY at post-upload GitHub API call timeout; independent GitHub REST confirms two assets state=uploaded (installer 699034158; checksum 699034160), exact names/sizes preserved.
- Central #312 downloads-verify-public-bytes-20261101-004 terminal COMPLETE exit=0: unauthenticated public HTTP fetched both installer and checksum files; Chat Cleaner installer SHA-256 6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0; WABAA SHA-256 5bc840ae5c7f6ab68846e283b7810dcc824fdc6e966f9feb075b99cc7ee5ac6c; public checksum files byte-identical to retained originals; temporary test downloads cleaned.
- GitHub main recursive tree verified 2026-11-01 with zero .github/workflows paths, two byte-identical archived workflow definitions in docs/legacy-github-actions.
