# Team API Package
## MarTech Platform Team

This package is an example of how a team can publish a usable interface instead of forcing every partner team into recurring coordination meetings.

A Team API is not a slogan. It is a contract.

It should answer five questions fast:
1. What does this team own?
2. How do I consume it?
3. What can I expect from it?
4. How do changes get communicated?
5. When do we actually need to meet?

---

## Package Contents

- `team-api.yaml`  
  Machine-readable team profile and interface summary.

- `service-catalog.md`  
  The list of services, owners, supported use cases, and support levels.

- `request-intake.md`  
  Standardized intake model for requests and exceptions.

- `governance.md`  
  Versioning, deprecation, approval, and control rules.

- `support.md`  
  Support model, response expectations, and escalation paths.

- `changelog.md`  
  Material changes to the Team API and service contracts.

- `services/`  
  Detailed contracts for each reusable capability.

- `templates/`  
  Templates consumers use instead of booking “quick syncs”.

- `metrics/scorecard.md`  
  Adoption, reliability, and friction measures.

- `examples/`  
  Concrete sample contracts for event tracking and audience definitions.

---

## Core Principles

- Repeated requests become products.
- Definitions live in contracts, not in memory.
- Standard work is async by default.
- Meetings are escalation tools, not plumbing.
- Every interface has an owner, SLE, and deprecation path.

---

## How To Use This Package

### If you consume MarTech capabilities
1. Check `service-catalog.md`.
2. Read the relevant contract in `services/`.
3. Submit the matching template from `templates/`.
4. Track status through the request system.
5. Escalate only if the request meets escalation criteria.

### If you run the MarTech platform team
1. Publish this package in an internal portal or repo.
2. Keep the catalog current.
3. Version major contract changes.
4. Review the scorecard monthly.
5. Kill any meeting that exists only because the contract is unclear.

---

## Escalation Rules

A live meeting is warranted only when one of these is true:

- A Sev 1 / Sev 2 incident is active.
- A legal or privacy interpretation is blocking launch.
- Two teams disagree on a definition or ownership boundary.
- A decision must be made inside 48 hours and async review has stalled.
- A new capability spans multiple domains and no stable contract exists yet.

Everything else should resolve through the package.

---

## Suggested Publishing Cadence

- **Weekly**: Changelog updates
- **Monthly**: Service metrics and adoption review
- **Quarterly**: Contract review and deprecation window audit
- **Twice yearly**: Team API redesign review

Because the alternative is institutionalized confusion with a calendar invite.
