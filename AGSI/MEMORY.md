# AGSI Memory - Key Learnings

## Company Overview

**AGSI - American Grill Service Institute** is a certification body for grill service technicians. Founded by Matthew Brunken (also runs Houston Grill Clean).

**Mission:** Make AGSI certification the definitive credential that proves a grill service professional is competent, safe, and trustworthy.

**Goal:** Grow to $500K+ ARR

## Revenue Streams

| Product | Price |
|---------|-------|
| CGCT (Level 1) | $499/3yr |
| CAGST (Level 2) | $499/3yr |
| Founding Cohort | $299/3yr |
| Company Certification | $6K+/yr |
| Study Guide | $19 |

## Current Status (March 2026)

- 3 certified technicians
- 1 paid, awaiting exam
- Revenue: Profitable (costs ~$200/year + tokens)

## Key Constraints

1. **No pay-to-play** - Can't require training to certify (ISO 17024 / ANAB)
2. **Training ≠ Certification** - Can provide free resources, but can't require purchase
3. **SME requirement** - Year 2+ needs Subject Matter Expert involvement in exam questions
4. **ANAB audit** - Due in ~10 months

## Technical Stack

- **Website**: Squarespace (Core plan with API access)
- **Exams**: ClassMarker ($20/month)
- **Database**: Airtable (to be set up)
- **Payments**: Squarespace Commerce

## API Access

- **Squarespace API Key**: a9fbe5ab-e244-4e4d-9cde-99ea2b60934d
- **Endpoint**: https://api.squarespace.com/1.0/commerce/orders

## Current Customers (from API)

1. Matthew Maloney - Bar-B-Clean (CA) - Founding Cohort - $299 - PENDING
2. Andrew Chestnut - BBQ Rescue (MD) - Founding Cohort - $299 - PENDING
3. (Study guide purchases - fulfilled/refunded)

## Friction Points (13 manual touchpoints)

1. Check for payment notifications
2. Extract customer details from Squarespace
3. Draft welcome email
4. Send reminders (manual follow-up)
5. Check-in on exam progress
6. Check ClassMarker for results
7. Draft congrats email (pass)
8. Send branding kit
9. Draft encouragement email (fail)
10. Update directory manually
11. Track CE due dates
12. Follow up on CE completion
13. Verify CE logs

## Workflow to Automate

```
Purchase (Squarespace)
    ↓
Agent detects new order → Creates Airtable record
    ↓
Auto-email: Welcome + ClassMarker link + Prep page
    ↓
Reminder sequence (Day 3, 7, 14)
    ↓
ClassMarker result → Agent detects
    ↓
[PASS] → Congrats email + Branding kit + Add to directory
[FAIL] → Encouragement email
    ↓
60-day renewal warning (future)
```

## Agent Structure

| Agent | Role |
|-------|------|
| CEO | Orchestration, $500K ARR goal |
| Sales | Convert leads to customers |
| Marketing | SEO, brand, demand generation |
| Operations | Exam delivery, branding kits |
| Support | Customer communication |
| SME | Subject Matter Experts, BOK |
| Compliance | ANAB audit prep, ISO 17024 |
| Training | Free prep materials (NOT required) |

## Files

- AGSI/AGSI-MISSION.md - Company mission
- AGSI/ORCHESTRATION.md - CEO guide
- AGSI/WORKFLOW-FRICTION.md - Manual touchpoints
- AGSI/AIRTABLE-DESIGN.md - Database design
- AGSI/agents/*/MISSION.md - Agent missions
