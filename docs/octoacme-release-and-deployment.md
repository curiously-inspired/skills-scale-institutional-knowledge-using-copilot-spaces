# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared
- **Release Manager Coordination:**
  - Confirm release readiness with QA Engineers and Developers
  - Verify all stakeholder sign-offs are complete
  - Schedule deployment window and communicate to all teams
  - Prepare rollback procedures and deployment verification steps

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) — **Release Manager coordinates**
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests — **QA Engineer validates**
- [ ] Deploy to production (automated pipeline preferred) — **Release Manager oversees**
- [ ] Run post-deploy verifications — **Release Manager and QA Engineer**
- [ ] Announce release to stakeholders and support — **Release Manager and Support Lead**

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call — **Release Manager leads**
  - Rollback to last known-good release if necessary — **Release Manager executes**
  - Triage root cause and capture action items — **Development team with Release Manager**
  - Communicate status to customers — **Support Lead coordinates**

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
