# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

### Risk Assessment Checklist

Use this checklist during planning sessions and weekly risk reviews:

#### Identifying Risks
- [ ] Review project scope and timeline for potential issues
- [ ] Consult with technical leads on implementation challenges
- [ ] Check for external dependencies (vendors, third-party services)
- [ ] Identify resource constraints (team capacity, budget, tools)
- [ ] Consider stakeholder alignment and approval risks
- [ ] Review security and compliance requirements
- [ ] Assess technical debt and infrastructure limitations
- [ ] Check for competing priorities or organizational changes

#### Assessing Each Risk
- [ ] Define risk clearly and specifically
- [ ] Assign Impact level:
  - **High**: Project failure, major delay (>2 weeks), significant budget overrun
  - **Medium**: Moderate delay (1-2 weeks), scope reduction needed
  - **Low**: Minor inconvenience, easily mitigated
- [ ] Assign Likelihood level:
  - **High**: >50% probability, likely to occur
  - **Medium**: 20-50% probability, possible
  - **Low**: <20% probability, unlikely
- [ ] Calculate priority (High Impact + High Likelihood = Critical)
- [ ] Assign risk owner (typically Risk Manager or Project Manager)
- [ ] Set review frequency based on priority

#### Developing Mitigation Plans
- [ ] Identify preventive actions to reduce likelihood
- [ ] Define contingency plans if risk occurs
- [ ] Assign action items with owners and due dates
- [ ] Estimate cost/effort of mitigation
- [ ] Document decision to mitigate, accept, transfer, or avoid risk
- [ ] Set triggers for escalation
- [ ] Update risk register with mitigation plan

#### Monitoring and Reviewing
- [ ] Review high-priority risks at weekly PM sync
- [ ] Update risk status (Active, Mitigated, Occurred, Closed)
- [ ] Track progress on mitigation action items
- [ ] Add newly identified risks to register
- [ ] Escalate critical risks to appropriate stakeholders
- [ ] Document lessons learned when risks occur
- [ ] Archive resolved risks with outcomes

### Example Risk Register Entry

| ID | Description | Impact | Likelihood | Owner | Mitigation Plan | Status |
|----|-------------|--------|------------|-------|----------------|--------|
| R-001 | Third-party API dependency may have downtime during launch | High | Medium | Risk Manager | Build retry logic and caching; have manual fallback process documented | Active |
| R-002 | Key developer out for 2 weeks during critical sprint | Medium | Low | Project Manager | Cross-train team member; adjust sprint commitments | Mitigated |
| R-003 | Database migration may take longer than maintenance window | High | Low | Tech Lead | Test migration on staging with production data size; prepare rollback | Active |

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status

## Communication Templates

### Weekly Status Update Template
Use this template for regular stakeholder updates:
- **Progress this week:**
  - Key accomplishments and milestones reached
  - Features completed and merged
- **Next steps:**
  - Planned work for coming week
  - Upcoming milestones or deliverables
- **Risks & blockers:**
  - Current issues impacting progress
  - Dependencies waiting on external teams
- **Ask / decisions needed:**
  - Specific input or approvals required
  - Trade-off decisions pending

### Weekly Status Update Checklist
- [ ] Review project board and completed work
- [ ] Update risk register with current status
- [ ] Identify blockers requiring escalation
- [ ] Highlight key decisions needed
- [ ] Send update by end of day Friday (or agreed cadence)
- [ ] Archive update in project documentation
- [ ] Follow up on any outstanding action items from previous week

### Stakeholder Communication Checklist
Before major updates or milestones:
- [ ] Identify all stakeholder groups (engineering, sales, support, leadership)
- [ ] Determine communication needs for each group (detail level, frequency)
- [ ] Select appropriate channels (email, Slack, all-hands, direct meetings)
- [ ] Draft message with clear purpose and call-to-action
- [ ] Review with Project Manager and Communication Coordinator
- [ ] Schedule send time for maximum visibility
- [ ] Monitor for questions and respond within 24 hours
- [ ] Document feedback for future communications

### Risk Communication Template
When communicating risks to stakeholders:
- **Risk ID and Description:**
- **Impact:** (High/Medium/Low) - what happens if the risk occurs
- **Likelihood:** (High/Medium/Low) - probability of occurrence
- **Current Status:** (Identified/Being Mitigated/Resolved/Accepted)
- **Mitigation Plan:**
  - Actions being taken
  - Owner and timeline
  - Success criteria
- **Escalation Required:** Yes/No - if yes, specify level and reason
- **Next Review Date:**

### Incident Communication Template
For active incidents requiring stakeholder notification:
- **Incident Summary:**
  - What happened and when
  - Systems or features affected
  - Customer impact (if any)
- **Triage Status:**
  - Current assessment of severity
  - Team members involved
- **Actions being taken:**
  - Immediate remediation steps
  - Investigation progress
- **Expected timeline:**
  - Estimated time to resolution
  - Next update scheduled for [time]
- **Follow-up:**
  - Post-incident blameless retrospective scheduled
  - Action items will be tracked and communicated

### Meeting Facilitation Checklist
For Project Managers and Communication Coordinators:
- [ ] Send meeting invitation with clear purpose and agenda 24-48 hours in advance
- [ ] Include relevant pre-read materials or context
- [ ] Prepare discussion topics and time allocation
- [ ] Assign note-taker and timekeeper roles
- [ ] Start on time with quick agenda review
- [ ] Keep discussion focused on agenda items
- [ ] Document decisions and action items with owners
- [ ] End with clear next steps and follow-up timeline
- [ ] Send meeting notes within 24 hours
- [ ] Track action items in project board or issue tracker

## Escalation Paths

### Standard Issue Escalation
1. **Team Level** (Developer, QA Lead)
   - Identify and attempt to resolve within the team
   - Timeframe: 1-2 business days
   - If unresolved, escalate to Project Manager

2. **Project Manager Level**
   - Assess impact and coordinate mitigation
   - Timeframe: 2-3 business days
   - If requiring scope/resource changes, escalate to Product Lead

3. **Product Lead Level**
   - Make trade-off decisions on scope, resources, or timeline
   - Timeframe: 3-5 business days
   - If requiring budget/strategic decisions, escalate to Sponsor

4. **Sponsor Level**
   - Final decision authority on major changes
   - Provides executive support and resources
   - Communicates to senior leadership as needed

### Risk Escalation Thresholds
Escalate immediately when:
- **High Impact + High Likelihood** risks are identified
- Project timeline at risk of >2 week delay
- Budget overrun >10% expected
- Critical resources become unavailable
- Scope changes affecting core deliverables
- Customer-facing incident or service disruption

### Security & Incident Escalation
- **Immediate**: Notify Security on-call via incident channel
- Follow security incident runbook
- Notify Project Manager and Risk Manager
- Document timeline and actions in incident log
- Schedule post-incident review within 48 hours

### Communication Escalation Checklist
When escalating an issue:
- [ ] Document the issue clearly (what, when, impact, attempts to resolve)
- [ ] Assess urgency and impact level
- [ ] Notify appropriate escalation contact (email + direct message)
- [ ] Provide recommended actions or decisions needed
- [ ] Set expected response timeframe
- [ ] Track escalation in project log or issue tracker
- [ ] Follow up if no response within timeframe
- [ ] Communicate resolution back to team
