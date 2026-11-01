# Yazhan Downloads — Project Control

PROJECT: Yazhan Downloads — public binary distribution only
REPOSITORY_ID: 1329118286
REPOSITORY: Yazhan-Labs/yazhan-downloads
STATUS: BLOCKED — customer-facing download outage; previous public release records exist but their assets are missing.
SOURCE_REF: main
SOURCE_HEAD: 0c06d3ce687e31ba44265078c39dbf3f66a30279 (pre-control-file baseline, 2026-08-28)
GOAL: Restore exact previously approved, byte-verified installer and SHA256SUMS assets to the existing Chat Cleaner 2.1.1 and WhatsApp Approved Batch Assistant 3.0.1 public releases, preserving their release identities, history and hashes.
CURRENT_WORK: Investigating October 5 asset removal; GitHub GET on 2026-11-01 independently confirms both releases still published with assets=[].
NEXT_ACTION: Obtain fresh exact protected owner permission for reattaching both original verified packages; verify the retained installer bytes against original approved SHA-256 and checksum manifests; establish/verify mapped project Slack Agent channel before any Owner-PC work (Slack first, Central #312 only for a confirmed same-task technical Agent failure); restore the exact assets on existing releases; independently fetch public downloads and verify byte/hash identity; report results in the original #complaints thread and request Website owner live verification.
COMPLETED_AND_PROTECTED: Historical successful public releases, tags, source provenance, approved hashes and past decisions are documented in PROJECT_MASTER.md and docs/*.md; do not redo unrelated project work, change source-app repos or remove release records/tags.
DO_NOT_REDO: Past completed publication/release validation and 2026-08-28 one-time retirement of superseded Chat Cleaner 2.0.0. Do not assume past publication implies assets are still present.
CURRENT_DECISIONS: CENTRAL_VERSION=7.6.0 controls; no GitHub Actions/runners for execution; no Auto-Wake; fresh exact protected release approval before publication or asset reattachment; no unverified substitute binaries; no unrelated source/licensing/customer changes.
CANONICAL_SPECS: Central CENTRAL.md; docs/RELEASE_HANDOFF_TEMPLATE.md (legacy workflow-dependent sections need reconciliation with Central 7.6); PROJECT_MASTER.md and docs/*_PUBLIC_RELEASE.md retain historical evidence only.
ACTIVE_WORK:
- DOWNLOADS-RESTORE-20261101: BLOCKED — approved release IDs 377794540 (WABAA) and 375558905 (Chat Cleaner) each have zero assets; exact Dropbox candidates and checksum manifests found, but binary SHA-256 still requires verification, protected authorization and a valid execution route. Source of truth: https://yazhan.slack.com/archives/C0C7L8LBQV9/p1793372089949909
- DOWNLOADS-NO-ACTIONS-20261101: OWNED — both .github/workflows/publish-approved-release.yml and gpt-workflow-bridge.yml are executable historical GitHub Actions paths, contrary to Central 7.6.0; disconnect/reroute safely without deleting protected release history or relying on Actions for a restoration.
BLOCKERS: Fresh release-repair authorization not yet obtained; no mapped Downloads Slack Agent execution channel was located; actual installer bytes not yet SHA-256 checked; no safe replacement release-execution path yet established.
PROOF:
- 2026-11-01 GitHub API /releases and /releases/{id}/assets confirms both published release records have assets=[].
- Retained original file candidates, correct historic sizes and matching checksum-manifest entries in Dropbox:
  - /Yazhan Labs/Artifacts storage/yazhan-downloads/yazhan-chat-cleaner-v2.1.1/ (YazhanChatCleaner-2.1.1-Setup.exe, 63304856 bytes; expected SHA-256 6787fb92723be614863df1590d85d437c322773ca4216c6980e50a09453708f0)
  - /Yazhan Labs/Artifacts storage/yazhan-downloads/yazhan-whatsapp-approved-batch-assistant-v3.0.1/ (WhatsApp.Approved.Batch.Assistant.v3.0.1.Setup.exe, 256685362 bytes; expected SHA-256 5bc840ae5c7f6ab68846e283b7810dcc824fdc6e966f9feb075b99cc7ee5ac6c)
- Dropbox matches are metadata/manifests only, NOT yet hash verification of binary bytes.
LATEST_ARTIFACT: Existing versioned retained Dropbox directories above; do not create new or duplicate retained artifacts elsewhere.
