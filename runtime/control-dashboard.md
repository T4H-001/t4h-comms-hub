# Runtime Control Dashboard

Status: PARTIAL

Purpose: one operational view for whether t4h-comms-hub is safe, current, and controlled.

## Panels

1. GitHub
- repo
- branch
- latest commit
- pull request state
- required checks

2. Vercel
- project
- production deployment
- deployment status
- production alias
- rollback candidate

3. Site health
- homepage status
- key route status
- last smoke test
- unexpected 404s

4. Release receipts
- latest receipt
- receipt completeness
- Reality Ledger link

5. Gaps
- missing checks
- missing receipts
- stale deployment
- branch protection unknown

## Truth rule

The dashboard must not mark a release REAL unless GitHub commit, Vercel deployment, smoke test, and ledger receipt all agree.

## Minimum dashboard data contract

```yaml
app: t4h-comms-hub
repo: TML-4PM/t4h-comms-hub
branch: main
commit_sha: REQUIRED
vercel_deployment_id: REQUIRED
production_url: https://t4h-comms-hub.vercel.app
smoke_status: REQUIRED
ledger_receipt: REQUIRED
status: REAL | PARTIAL | BLOCKED
```
