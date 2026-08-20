# Cold-start onboarding smoke — 2026-08-20

## Subject

Fresh public repository with an empty default branch and no inherited project files.

## Results

### PASS — identity and visibility

Repository identity and public visibility were determinable from the provider without local files.

### FINDING — empty-repository bootstrap gap

Before the first commit, a fresh worker has no repo-local pointer describing purpose, safety boundaries, rights posture, active work, or managed-development expectations. The first commit therefore requires a deliberately minimal bootstrap; normal branch-based mutation can begin only after a base commit exists.

### PASS — least-disclosure bootstrap

The bootstrap README contains only public-safe purpose and boundary information. It does not copy a private framework, private evidence, cross-project state, secrets, or proprietary implementation details into the public repository.

### PASS — rights fail closed

Public visibility is explicitly separated from permission to reuse, redistribute, contribute, or use trademarks. No license or contribution policy was inferred or generated automatically.

### PASS — worker boundary discoverable after onboarding branch

The proposed `AGENTS.md` tells a fresh worker what it may read/propose, what must never be imported or reconstructed, and what gate applies before a real report is added.

### FINDING — portable managed contract still incomplete

The repository currently has a human-readable worker entry contract, but no accepted machine-readable portable managed-project contract is claimed here. The repository must not pretend that prose alone proves full managed-project conformance.

### FINDING — publication safety needs cumulative review

Per-report redaction is insufficient. Multiple public reports can create a differential-disclosure channel that reconstructs private identity, topology, or proprietary methodology. Release qualification must consider cumulative history for related reports.

## Current qualification

```text
PUBLIC REPO BOOTSTRAP              PASS
LEAST-DISCLOSURE INTENT           PASS
RIGHTS DEFAULT                    PASS_FAIL_CLOSED
FRESH-WORKER HUMAN ENTRY          PASS_ON_BRANCH
MACHINE-READABLE MANAGED ABI      NOT_CLAIMED
REAL REPORT PUBLICATION           BLOCKED
INDEPENDENT RELEASE REVIEW        REQUIRED_FOR_PRIVATE_DERIVED_REPORTS
```

## Next safe action

Review the exact onboarding branch for accidental disclosure and worker usability. Do not publish a real private-derived burndown report until a synthetic/public-safe candidate has passed the publication boundary and an independent release review.
