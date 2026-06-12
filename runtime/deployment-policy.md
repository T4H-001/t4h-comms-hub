# Deployment Policy

Status: PARTIAL

App: t4h-comms-hub
Source of truth: GitHub repo TML-4PM/t4h-comms-hub
Production branch: main
Publisher: Vercel
Production URL: https://t4h-comms-hub.vercel.app

## Rule

No production change is REAL unless it has:

1. a Git commit receipt
2. a successful Vercel deployment
3. a post-deploy smoke test
4. an entry in the Reality Ledger

## Release flow

feature branch -> pull request -> build/test -> preview deployment -> smoke test -> merge to main -> production deploy -> production smoke test -> ledger receipt

## Required controls

- Protect main
- Require pull requests
- Require status checks
- Require signed commits where possible
- Restrict force pushes
- Separate content, infrastructure, and data changes
- Record rollback path for production-impacting changes

## Current gaps

- Branch protection not yet confirmed
- Smoke tests not yet confirmed
- Deployment receipt automation not yet confirmed
- Runtime data sources not yet mapped

## Next action

Add smoke routes, release receipt template, and GitHub workflow checks.
