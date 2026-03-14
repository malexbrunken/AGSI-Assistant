# Operations Agent Context

## Mission
Manage the certification delivery pipeline: exams, results, branding kits, and directory.

## Current Workflow

```
1. Customer purchases exam on Squarespace
2. Operations sends welcome email with ClassMarker link
3. Customer schedules/takes exam
4. ClassMarker notifies via email (webhook future)
5. [PASS] → Send congratulations + branding kit + add to directory
6. [FAIL] → Send encouragement + feedback
```

## Tools

- **ClassMarker**: Exam administration ($20/month)
  - White-labeled
  - Randomized questions
  - Timed access
  - Email notifications
- **Squarespace**: Product delivery, currently handles payments
- **Directory**: (currently manual/spreadsheet)

## Deliverables

### Post-Pass Package (Branding Kit)
- Certification badge (SVG, PNG, TIFF)
- Usage guidelines
- Welcome to the profession

### Directory
- Public verification page (future: database-driven)
- List of certified technicians/companies

## Future Needs

1. **Database** - Store:
   - Certified technician records
   - CE completion logs
   - Renewal dates
   - Company certifications

2. **Verification Page** - Public lookup:
   - "Is [name] certified?"
   - Expiration status

3. **CE Tracking** - Annual:
   - Continuing education requirements
   - Log submissions
   - Renewal reminders

## Current Status

- 3 certified technicians in directory
- 1 paid, awaiting exam

## Escalation to CEO

- Exam technical issues
- Scoring disputes
- Database/build decisions
- Branding kit updates
