# Yazhan Downloads — Release Handoff

Use this when an app is ready for public release.

SOURCE REPOSITORY:
SOURCE VERSION:
SOURCE TAG:
SOURCE COMMIT:
SOURCE WORKFLOW RUN ID:
SOURCE ARTIFACT NAME:
PUBLIC RELEASE TAG:
PUBLIC RELEASE TITLE:
PRIMARY ASSET:
PRIMARY ASSET SHA-256:
OWNER RELEASE APPROVAL: YES / NO

## Required source handoff workflow

The source app prepares and validates the release package only.

Standard source workflow path:

`.github/workflows/release-handoff-artifact.yml`

Standard handoff job name:

`create-handoff-artifact`

The handoff run must be an explicit successful `workflow_dispatch` run.

Its final receipt must state the exact approved:

- source tag
- source commit
- primary installer/package SHA-256
- `SOURCE RELEASE HANDOFF: PASS`
- `No Yazhan Downloads publication was attempted.`

## Required artifact contents

The source artifact must contain only the approved handoff files needed by Downloads:

- approved public release asset(s)
- `SHA256SUMS.txt`
- `RELEASE_NOTES.md`

The primary asset hash in `SHA256SUMS.txt` must match the approved handoff SHA-256.

`Yazhan-Labs/yazhan-downloads` is the only public publisher.

Source application repositories do not receive a Downloads publishing token.
