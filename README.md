# StockPilot

Inventory management and replenishment planning for small shops.

## Project status

- Planning baseline: 6 weeks starting 2026-10-26 (proposed; adjust to the course deadline).
- Initial repository bootstrap; implementation stack is to be confirmed by the team in Sprint 0.
- Work items are tracked by IDs `SP-001` to `SP-033` in GitHub Issues and the team's Excel tracker.

## MVP scope

- Authentication and RBAC: Owner/Manager, Staff, Analyst, Admin.
- Products, categories, and suppliers.
- Purchase orders and sales orders.
- Inventory transactions, stock count, and stock adjustment.
- Basic dashboard, Smart Replenishment, and Alert Center.
- Audit log and database backup/restore.
- Tests, documentation, and LAN/staging deployment.

Inventory correctness is a key requirement: confirmed operations should update stock atomically, duplicated confirmations must be prevented, and confirmed transaction history should not be edited directly.

Smart Replenishment uses explainable rules from the project specification. When sales history is unavailable, surface a no-demand-data state instead of pretending the product has a reliable forecast. Suggested purchase orders require user review; do not automatically confirm orders.

## Team responsibilities (temporary labels)

| Member | Primary focus |
|---|---|
| TV1 — Nguyễn Quốc Thịnh (`nquocthinh06`) | **Confirmed:** BE lead — database/migrations, authentication/RBAC, API, inventory transaction integrity, audit log, replenishment logic |
| TV2 — not decided | Frontend/UI is a **proposed** role only; wait for member confirmation |
| TV3 — not decided | QA/DevOps/CI, backup/restore and deployment are **proposed** responsibilities only; wait for member confirmation |
| All | Architecture/ERD decisions, PR reviews, end-to-end testing and demo |

Only TV1's BE lead role is confirmed. Do not treat the proposed TV2/TV3 assignments as final until those members choose their roles. Update task owners and GitHub assignees after the team agrees.

## Getting started

1. In Sprint 0, choose one frontend framework, one backend framework and PostgreSQL; record exact versions and decisions.
2. Add the project setup instructions and `.env.example` once the stack is selected. Never commit credentials or production data.
3. Review [GitHub Issues](https://github.com/nquocthinh06/StockPilot-Manager-Teams/issues) and start with SP-001 through SP-005.
4. Link a branch and pull request to its Issue using the shared `SP-###` identifier.

## Collaboration conventions

- Branches: `feature/SP-###-short-name` or `fix/SP-###-short-name`.
- Commits: `SP-###: imperative summary`.
- Pull requests must describe changes, tests run, screenshots where useful, and link the Issue (e.g. `Fixes #7`).
- At least one teammate other than the author reviews the PR.
- Mark a task Done only after the PR is merged, applicable tests pass, and relevant documentation is updated.
- Record blockers in the relevant Issue. Sync the Excel tracker at least twice per week.

## Project documents

The planning baseline and Excel tracker are maintained by the team. Use the GitHub Issue ID/URL column in the workbook to navigate from a task to its detailed acceptance criteria.
