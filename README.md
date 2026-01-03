# KinkDom — MVP Feature Lock

**Status:** Locked for MVP  
**Phase:** Closed Alpha → Early Beta  
**Purpose:** Prevent scope creep, ensure safety, and enable fast, controlled launch

---

## Overview

**KinkDom** is a free-first, consent-driven social discovery app for adults (18+) seeking kink-aligned connections.  
The MVP focuses on **safe discovery, controlled interaction, and strict ratio enforcement** to create a welcoming and secure environment—especially for women.

This document defines the **non-negotiable scope** of the MVP.  
Anything not listed here is **explicitly out of scope** until Post-MVP review.

---

## Core Principles

- Safety over scale  
- Trust over features  
- Ratio enforcement over growth  
- Server-side enforcement for all critical logic  

---

## Target Users

- Adults **18+ only**
- Men and women seeking consensual, kink-aligned interactions
- Early adopters participating in a closed alpha environment

---

## Core Value Proposition (MVP)

- Discover like-minded people based on interests, boundaries, and distance
- Communicate safely through mutual matching
- Maintain a **3:1 women-to-men ratio at all times**
- Provide a safer alternative to mainstream dating apps

---

## User Roles & States

### User States
- `unverified` — onboarding incomplete
- `verified` — age and photo verified
- `waitlisted` — men only, ratio-controlled
- `active` — full access
- `banned` — no access

### User Flags
- `is_female`
- `has_active_ban`
- `is_special_member` (reserved for future use)

---

## MVP Features (In Scope)

### Identity & Safety
- 18+ age verification
- Email verification
- One account per user
- Immediate ban enforcement
- One-tap block & report

---

### Profile System
**Required**
- At least 1 recent photo
- Age
- Gender
- Coarse location

**Optional**
- Bio
- Kink preference tags (non-graphic, opt-in)

**Photo Rules**
- No explicit nudity
- Recent uploads required

---

### Discovery
- Distance-based discovery
- Age range filtering
- Gender filtering
- Ratio-aware results
- Excludes:
  - Blocked users
  - Banned users
  - Previously skipped users (session-based)

> All discovery logic runs **server-side only**.

---

### Matching
- Mutual interest required
- Matches created automatically
- No unsolicited messages

---

### 1:1 Chat
- Text-only messaging
- Only between matched users
- Block instantly ends chat
- Reports capture recent messages
- Active bans immediately disable messaging

---

### Moderation & Admin
Admins can:
- View reports
- Ban users
- Remove photos
- Lock accounts

Automated controls:
- Multiple reports trigger auto-flagging
- Severe abuse triggers auto-ban

---

## Ratio Enforcement (Non-Negotiable)

**Target Ratio:**  
**3 women : 1 man**

### Enforcement Rules
- Women:
  - Immediate access
  - No waitlist
- Men:
  - May be waitlisted at signup
  - Discovery and messaging throttled if ratio drifts
- Ratio logic enforced **server-side only**
- UI messaging remains soft and respectful

> If the ratio breaks, growth stops.

---

## Explicitly Out of Scope (Locked)

The following features are **not included** in the MVP:

- ❌ Group chat (designed, feature-flagged OFF)
- ❌ Public forums
- ❌ Video uploads
- ❌ Payments or subscriptions
- ❌ Explicit sexual content
- ❌ Searchable groups
- ❌ Events marketplace
- ❌ Profile comments
- ❌ Push notifications (post-MVP)

Any request to add these is deferred to Post-MVP review.

---

## Group Chat (Planned, Disabled)

- Group chat is **planned but not active**
- Backend may exist behind feature flags
- UI and access disabled for all users
- Only Special Members may create groups in the future

> Group chat will **not** be enabled during MVP or closed alpha.

---

## Technical Constraints (MVP)

- Flutter (frontend)
- Supabase (auth, database, storage)
- PostgreSQL RPCs for discovery
- Row-Level Security enforced everywhere
- Free-tier friendly infrastructure

---

## Success Criteria (MVP)

The MVP is successful if:
- Ratio remains within tolerance
- Women report feeling safe
- Abuse is manageable
- Core flows are stable
- Users engage in matches and chat

Growth and revenue are **not** success metrics at this stage.

---

## Change Control

Any change to this document requires:
- Explicit Post-MVP approval
- Abuse and moderation impact review
- Ratio impact review

Until then: **this document is law**.

