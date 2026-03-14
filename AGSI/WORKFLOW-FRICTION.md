# AGSI Workflow Friction Analysis

## Overview

Current state: **Zero automation** — nothing moves without Matthew (founder).

Goal: Identify every manual touchpoint to build automation roadmap.

---

## Stage 1: Initial Purchase

| Step | Current Manual Action | Can Automate? |
|------|----------------------|----------------|
| 1a | Customer purchases on Squarespace | ✅ Already digital |
| 1b | **Matt notices payment received** | 🔴 No notification |
| 1c | **Matt logs into Squarespace to identify customer + details** | ✅ Can API/email parsing |

**Friction Points:**
- No automated notification of new purchase
- Must manually check Squarespace dashboard
- Must manually extract customer details (name, address, company)

**Automation Opportunity:**
- Webhook from Squarespace → email to agent → auto-capture details
- Or: Email notification from Squarespace → agent parses → logs to spreadsheet

---

## Stage 2: Onboarding & Prep

| Step | Current Manual Action | Can Automate? |
|------|----------------------|----------------|
| 2a | **Matt drafts welcome email with ClassMarker link + prep page** | ✅ Can create template |
| 2b | **Matt prompts customer every few days** | ✅ Can schedule follow-ups |
| 2c | **Matt reaches out to check for questions** | ✅ Can schedule check-ins |

**Friction Points:**
- Every welcome email is drafted manually (can be templated)
- No automated reminder sequence
- No proactive check-in for stuck customers

**Automation Opportunity:**
- Welcome email triggered by purchase (template + personalization)
- Drip campaign: Day 3, Day 7, Day 14 follow-ups
- Automated check-in: "Any questions?" at Day 7

---

## Stage 3: Examination & Follow-up

| Step | Current Manual Action | Can Automate? |
|------|----------------------|----------------|
| 3a | Customer takes exam on ClassMarker | ✅ Already digital |
| 3b | **Matt receives ClassMarker notification** | 🔴 Manual check |
| 3c | **If pass: Matt writes congrats email + sends branding kit** | ✅ Template possible |
| 3d | **If fail: Matt writes encouragement email** | ✅ Template possible |
| 3e | **Matt adds to directory** | ✅ Can auto-append |

**Friction Points:**
- Must check ClassMarker for results (or wait for email, then act)
- Congrats email drafted each time
- Branding kit delivery manual
- Directory update manual

**Automation Opportunity:**
- ClassMarker webhook → agent receives result → triggers workflow
- Pass: Auto-send congrats email + branding kit link + add to directory
- Fail: Auto-send encouragement + retake info

---

## Stage 4: Certification Maintenance

| Step | Current Manual Action | Can Automate? |
|------|----------------------|----------------|
| 4a | **Matt tracks CE due dates** | 🔴 Manual spreadsheet |
| 4b | **Matt follows up when CEs are due** | 🔴 Manual |
| 4c | **Matt verifies CE completion** | 🔴 Manual review |
| 4d | **Matt tracks who certifies in next 60 days** | 🔴 Manual |

**Friction Points:**
- No database to track certifications
- No automated renewal reminders
- No CE submission/review system
- Must manually identify expiring certifications

**Automation Opportunity:**
- Database for all certifications with expiration dates
- 60-day, 30-day, 7-day automated reminders
- CE submission portal (future)
- Renewal workflow automation

---

## Summary: Friction Heat Map

| Stage | Manual Touchpoints | Automation Priority |
|-------|-------------------|---------------------|
| Purchase | 2 | HIGH |
| Onboarding | 3 | HIGH |
| Exam/Follow-up | 4 | HIGH |
| Maintenance | 4 | MEDIUM (future) |

**Immediate Opportunities:**
1. **Webhook setup** - Squarespace + ClassMarker → agent
2. **Email templates** - Welcome, congrats, encouragement
3. **Customer tracking** - Simple spreadsheet/database
4. **Reminder sequences** - Drip campaigns

**Future Needs:**
1. CE tracking database
2. Public verification page
3. Self-service portal

---

## What I Need to Start Automating

1. **Squarespace webhook or email parsing** - Detect new purchases
2. **ClassMarker webhook or email parsing** - Detect exam results
3. **Email templates** - For each stage
4. **Customer database** - Track status (purchased → onboarded → exam → certified)
5. **Google Drive access** - Branding kit files
