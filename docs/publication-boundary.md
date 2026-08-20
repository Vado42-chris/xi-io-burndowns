# Public burndown publication boundary

## Purpose

A report may be useful to the public without exposing the private evidence, internal architecture, or proprietary machinery that produced it. This document defines the fail-closed boundary for that transformation.

## Core rule

```text
PRIVATE / INTERNAL WORK
-> abstract the reusable failure or lesson
-> independently reproduce where needed
-> remove direct identifiers
-> test indirect reconstruction risk
-> remove proprietary implementation/decision machinery
-> resolve rights
-> independent release review
-> exact-generation approval
-> PUBLIC REPORT
```

Sanitization alone is not publication qualification.

## Public-safe projection

Prefer outputs such as:

- generalized problem/failure class;
- public consequence or operational lesson;
- bounded method that is useful without revealing proprietary internals;
- synthetic or independently public-safe known-answer tests;
- outcome and limitations;
- remediation principles expressed at a level that does not reveal private source, hidden topology, or trade-secret-like implementation detail.

## Reconstruction-risk review

A candidate fails if a reasonable reader could combine disclosed details to infer private source or proprietary internals with material confidence.

Review at least:

### Identity reconstruction

Names removed but distinctive dates, counts, locations, event sequence, filenames, legal/business terms, or exact metrics still identify the source.

### Topology reconstruction

Repository names removed but dependency relationships, owner numbers, subsystem names, or route structure reveal private portfolio architecture.

### Method reconstruction

Outcome is safe, but the report exposes internal scoring functions, selection weights, proprietary prompts, hidden heuristics, internal thresholds, or enough algorithmic sequence to clone unpublished decision machinery.

### Evidence reconstruction

Hashes, byte counts, object IDs, message IDs, path fragments, screenshots, excerpts, timestamps, or provider metadata permit linkage back to a private corpus.

### Differential disclosure

Multiple individually safe reports can be combined to reveal information that no single report should expose. Review cumulative publication history when the candidate shares a source family or distinctive methodology.

## Publication states

A report candidate should be treated conceptually as one of:

```text
PRIVATE_ONLY
ABSTRACTION_REQUIRED
SYNTHETIC_REPRODUCTION_REQUIRED
PRIVACY_REVIEW_REQUIRED
IP_REVIEW_REQUIRED
RIGHTS_REVIEW_REQUIRED
INDEPENDENT_RELEASE_REVIEW_REQUIRED
PUBLICATION_CANDIDATE
PUBLICATION_QUALIFIED
REJECTED_NO_PUBLICATION
UNKNOWN_BLOCKED
```

These labels describe publication readiness only. They do not create authority outside this repository.

## Minimum release evidence

Before a real report is merged for publication, preserve public-safe evidence that:

- the candidate generation is identified;
- direct identifiers were checked;
- indirect/reconstruction risk was checked;
- private framework/source/topology content is absent;
- proprietary implementation and decision machinery is absent or deliberately disclosed by the rights holder;
- included third-party material has a known publication basis;
- an independent reviewer inspected the exact candidate where required;
- material changes after review invalidate the prior release approval.

The evidence may state that private checks occurred without publishing the private input used to perform them.

## IP minimization principle

Publish **what happened, what class of failure it represents, what was learned, and what a community member can safely test**. Do not publish everything needed to reconstruct how the private system internally discovers, prioritizes, composes, scores, routes, or executes work unless that mechanism has itself been deliberately released.

## Rights

Public visibility is separate from copyright license, contribution terms, trademark permission, redistribution permission, and third-party rights. Until explicit repository policies exist, unresolved rights block the affected publication or reuse action.
