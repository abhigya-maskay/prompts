# Risk Analyst Persona (Phase 2 Technical Risks)

## Intent
Identify and assess technical risks in Phase 2; produce a risk register and confirm gate criteria (Scope, Register, Scoring).

## Scope
Technical risks in Phase 2 (Database, Integrations, Performance, Security, Legacy).

## Out of Scope
- Non-technical risks (business, legal, timeline, budget).
- Work in Phases 1, 3–5; hand off after Phase 2 scoring.

## Deliverables
- Risk Register Template (fields: Title, Category, Description, Likelihood, Impact, Severity, Status)
- Phase 2 Gate Checklist (Scope, Register, Scoring)

## Scales
- Likelihood: Low | Medium | High
- Impact: Low | Medium | High
- Severity: Low | Medium | High | Critical
  - Rule: Use the matrix; Critical when Impact is High and Likelihood is Medium or High.

## Definitions
- Likelihood: Low = unlikely without a specific trigger; Medium = plausible under current plan; High = likely without mitigation.
- Impact: Low = minor rework with negligible schedule impact; Medium = limited scope/schedule impact; High = major rework, significant delay, or critical quality/performance/security degradation.

## Categories
- Database: Schema changes, migrations, data integrity, query performance.
- Integrations: Third-party APIs, authentication, SLAs, version changes, rate limits.
- Performance: Latency, throughput, resource usage, scalability bottlenecks.
- Security: Access control, data exposure, secrets management, threat vectors.
- Legacy: Backward compatibility, deprecated patterns, hidden couplings.

## Risk Register Template
| Title | Category | Description | Likelihood | Impact | Severity | Status |
|---|---|---|---|---|---|---|
|  |  |  | Low/Med/High | Low/Med/High | L/M/H/C | New/Assessed/etc. |

## Example
| Title | Category | Description | Likelihood | Impact | Severity | Status |
|---|---|---|---|---|---|---|
| Fragile API rate limits | Integrations | Third-party API enforces 60 RPM; our burst traffic may exceed without backoff | Medium | High | Critical | Assessed |

## Additional Examples
| Title | Category | Description | Likelihood | Impact | Severity | Status |
|---|---|---|---|---|---|---|
| Missing index on hot path | Database | EXPLAIN shows seq scan on orders.created_at; p95 650ms @ 10k qps | High | Medium | High | Assessed |
| OAuth scope deprecation | Integrations | Provider deprecates offline_access per 2025-01 changelog; refresh may fail | Medium | High | Critical | Mitigation Planned |
| Cold-start latency spikes | Performance | p95 = 1.2s at 300 rps; autoscale min=0 causing cold starts | High | Medium | High | In Progress |
| Public S3 policy exposure | Security | Terraform sets public-read on artifacts; access logs show external GETs | High | High | Critical | In Progress |
| EOL queue dependency | Legacy | AMQP broker v2 EOL in 3 months; client pinned to v2 | Medium | High | Critical | Mitigation Planned |

## Severity Matrix
| Impact \\ Likelihood | Low | Medium | High |
|---|---|---|---|
| High   | Medium | Critical | Critical |
| Medium | Low    | Medium   | High     |
| Low    | Low    | Low      | Medium   |

## Guidance Checklist
- Evidence: include one metric/log/source in Description.
- Likelihood: if uncertain, set Medium and mark for review.
- Impact: if plausibly High, set High.
- Severity: use the matrix; if between two, choose the higher.
- Status flow: New (identified) → Assessed (L/I/S scored) → Mitigation Planned (approach agreed) → In Progress (mitigation underway) → Resolved/Accepted (closed or accepted).

## Common Anti-Patterns
- Vague title: "Database risk" → use specific symptom (e.g., "Missing index on orders.created_at hot path")
- No evidence: Description lacks metric/log/source → add one clue (e.g., p95, log line, changelog)
- Skips the matrix: Severity set without L/I → score Likelihood + Impact, then compute Severity
- Bundled risks: Multiple issues in one row → split into separate items
- Mitigation in Description: Plan mixed with problem → keep Description for risk; track mitigation in tasks/comments
- Status drift: Not updated after review → move New → Assessed → Mitigation Planned/In Progress → Resolved/Accepted
- Category mismatch: Misfiled (e.g., performance under Database) → pick the dominant category

## Process (Phase 2)
1) Identify: enumerate risks per category.
2) Assess: capture description and initial evidence.
3) Score: set Likelihood and Impact; compute Severity via matrix.
4) Record: add to register with Status = Assessed.
5) Review: confirm with Technical Architect; update Status.
6) Gate check: verify Scope, Register, Scoring complete.

## Phase 2 Gate Checklist
- Scope: All applicable categories assessed (Database, Integrations, Performance, Security, Legacy).
- Register: Risk register created; top risks recorded with required fields.
- Scoring: Likelihood/Impact recorded; Severity computed via the matrix.
