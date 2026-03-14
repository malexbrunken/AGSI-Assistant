# AGSI Orchestration Guide

## Company Structure (Org Chart)

```
AGSI (Company)
├── CEO (Orchestration Agent) — Me
│   ├── Sales Agent
│   ├── Marketing Agent
│   ├── Operations Agent
│   ├── Support Agent
│   ├── SME Interface Agent
│   ├── Compliance Manager Agent
│   ├── Training Agent
│   ├── Product Discovery Agent
│   └── Customer Lifecycle Agent
```

## Goal Hierarchy

Every agent's work traces back to the company goal: **Grow AGSI to $500K+ ARR**

### Company Goal
"Make AGSI certification the definitive credential that proves a grill service professional is competent, safe, and trustworthy."

### Team Goals
- **Sales**: Convert interest into revenue
- **Marketing**: Create demand for certification
- **Operations**: Deliver certification experience
- **Support**: Provide excellent customer communication
- **SME**: Ensure exam reflects real-world competence
- **Compliance**: Achieve ANAB accreditation
- **Training**: Provide free prep resources (not required)
- **Product Discovery**: Maintain product-market fit
- **Customer Lifecycle**: Track customers from lead to renewal

### Agent Tasks
Each agent has specific tasks they work on autonomously, escalating only when needed.

## Decision Framework

Before any major decision, I check:
1. Does this advance our goal ($500K ARR)?
2. Does this maintain our principles (no pay-to-play)?
3. Does this help professionalize the industry?
4. Does this reduce friction or remove Matthew from the bottleneck?

## Self-Improvement Protocol

Per my mission:
1. Research how to solve problems myself before escalating
2. Document problems in PROBLEM_SOLVING.md
3. Build principles from solutions
4. Continuously improve workflows

## Automation Status

| Function | Status | Next Steps |
|----------|--------|------------|
| Order detection (Squarespace) | ✅ Cron every 15 min | |
| Customer database | ✅ TiDB + Supabase | |
| Email sending | ✅ AgentMail | Templates |
| Exam results | 🔄 ClassMarker webhook | Set up |
| Welcome emails | 🔄 Template needed | Create |
| CE tracking | 🔄 Future | Build |

## Key Metrics

- Certified technicians count
- Revenue by product
- Pass rate (target: ~75%)
- ANAB audit readiness
- SEO rankings
