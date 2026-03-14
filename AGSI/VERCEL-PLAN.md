# AGSI Verification Page - Project Plan

## Overview

Public verification page where customers can search for certified technicians and companies.

**URL:** agsinstitute.org/verify (or similar)

---

## Features

### Search
- Search by: Name, Company, City, State
- Real-time results as user types

### Results Display
- **Companies first** (always displayed more prominently)
- **Technicians under their company** (if applicable)
- **Solo technicians** listed individually
- Show: Name, Company, City/State, Certification Type, **Expiration Date**

### Data Source
- TiDB Database (existing)
- Fields: name, company, city, state, certification_type, expiration_date, status

---

## Vercel Project Structure

```
agsi-verification/
├── app/
│   ├── page.tsx          # Main search page
│   ├── layout.tsx        # Layout
│   └── globals.css       # Styles
├── components/
│   ├── SearchBar.tsx     # Search input
│   ├── SearchResults.tsx # Results display
│   └── ResultCard.tsx    # Individual result
├── lib/
│   ├── db.ts             # TiDB connection
│   └── types.ts          # TypeScript types
├── api/
│   └── search/
│       └── route.ts      # Search API endpoint
├── .env.local            # Environment variables
├── next.config.js
└── package.json
```

---

## Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Database:** TiDB (via mysql2)
- **Styling:** Tailwind CSS
- **Deployment:** Vercel

---

## API Endpoint

`GET /api/search?q={query}`

Returns:
```json
{
  "companies": [...],
  "technicians": [...]
}
```

---

## UI Mockup

```
┌─────────────────────────────────────┐
│  AGSI Certification Verification    │
│  [🔍 Search by name, company,      │
│      city, or state...]            │
└─────────────────────────────────────┘

  ┌─────────────────────────────────┐
  │ ★ COMPANY RESULTS               │
  │ ─────────────────               │
  │ ABC Grill Services               │
  │ Houston, TX                     │
  │ Certified: Yes | Expires: 3/15/27│
  │ Employee: John Smith             │
  └─────────────────────────────────┘

  ┌─────────────────────────────────┐
  │ TECHNICIAN RESULTS              │
  │ ─────────────────               │
  │ John Smith                      │
  │ ABC Grill Services              │
  │ Houston, TX                     │
  │ CGCT | Expires: 3/15/27         │
  └─────────────────────────────────┘
```

---

## Priority Rules

1. **Companies always first** - Displayed before technicians
2. **Companies more prominent** - Larger card, highlighted
3. **Technicians under company** - If they work for a certified company
4. **Expiration always shown** - Prominently displayed on every result

---

## Implementation Steps

1. Create Next.js project
2. Configure TiDB connection
3. Build search API
4. Build search UI
5. Apply priority sorting
6. Deploy to Vercel
7. Connect to agsinstitute.org

---

## Owner

This will be built by a **coding sub-agent** with my supervision.
