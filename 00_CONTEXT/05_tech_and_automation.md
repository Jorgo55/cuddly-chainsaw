# Tech Stack & Automation Requirements

## CRM
- **Go High Level (GHL)** — Andy's existing system
- Everything automated from registration onward

## Automation Flow
```
Lead registers on funnel
        ↓
Data hits CRM automatically
        ↓
Automated email + SMS: confirmation + booking details
        ↓
30 min before call: automated reminder (email + SMS)
        ↓
Salesperson joins Google Meet at booked time
        ↓
Post-call: automated follow-up sequences
```

## Video Calls
- **Google Meet** (NOT Zoom)
- Reasons: free, no download, accessible via Chrome, scales cheaper
- Auto-generated meeting links sent at booking

## Funnel Tech
- Custom built (we're the dev team)
- Full CRM integration
- Video player with completion gating (must watch before proceeding)
- Calendar/booking integration
- Qualification questions at booking step

## Email Infrastructure
- Custom SMTP setup for cold outreach
- 1 email/minute send rate to avoid blocks
- Independent of third-party platforms (Instantly, etc.)
- Focus on deliverability at the infrastructure level

## Future Automation Possibilities (Not Now)
- AI calling for SDR replacement (too expensive for now)
- AI content creation for social media (our main R&D project)
- Full automated video creation + social posting pipeline
- AI salesperson (ultimate goal, way down the line)

## What We're Building (Our Scope)
- The funnel (landing page → booking → thank you)
- CRM integration
- Email/SMS automation sequences
- Qualification logic
- Full system — not just a landing page
