# BridgeMed OpenAPI client Phase 1 readiness

Status: project-branch readiness note for `copr/bridge-med-project`. This document is informational and does not approve production deployment, API scope expansion, secrets changes, infrastructure changes, or a release PR to `main`.

## Role in Phase 1

This repository is the generated contract bridge between `backend-api` and `app-frontend`.

For Phase 1, generated clients must keep the UI aligned with backend OpenAPI surfaces for:

- Catalog content publication, visibility policies, and recipient explanations.
- Training request idempotency header support.
- Product-level video metadata, upload-complete, playback/status, and not-configured contracts.

## Zero-PHI contract guardrails

The generated client must preserve BridgeMed's product boundary:

> No patient data. No cases. No schedules.

Before accepting generated output or hand-authored docs, confirm that API models, docs, examples, and request helpers do not introduce:

- Patient identities, MRNs, dates of birth, diagnoses, treatment details, or patient-linked identifiers.
- Case identifiers, care-delivery timelines, procedure schedules, room assignments, or appointment context.
- PHI-bearing filenames, object keys, cache key examples, analytics labels, logs, fixtures, or sample payloads.

Generated video models should remain product/content metadata surfaces only. Storage object keys and playback authorization must use opaque IDs and backend-issued authorization, not user-entered labels.

## Generation source of truth

- Source contract: `../backend-api/api/openapi.yaml` from the backend `copr/bridge-med-project` lineage.
- Generator: `@openapitools/openapi-generator-cli` with `typescript-fetch`.
- Output: `typescript-client/`.

Recommended generation command:

```bash
cd ../openapi-client
npx --yes @openapitools/openapi-generator-cli generate \
  -i ../backend-api/api/openapi.yaml \
  -g typescript-fetch \
  -o typescript-client \
  --additional-properties=supportsES6=true,useSingleRequestParameter=true,withInterfaces=true,modelPropertyNaming=original
```

Java is required by OpenAPI Generator. If `java` is unavailable in the runner, do not hand-edit generated output to simulate a generator run; document the blocker and rely on a runner with Java.

## Acceptance gates for generated-client slices

For each OpenAPI/client sync slice:

1. Start from the current `copr/bridge-med-project` project branch state.
2. Regenerate from the backend project-branch OpenAPI contract.
3. Inspect generated API methods and models for the intended backend contract changes only.
4. Run `git diff --check`.
5. Run `yarn install --immutable` when available.
6. Run a zero-PHI scan over generated docs/examples and any hand-authored README/status changes.
7. Update downstream `app-frontend` dependency pins only after the client branch is merged to the project branch.

## Human approval checkpoints

Stop and ask before:

- Documenting speculative API endpoints that are not implemented in backend handlers.
- Expanding the contract into patient, case, procedure schedule, EHR, inventory, native mobile, or chat scope.
- Adding telemetry, secret handling, auth behavior, billing, cloud/storage/CDN, or deployment assumptions.
- Accepting unresolved Critical or High security/compliance findings.
