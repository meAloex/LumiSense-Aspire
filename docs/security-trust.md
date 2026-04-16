# Security and Trust

LumiSense is built for review work where incoming material cannot be treated as trusted by default. That rule shapes the rest of the security model.

## Untrusted input

Uploaded files, forms and messages are handled as data, not as instructions. A document can try to instruct the model; the model is not allowed to act on instructions found inside retrieved content.

## Trust zones

Three zones with different authority:

- Untrusted — raw uploads, extracted text, retrieved content. Nothing from this zone executes actions.
- Trusted — system prompts, workflow policies, internal configuration. These define what is allowed.
- Validated tool results — returned from a small allowlist of server-side operations. The model can ask; the server decides.

The model selects from the allowlist; the server validates arguments before running anything.

## Tenant and case isolation

Four layers, applied on every request:

1. Authentication and tenant context — identity and tenant are resolved from the request; no tenant, no access.
2. Query-level tenant filter — data access is filtered by tenant at the ORM boundary, so application code that forgets a filter still cannot read across tenants.
3. Case ownership check — beyond the tenant, every run verifies access to the specific case; cross-case attempts are recorded.
4. Tenant-partitioned storage — raw material is stored per tenant with write-once semantics, so submissions cannot be modified after upload.

## Submitter access

External submitters are not treated like platform users. Access is through a short-lived, case-scoped link that is exchanged for a session, not through a general account. This fits inbound review better than asking an external contributor to register.

## Evidence-linked outputs

Every claim carries a reference to its source — the element, the anchor and the quoted span. The reference is verified at publish time: the quote must exist in the source and the anchor must resolve. Unverified claims do not enter a formal report.

## Audit and continuity

Each run records its inputs, outputs and the configuration snapshot it used. The record is immutable. A reviewer returning to a case tomorrow can see what ran, with what material, under what policy, and what the output was.

## Scope

This is not a compliance claim. It is the security posture the product is built around so compliance work can be layered on later.
