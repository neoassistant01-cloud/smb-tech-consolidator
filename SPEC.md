# SMB Tech Stack Consolidator - MVP Specification

## Project Overview
- **Name:** SMB Tech Stack Consolidator
- **Type:** Single-file HTML MVP (localStorage)
- **Purpose:** Help small businesses audit, track, and optimize their SaaS subscriptions
- **Target:** Business owners with 5-15 SaaS tools

## UI/UX

### Layout
- Single page app with 3 tabs: Dashboard, Subscriptions, Add New
- Bottom tab navigation (mobile-first)
- Desktop: sidebar + main content area

### Color Palette
- Primary: #1E3A5F (deep navy)
- Secondary: #3B82F6 (blue accent)
- Success: #10B981 (green)
- Warning: #F59E0B (amber)
- Danger: #EF4444 (red)
- Background: #F8FAFC (light gray)
- Card: #FFFFFF
- Text: #1F2937

### Typography
- Font: 'DM Sans', sans-serif
- Headings: 600 weight
- Body: 400 weight

### Components
- Subscription cards with cost, category badge, usage indicator
- Progress bars for spend limits
- Category pie chart (CSS-based)
- Alert banners for unused tools

## Features

1. **Dashboard**
   - Total monthly spend
   - Total yearly spend
   - Category breakdown (chart)
   - Unused tools warning
   - Recent additions list

2. **Subscriptions List**
   - All subscriptions with search/filter
   - Sort by cost, name, date added
   - Usage frequency indicator
   - Delete/edit actions

3. **Add Subscription Form**
   - Name, cost, billing cycle (monthly/yearly)
   - Category dropdown
   - Usage frequency (daily/weekly/monthly/rarely)
   - Notes field

4. **Unused Tool Detection**
   - Auto-flag tools marked "rarely" used
   - 30-day reminder indicator

5. **CSV Export**
   - Export all subscriptions

## Data Model
```json
{
  "id": "uuid",
  "name": "Tool Name",
  "cost": 29.99,
  "billingCycle": "monthly|yearly",
  "category": "accounting|crm|marketing|productivity|communication|other",
  "usageFrequency": "daily|weekly|monthly|rarely",
  "lastUsed": "2026-04-01",
  "notes": "",
  "createdAt": "2026-04-05"
}
```

## Acceptance Criteria
- [ ] Add subscription persists to localStorage
- [ ] Dashboard shows accurate totals
- [ ] Unused tools flagged correctly
- [ ] CSV export works
- [ ] Mobile responsive