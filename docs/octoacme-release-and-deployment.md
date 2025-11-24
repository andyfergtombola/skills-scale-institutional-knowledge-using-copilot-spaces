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

## Deployment Checklist

### Pre-Deployment (Complete 24-48 hours before)
- [ ] All acceptance criteria met and PRs merged to release branch
- [ ] CI pipeline passing (all tests green)
- [ ] Security scans completed with no critical findings
- [ ] Release notes drafted and reviewed
- [ ] Rollback / mitigation plan documented and reviewed
- [ ] Smoke test plan prepared
- [ ] Stakeholders notified of deployment window
- [ ] Support team briefed on changes and potential issues
- [ ] Database migrations tested (if applicable)
- [ ] Configuration changes reviewed and validated

### Pre-Deployment (Day of Release)
- [ ] Deployment window scheduled and confirmed with team
- [ ] On-call engineer identified and available
- [ ] Communication channels prepared (Slack, email, status page)
- [ ] Backup or snapshot taken (if applicable)
- [ ] Final team sync to review deployment plan
- [ ] Monitoring dashboards prepared and accessible

### Deployment Execution
- [ ] Deploy to staging environment
- [ ] Run smoke tests on staging
- [ ] Verify database migrations on staging (if applicable)
- [ ] Review staging logs for errors or warnings
- [ ] Get approval from QA Lead and Project Manager to proceed
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Monitor deployment progress and logs
- [ ] Verify health checks and service status

### Post-Deployment Verification (Within 1 hour)
- [ ] Run post-deploy smoke tests on production
- [ ] Verify critical user flows are working
- [ ] Check error rates and monitoring dashboards
- [ ] Review application logs for unexpected errors
- [ ] Confirm database migrations completed successfully (if applicable)
- [ ] Test rollback procedure if time permits (optional but recommended)

### Post-Deployment Communication (Within 2 hours)
- [ ] Announce release to stakeholders
- [ ] Notify support team that deployment is complete
- [ ] Update status page or release tracker
- [ ] Share release notes with relevant teams
- [ ] Document any issues or deviations from plan
- [ ] Schedule post-deployment review meeting (within 24-48 hours)

### Post-Deployment Monitoring (24-48 hours)
- [ ] Monitor error rates and performance metrics
- [ ] Track user feedback and support tickets
- [ ] Review system health and stability
- [ ] Address any minor issues discovered
- [ ] Document lessons learned
- [ ] Update runbooks if needed

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
