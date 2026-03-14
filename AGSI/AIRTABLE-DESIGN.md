# Airtable Base Design

Create a new Airtable base with these tables:

---

## Table 1: Customers

| Field | Type | Description |
|-------|------|-------------|
| Order ID | Single line text | Squarespace order ID |
| First Name | Single line text | From order |
| Last Name | Single line text | From order |
| Email | Email | Customer email |
| Phone | Phone number | From order |
| Company | Single line text | Company name |
| Full Address | Long text | Full address |
| Product | Single select | Founding Cohort, Level 1, Level 2, Study Guide |
| Amount | Currency | Order amount |
| Order Date | Date | When ordered |
| Status | Single select | New, Onboarded, Exam Ready, Passed, Failed, Certified |
| Certification Date | Date | When they passed |
| Expiration Date | Date | 3 years from certification |
| CE Due Date | Date | 1 year from certification |
| Notes | Long text | Any notes |

---

## Table 2: Communications Log

| Field | Type | Description |
|-------|------|-------------|
| Customer (Link) | Link to Customers | Related customer |
| Type | Single select | Welcome, Reminder, Congrats, Fail, CE Reminder, etc. |
| Date | Date | When sent |
| Subject | Single line text | Email subject |
| Status | Single select | Sent, Opened, Clicked |

---

## Table 3: Exam Results (Future)

| Field | Type | Description |
|-------|------|-------------|
| Customer (Link) | Link to Customers | Related customer |
| Exam Date | Date | When taken |
| Score | Number | Pass/Fail or score |
| Result | Single select | Pass, Fail |
| Attempt Number | Number | 1st, 2nd, 3rd attempt |
| Sections | Multiple select | Which BOK sections |

---

## Table 4: CE Records (Future)

| Field | Type | Description |
|-------|------|-------------|
| Customer (Link) | Link to Customers | Related customer |
| Activity Date | Date | When completed |
| Activity Type | Single select | Course, Webinar, etc. |
| Hours | Number | CE hours earned |
| Description | Long text | What they did |
| Approved | Checkbox | Whether approved |

---

## Automation Triggers

Once Airtable is set up, I can:

1. **New Order** → Create Customer record
2. **Onboarded** → Send welcome email
3. **Exam Ready** → Send ClassMarker link
4. **Passed** → Send congrats + add to directory
5. **60 Days Before Expiration** → Send CE reminder
