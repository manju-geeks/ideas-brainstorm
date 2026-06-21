# Business Requirements Document: Education Tutor Platform (Enhanced)
**Document Version:** 2.1  
**Date:** 21 June 2026  
**Status:** Draft for Review

---

## 1. Introduction
This document outlines the business requirements for a mobile-first education platform designed to connect students (Class 4 onwards) with verified, reliable tutors across India. The platform prioritizes offline tutoring (with online as a strong secondary option) and aims to maximize student learning outcomes while minimizing time investment.

This BRD covers MVP1 (core marketplace with trust, safety, and basic monetization), MVP1.5 (parent-side subscription tier), and outlines the roadmap for MVP2 (AI-driven academic tooling). It is written with sufficient clarity and technical precision to serve as a foundation for AI-assisted application development.

---

## 2. Vision, Goals & KPIs

**Vision:** Helping students with the right education, maximizing results with minimal time.

### Primary KPIs

| KPI | Target | Measurement Method |
|-----|--------|-------------------|
| Learning improvement | 30–50% improvement in grasp, memorization, and logic application | Pre/post assessment surveys (baseline at onboarding, post after 1–2 quarters) |
| Tutor reliability | <10% session cancellation rate | Platform session tracking |
| Student retention | >70% students continue after first free session | Conversion funnel analytics |
| Tutor retention | >60% active tutors retained after 6 months | Monthly activity tracking |
| Parent satisfaction (NPS) | >50 NPS score | In-app survey after every 10 sessions |

### Secondary KPIs
- Average time-to-match (student request → tutor acceptance)
- Tutor verification turnaround time
- Session completion rate
- Rating distribution across tutors

---

## 3. Business Objectives

1. Provide parents/students access to verified, consistent, high-quality academic and language tutors — starting with Bengaluru for offline, pan-India for online.
2. Enable rapid tutor discovery with intelligent matching prioritizing student preferences.
3. Offer flexible learning modes: offline (tutor's home, student's home, or group setting) and online 1-to-1.
4. Build a trust-first platform through rigorous tutor verification, session recordings, ratings, and **same-tutor continuity guarantee with flexible rescheduling**.
5. Differentiate from competitors (e.g., UrbanPro) through:
   - Tutor-when-needed availability
   - Self-help continuity — students don't lose momentum if a tutor is unavailable
   - **Same-tutor continuity guarantee** — flexible rescheduling ensures relationship preservation
   - Transparent, comparable pricing with visible rates
   - First session free — zero-risk trial for parents
   - **Post-session notes upload** — verifiable record of offline sessions
6. Create a sustainable revenue model through tutor subscriptions, dynamic commission margins, and future parent-side subscriptions.

---

## 4. Target Users & Personas

### 4.1. Primary Users

| Persona | Description | Key Needs |
|---------|-------------|-----------|
| Parent | Decision-maker, pays for tutoring, monitors progress | Trustworthy tutors, transparent pricing, progress visibility, convenience |
| Student | Class 4–12, CBSE board, needs academic or language support | Effective teaching, flexible timing, continuity, engaging sessions |
| Tutor | Freelance or part-time educator, subject-matter expert | Steady student flow, fair compensation, professional credibility, scheduling tools |

### 4.2. Internal Users

| Persona | Description |
|---------|-------------|
| Platform Admin | Manages tutor verification, monitors platform health, handles disputes, configures pricing/margins, performs overrides |

---

## 5. Scope

### 5.1. MVP1 — Core Marketplace + Trust + Monetization
- Tutor recruitment, onboarding, and multi-step verification
- Student/parent onboarding with preference capture and pre-assessment survey
- Tutor discovery and intelligent matching (location, subject, availability, ratings)
- Session booking, scheduling, and management
- First session free trial mechanism
- Online sessions via Google Meet with mandatory recording
- Offline session safety features (group class default for new connections, check-in/check-out)
- **Post-session notes upload for offline sessions**
- Rating and review system
- **Session rescheduling & continuity mechanism** (replacing backup tutor arrangement)
- Dynamic pricing with visible rates (tutor rate + platform margin)
- Tutor subscription-based monetization + commission model
- AI-assisted registration validation
- AI-assisted marketing content generation
- Push notifications (SMS, email, WhatsApp)
- Admin dashboard (metrics, monitoring, user management, overrides)
- Informational web presence with app download path

### 5.2. MVP1.5 — Parent Subscription Tier
- Premium parent subscription with benefits (priority matching, detailed progress reports, session recording access, direct tutor communication)

### 5.3. Out-of-Scope for MVP1 (Planned for MVP2)
- AI-based academic tooling (automated exam validation, question paper generation)
- AI-driven PTM automation
- AI-based self-serve classes and topic-specific reminders
- Agentic AI for student caliber assessment
- In-app payment gateway
- In-app video conferencing (using Google Meet externally for MVP1)
- **AI-powered analysis of uploaded session notes**

---

## 6. Functional Requirements — MVP1

### 6.1. Student/Parent Onboarding

| Req ID | Requirement |
|--------|-------------|
| R1.01 | Register via mobile number with OTP verification; email capture mandatory |
| R1.02 | Capture student name, age/class, and school name |
| R1.03 | Capture residential address (street, postal code) with GPS-based geolocation for radius search |
| R1.04 | Select academic board (CBSE for MVP1) and class level (Class 4–12) |
| R1.05 | For students below Class 9: option to upload local school book names and specific topics/chapters for tutor adaptation |
| R1.06 | Select preferred learning mode: offline, online, or both |
| R1.07 | If offline: specify preferred location — student's home, tutor's home, or nearby group setting |
| R1.08 | Select subject preferences (academics and/or language) and language of instruction (default: English) |
| R1.09 | Complete a pre-assessment survey capturing current academic standing, specific subject challenges, learning style preferences, and goals. This establishes the baseline for KPI measurement |
| R1.10 | AI-assisted validation of all registration inputs — mobile number format, address verification against postal code database, duplicate detection |

### 6.2. Tutor Onboarding & Verification

| Req ID | Requirement |
|--------|-------------|
| R2.01 | Register via mobile number with OTP verification; email capture mandatory |
| R2.02 | Capture personal details: full name, photograph (clear face photo, verified against ID) |
| R2.03 | Upload Government ID (Aadhaar, PAN, Voter ID, or Passport) for identity verification |
| R2.04 | Capture educational background: degrees, certifications, institutions attended |
| R2.05 | Capture teaching experience: years of experience, subjects and class levels taught, any institutional affiliations |
| R2.06 | Specify subjects, academic board(s), and class levels offered (e.g., CBSE Class 6–10 Mathematics, Science) |
| R2.07 | Specify language proficiency for instruction: English, Hindi, Kannada |
| R2.08 | Upload or record a demo class video (3–10 minutes) showcasing teaching style on a topic of their choice |
| R2.09 | Specify availability: days of week and time slots (morning, afternoon, evening) |
| R2.10 | Specify preferred teaching mode: offline, online, or both |
| R2.11 | If offline: capture teaching address (with postal code and GPS) and willingness to teach at student's home, own home, or both |
| R2.12 | Set per-session or per-month tutoring rates — visible to platform admin; displayed to parents with platform margin applied |
| R2.13 | Specify number and breadth of subjects covered (used in ranking algorithm) |

#### Verification Workflow

| Req ID | Requirement |
|--------|-------------|
| R2.14 | Step 1 — Automated checks: AI validates mobile OTP, Government ID format/structure, photo-to-ID face match (where feasible), duplicate tutor detection |
| R2.15 | Step 2 — AI-assisted review: AI flags inconsistencies in credentials (e.g., claimed degree vs. institution, experience timeline gaps). Flagged profiles are routed to admin |
| R2.16 | Step 3 — Admin review: Admin reviews flagged items, demo class video quality, and overall profile completeness |
| R2.17 | Step 4 — Status assignment: Tutor receives "Verified" badge upon passing all checks. Unverified tutors are not visible in search results |
| R2.18 | Verification turnaround target: 48 hours from complete submission |

### 6.3. Tutor Discovery & Matching

| Req ID | Requirement |
|--------|-------------|
| R3.01 | Search filters: Subject, Class Level, Academic Board, Mode (offline/online), Language of instruction, Location (offline only — within 5km radius of student's address) |
| R3.02 | Ranking algorithm shall prioritize results based on (weighted, in order of importance): 1. Subject expertise match, 2. Availability alignment with student's preferred timings, 3. Tutor rating (average score from reviews), 4. Breadth of subject coverage matching student needs, 5. Proximity to student (offline only), 6. Verification status and profile completeness |
| R3.03 | If no offline tutors are found within 5km, the platform shall: (a) display a message indicating no nearby offline tutors, (b) automatically show matching online tutors as an alternative, (c) offer option to expand search radius |
| R3.04 | Tutor profile page shall display: verified badge, name, photo, qualifications, experience summary, subjects/classes offered, demo class video, ratings/reviews, availability slots, and displayed rate (tutor rate + platform margin) |
| R3.05 | Students/parents can view and compare multiple tutor profiles side-by-side |
| R3.06 | Students/parents can watch the demo class video directly from the tutor profile before booking |

### 6.4. Pricing & Margin Engine

| Req ID | Requirement |
|--------|-------------|
| R4.01 | Tutors set their own base rate (per session or per month) during registration; this is visible only to admins |
| R4.02 | The platform applies a dynamic margin on top of the tutor's base rate to derive the displayed rate shown to parents |
| R4.03 | Default margin: 20% of tutor's base rate |
| R4.04 | Dynamic margin logic: If the tutor's base rate falls below a configurable market-floor threshold, the margin percentage increases to bring the displayed rate in line with comparable market rates. Admin can configure the floor threshold and maximum margin percentage |
| R4.05 | Parents see only the displayed rate (tutor rate + margin); they can compare across tutors transparently |
| R4.06 | Admin dashboard shall provide margin analytics: average margin %, revenue per session, revenue per tutor, total platform revenue |

### 6.5. Session Management & Booking

| Req ID | Requirement |
|--------|-------------|
| R5.01 | First session free: Every new student-tutor pairing starts with one complimentary session. The tutor is compensated by the platform at a reduced/configurable rate for this session |
| R5.02 | After the free session, the student/parent decides whether to continue. If they decline, they can try another tutor (one free session per unique tutor, capped at 3 free trials total per student) |
| R5.03 | Students/parents send a tutoring request specifying: subject, class, mode, preferred schedule, and location preference (for offline) |
| R5.04 | Tutors receive the request via push notification and can accept or decline within a configurable time window (default: 24 hours) |
| R5.05 | If a tutor doesn't respond within the window, the request automatically cascades to the next-best-matched tutor |
| R5.06 | Upon acceptance, the platform confirms the booking to both parties with session details via push notification (SMS, email, WhatsApp) |
| R5.07 | For online sessions: The platform auto-generates a Google Meet link and shares it with both parties. Session recording is mandatory and stored on the platform |
| R5.08 | For offline sessions: The platform confirms the agreed location. For initial sessions with new tutors, the platform recommends a group setting or a setting with a parent/guardian present |
| R5.09 | Both parties can reschedule or cancel with a minimum notice period (configurable, default: 4 hours). **Cancellation handling routes through Section 6.6 (Session Rescheduling & Continuity) rather than triggering a backup tutor search** |
| R5.10 | Session tracking: platform logs session start/end (self-reported for offline; system-tracked for online via Google Meet API) |

### 6.6. Session Rescheduling & Continuity *(Replaces former Backup Tutor Guarantee)*

**Purpose:** Maintain continuity of the same student-tutor relationship rather than substituting a backup tutor. When either party is unavailable, the session is rescheduled — not reassigned.

| Req ID | Requirement |
|--------|-------------|
| R6.01 | If a tutor is unavailable for a scheduled session (leave, illness, personal reason), they shall mark the session as "unavailable" through the app with a reason |
| R6.02 | If a student is unavailable, the parent/student shall mark the session as "cannot attend" through the app |
| R6.03 | Upon either party marking unavailability, the platform shall immediately notify both parties (push, SMS, WhatsApp) that the session will not take place as scheduled |
| R6.04 | The notification shall include a rescheduling prompt — both student and tutor are invited to propose alternate dates/times |
| R6.05 | The platform shall display the tutor's available time slots and the student's preferred times to facilitate quick rescheduling |
| R6.06 | Either party can propose a reschedule time; the other party confirms or suggests an alternative. This back-and-forth is facilitated in-app (not a full chat — structured slot selection) |
| R6.07 | Once both parties agree on a new time, the session is rescheduled and confirmation notifications are sent to both |
| R6.08 | If rescheduling is not agreed upon within a configurable window (default: 48 hours), the session is marked as "missed" and the admin is notified |
| R6.09 | The platform tracks cancellation and reschedule frequency per tutor. Repeated cancellations (configurable threshold, e.g., >3 in a month) trigger a warning to the tutor and flag for admin review |
| R6.10 | The platform tracks cancellation frequency per student as well (for fairness and pattern detection) |
| R6.11 | No automatic backup tutor assignment. The design prioritizes maintaining the same student-tutor pairing for relationship continuity and consistent learning progress |
| R6.12 | If a tutor becomes permanently unavailable (e.g., deactivates account, is suspended), only then does the platform recommend alternative tutors to the student through the standard matching flow (Section 6.3) |
| R6.13 | **This same-tutor continuity guarantee is a key differentiator and shall be prominently communicated in marketing materials and the onboarding flow** |

### 6.7. Rating & Review System

| Req ID | Requirement |
|--------|-------------|
| R7.01 | After every completed session, the student/parent is prompted to rate the tutor on a 1–5 star scale |
| R7.02 | Rating dimensions: Teaching quality, Punctuality, Communication, Subject knowledge |
| R7.03 | Optional written review (text, up to 500 characters) |
| R7.04 | Tutor's overall rating is a weighted average across all sessions, displayed on their profile |
| R7.05 | Tutors with an average rating below a configurable threshold (e.g., 2.5 stars over 10+ sessions) are flagged for admin review and potential deactivation |
| R7.06 | Tutors can respond to reviews (visible publicly) to maintain fairness |
| R7.07 | AI-assisted review moderation to filter spam, abusive language, or fake reviews |

### 6.8. Pre/Post Assessment & Progress Tracking

| Req ID | Requirement |
|--------|-------------|
| R8.01 | Pre-assessment survey at student registration: captures self-reported (or parent-reported) academic standing, subject-wise confidence levels (1–5 scale), specific weak areas, and learning goals |
| R8.02 | Post-assessment survey triggered after the first quarter (configurable, e.g., after 20 sessions or 3 months): same dimensions as pre-assessment to measure improvement |
| R8.03 | The platform generates a progress snapshot comparing pre and post scores, contributing directly to the 30–50% KPI measurement |
| R8.04 | Progress snapshots are visible to parents and shared with the tutor (with parent consent) |
| R8.05 | Aggregate anonymized assessment data feeds into the admin dashboard for platform-wide KPI tracking |

### 6.9. Safety & Trust Features

| Req ID | Requirement |
|--------|-------------|
| R9.01 | Mandatory session recording for all online sessions conducted via Google Meet. Recordings stored securely with access limited to parent, tutor, and admin |
| R9.02 | Recordings retained for a configurable period (default: 90 days) and auto-deleted thereafter unless flagged |
| R9.03 | For offline sessions with new tutors, the platform recommends group settings or parent/guardian presence. This recommendation is displayed prominently during booking confirmation |
| R9.04 | Post-session safety feedback: After every offline session, the parent receives a brief check-in prompt ("How did the session go? Any concerns?") via push notification |
| R9.05 | An emergency/report button is accessible at all times within the app, allowing parents or students to flag safety concerns. Flagged reports are escalated to admin immediately |
| R9.06 | Emergency contact capture: Parent's alternate phone number is collected during registration for safety communication |
| R9.07 | Tutors with any safety-related complaint undergo immediate review; their profile is temporarily suspended pending investigation |

### 6.10. AI-Assisted Platform Operations

| Req ID | Requirement |
|--------|-------------|
| R10.01 | Registration AI: Validates input formats (mobile, email, postal code), parses uploaded Government ID documents to extract name and ID number, performs photo-to-ID face matching (basic), detects duplicate registrations across tutor and student databases |
| R10.02 | Credential Review AI: Flags inconsistencies in tutor applications (education claims, experience timelines) for admin attention. Does not auto-reject — all flags go to human review |
| R10.03 | Marketing AI: Generates social media post content (Instagram, Facebook, WhatsApp status), email campaign drafts for lead outreach, and identifies target demographics based on educational trend data and platform usage patterns |
| R10.04 | Review Moderation AI: Screens submitted reviews for spam, profanity, and potentially fake content; flags for admin review rather than auto-deleting |

### 6.11. Notifications & Communication

| Req ID | Requirement |
|--------|-------------|
| R11.01 | Multi-channel notifications: Push notifications (in-app), SMS, Email, and WhatsApp |
| R11.02 | Notification triggers include: OTP delivery, registration confirmation, booking request received/accepted/declined, session reminders (24 hours and 1 hour before), session cancellation/reschedule, **rescheduling prompts and confirmations**, rating prompt post-session, safety check-in (offline), **notes upload reminder (30 min after offline session)**, admin communications |
| R11.03 | Users can configure notification preferences (channel selection) in their profile settings |
| R11.04 | WhatsApp integration via WhatsApp Business API for transactional messages |

### 6.12. Admin Dashboard

| Req ID | Requirement |
|--------|-------------|
| R12.01 | Tutor Management: View all tutors, filter by verification status, location, subject, rating. Approve/reject/suspend tutor profiles. View tutor rates and applied margins |
| R12.02 | Student Management: View all registered students, filter by class, location, active/inactive status. View session history per student |
| R12.03 | Session Monitoring: View all scheduled, completed, and cancelled sessions. Identify patterns (e.g., high cancellation tutors, low-engagement students). **View rescheduling history and missed sessions** |
| R12.04 | Revenue & Pricing: View total revenue, revenue per tutor, revenue per session. Configure base margin percentage, market-floor rate thresholds, and maximum margin caps |
| R12.05 | KPI Dashboard: Platform-wide metrics — total users, active users, sessions completed, average rating, pre/post assessment improvement scores, NPS, tutor retention rate, student conversion rate (free → paid) |
| R12.06 | Safety & Escalation: View flagged safety reports, review moderation queue, tutor suspension management |
| R12.07 | Override Capabilities: Admin can manually adjust tutor ratings (with reason logging), override pricing for specific tutors, **manually mark sessions as rescheduled or missed**, and manage user account status |
| R12.08 | Marketing Insights: View campaign performance metrics, lead conversion data, and AI-generated content drafts for approval |

### 6.13. Post-Session Notes Upload (Offline Trust & Authenticity) *(NEW)*

**Purpose:** Strengthen trust in offline tutoring by creating a verifiable record of what was covered in each session. Notes also serve as a foundation for future AI-driven performance evaluation (MVP2).

| Req ID | Requirement |
|--------|-------------|
| R13.01 | After every offline session, the student (or parent) shall have the option to upload session notes (photos of handwritten notes, typed summaries, or scanned pages) via the app |
| R13.02 | Uploads shall support image formats (JPEG, PNG) and PDF. Multiple pages per session allowed (up to 10 files, max 5MB each) |
| R13.03 | Uploaded notes are tagged to the specific session (date, tutor, subject, topic) and stored securely in the student's session history |
| R13.04 | Parents can access all uploaded notes for their child at any time through the app — organized by date, subject, and tutor |
| R13.05 | Tutors can view notes uploaded for their own sessions (useful for continuity planning) |
| R13.06 | For MVP1, the platform extracts and stores the notes only — no AI analysis or performance evaluation is performed on the content |
| R13.07 | Notes are retained for the duration of the student's active account and made available for future AI-based extraction and evaluation (MVP2 scope) |
| R13.08 | A gentle push notification reminder is sent to the student/parent 30 minutes after a scheduled offline session ends, prompting them to upload notes |
| R13.09 | Session records in the admin dashboard and progress tracking indicate whether notes were uploaded (completeness indicator) |

#### MVP2 Future Use of Notes
- AI-powered OCR and content extraction from handwritten notes
- Topic coverage mapping against NCERT syllabus
- Automatic identification of weak areas based on notes quality and coverage
- Input into the pre/post assessment improvement KPI

---

## 7. Non-Functional Requirements

| Category | Requirement | Target |
|----------|-------------|--------|
| Performance | Tutor search results load time | < 2 seconds |
| Performance | App cold start time | < 3 seconds |
| Performance | Notification delivery (push/SMS) | < 10 seconds |
| Scalability | Concurrent users supported at launch | 5,000+ |
| Scalability | Architecture designed for horizontal scaling | Microservices or modular monolith |
| Availability | Platform uptime | 99.5% |
| Security | Data encryption | AES-256 at rest, TLS 1.3 in transit |
| Security | Authentication | OTP-based, session tokens with expiry |
| Security | Government ID storage | Encrypted, access-restricted to verification workflow only |
| Security | Session recordings | Encrypted storage, role-based access (parent, tutor, admin) |
| **Security** | **Session notes storage** | **Encrypted, role-based access (parent, tutor, admin)** |
| Compliance | Indian data privacy | Compliance with Digital Personal Data Protection Act (DPDPA) 2023 |
| Compliance | Payment data | PCI-DSS compliance when payment gateway is integrated (MVP2) |
| Usability | Accessibility | WCAG 2.1 Level AA for core user flows |
| Usability | Language support (UI) | English (MVP1); Hindi, Kannada planned for MVP2 |
| Maintainability | Code quality | Documented, modular, CI/CD pipeline, automated testing (>70% coverage) |

---

## 8. Technical Architecture — High Level

### 8.1. Platform Type
- **Mobile-first:** Native Android and iOS apps (React Native or Flutter for cross-platform efficiency)
- **Web:** Informational/marketing website with app download links, basic SEO landing pages. Not a full web app for MVP1

### 8.2. Architecture Components

**Client Layer**
- Mobile App - Android/iOS
- Informational Website

**API Gateway**
- API Gateway / Load Balancer

**Backend Services**
- Auth Service - OTP, Sessions
- User Service - Profiles, Preferences
- Matching & Search Service
- Session & Booking Service
- **Session Rescheduling Service**
- Pricing & Margin Engine
- Notification Service - SMS, Email, WhatsApp, Push
- Rating & Review Service
- Assessment & Survey Service
- Safety & Reporting Service
- **Session Notes Service** *(NEW)*
- AI Registration Validator
- AI Marketing Content Generator
- AI Review Moderator
- Admin Dashboard Service

**Data Layer**
- Primary Database - PostgreSQL
- Cache - Redis
- Object Storage - S3/GCS for recordings, IDs, demo videos, **session notes**
- Search Index - Elasticsearch

**External Integrations**
- Google Meet API
- Google Maps / Geocoding API
- SMS Gateway - e.g., Twilio, MSG91
- WhatsApp Business API
- Email Service - e.g., SendGrid
- ID Verification API - optional

### 8.3. Key Technology Recommendations

| Component | Recommended Stack | Rationale |
|-----------|------------------|-----------|
| Mobile App | Flutter (Dart) | Single codebase for Android + iOS, strong UI toolkit, good performance |
| Backend | Python (FastAPI) or Node.js (NestJS) | FastAPI for AI integration ease; NestJS for TypeScript consistency with Flutter/Dart ecosystem |
| Database | PostgreSQL | Relational integrity for user profiles, sessions, ratings; PostGIS extension for geospatial queries (5km radius) |
| Search | Elasticsearch | Fast, weighted, full-text search for tutor discovery and ranking |
| Cache | Redis | Session tokens, frequently accessed tutor search results, rate limiting |
| Object Storage | AWS S3 or Google Cloud Storage | Demo videos, Government IDs, session recordings, **session notes** |
| AI Services | OpenAI API / Google Gemini API | Registration validation (document parsing, face matching), marketing content generation, review moderation |
| Geolocation | Google Maps Platform (Geocoding + Distance Matrix) | Address-to-coordinates, radius-based search |
| Video Conferencing | Google Meet (via Google Calendar API) | Auto-create Meet links for scheduled sessions |
| Notifications | Firebase Cloud Messaging (push), MSG91 or Twilio (SMS), SendGrid (email), WhatsApp Business API | Multi-channel delivery |
| Hosting | AWS or GCP | Auto-scaling, managed services, AI/ML integration |
| CI/CD | GitHub Actions or GitLab CI | Automated build, test, deploy pipeline |

### 8.4. Data Model — Core Entities

**STUDENT**
- id (uuid, PK)
- name (string)
- mobile (string)
- email (string)
- school_name (string)
- class_level (int)
- board (string)
- address (string)
- postal_code (string)
- latitude (float)
- longitude (float)
- preferred_mode (string)
- preferred_location (string)
- subject_preferences (json)
- language_preference (string)
- pre_assessment (json)
- post_assessment (json)
- created_at (timestamp)

**TUTOR**
- id (uuid, PK)
- name (string)
- mobile (string)
- email (string)
- photo_url (string)
- govt_id_url (string)
- education_background (json)
- teaching_experience (json)
- subjects_offered (json)
- class_levels (json)
- board (string)
- languages (json)
- demo_video_url (string)
- availability (json)
- preferred_mode (string)
- teaching_address (string)
- postal_code (string)
- latitude (float)
- longitude (float)
- base_rate (decimal)
- verification_status (string)
- average_rating (float)
- total_reviews (int)
- **cancellation_count** (int) *(NEW)*
- created_at (timestamp)

**SESSION**
- id (uuid, PK)
- student_id (uuid, FK)
- tutor_id (uuid, FK)
- subject (string)
- class_level (int)
- mode (string)
- location_type (string)
- location_address (string)
- meet_link (string)
- recording_url (string)
- scheduled_start (timestamp)
- scheduled_end (timestamp)
- actual_start (timestamp)
- actual_end (timestamp)
- status (string) — *includes "rescheduled", "missed"*
- **rescheduled_from** (uuid, FK, nullable) *(NEW)*
- **reschedule_reason** (string, nullable) *(NEW)*
- **notes_uploaded** (boolean) *(NEW)*
- is_free_trial (boolean)
- created_at (timestamp)

**SESSION_NOTES** *(NEW)*
- id (uuid, PK)
- session_id (uuid, FK)
- student_id (uuid, FK)
- tutor_id (uuid, FK)
- file_url (string)
- file_type (string) — JPEG, PNG, PDF
- file_size (int)
- subject (string)
- topic (string, nullable)
- uploaded_at (timestamp)

**BOOKING_REQUEST**
- id (uuid, PK)
- student_id (uuid, FK)
- tutor_id (uuid, FK)
- subject (string)
- mode (string)
- preferred_schedule (json)
- location_preference (string)
- status (string)
- expires_at (timestamp)
- created_at (timestamp)

**RESCHEDULE_REQUEST** *(NEW)*
- id (uuid, PK)
- session_id (uuid, FK)
- requested_by (string) — "tutor" or "student"
- reason (string)
- proposed_times (json)
- status (string) — "pending", "accepted", "counter_proposed", "expired"
- expires_at (timestamp)
- created_at (timestamp)

**RATING**
- id (uuid, PK)
- session_id (uuid, FK)
- student_id (uuid, FK)
- tutor_id (uuid, FK)
- teaching_quality (int)
- punctuality (int)
- communication (int)
- subject_knowledge (int)
- overall_score (float)
- review_text (string)
- tutor_response (string)
- moderation_status (string)
- created_at (timestamp)

**PRICING**
- id (uuid, PK)
- tutor_id (uuid, FK)
- base_rate (decimal)
- margin_percentage (float)
- displayed_rate (decimal)
- market_floor (decimal)
- effective_from (timestamp)

**SAFETY_REPORT**
- id (uuid, PK)
- reporter_id (uuid, FK)
- reported_tutor_id (uuid, FK)
- session_id (uuid, FK)
- report_type (string)
- description (string)
- status (string)
- admin_notes (string)
- created_at (timestamp)

**NOTIFICATION_LOG**
- id (uuid, PK)
- user_id (uuid, FK)
- channel (string)
- type (string) — *includes "reschedule_prompt", "notes_reminder"*
- content_summary (string)
- delivery_status (string)
- sent_at (timestamp)

---

## 9. Monetization Strategy

### MVP1 Revenue Model

| Revenue Stream | Description | Details |
|---------------|-------------|---------|
| Tutor Subscription | Monthly/annual fee for tutors to list on the platform | Tiered: Basic listing vs. Featured/boosted profile (featured planned for MVP1.5) |
| Session Commission | Platform margin applied on top of tutor's base rate | Default 20%; dynamic increase for below-market-rate tutors to match market floor |
| First Session Subsidy | Platform pays tutor a reduced rate for the free first session | Cost of acquisition — tracked as marketing spend |

### MVP1.5 Addition

| Revenue Stream | Description |
|---------------|-------------|
| Parent Premium Subscription | Monthly fee for: priority matching, detailed progress reports, session recording access, direct communication channel with tutor |

### Unit Economics Target (MVP1)

| Metric | Target |
|--------|--------|
| Average session price (displayed to parent) | ₹400–800 per session |
| Platform margin per session | ₹80–160 (at 20%) |
| Tutor subscription (monthly) | ₹299–499 |
| Free trial cost per student (platform bears) | ₹200–400 (1–3 free sessions) |
| Target break-even | 500 active student-tutor pairs |

---

## 10. Competitive Differentiation

| Feature | This Platform | UrbanPro |
|---------|--------------|----------|
| First session free | ✅ Zero-risk trial | ❌ |
| **Same-tutor continuity with flexible rescheduling** | ✅ Relationship preserved; no random substitutes | ❌ |
| **Post-session notes upload for offline trust** | ✅ Verifiable record of every session | ❌ |
| Mandatory session recording (online) | ✅ Trust & safety | ❌ |
| Pre/post learning assessment | ✅ Measurable outcomes | ❌ |
| Dynamic pricing with transparent comparison | ✅ Parents compare displayed rates | Limited |
| Offline safety recommendations | ✅ Group setting prompts, post-session check-in | ❌ |
| AI-assisted tutor verification | ✅ Multi-step automated + human review | Basic manual |
| Tutor subject coverage ranking | ✅ Multi-subject tutors ranked higher | Basic filters |
| WhatsApp notifications | ✅ Native integration | ❌ |

---

## 11. User Flows — Key Journeys

### 11.1. Student/Parent Journey

```
Download App
    ↓
Register - Mobile OTP + Email
    ↓
Fill Profile - Name, Class, School, Address, Board
    ↓
Set Preferences - Mode, Location, Subjects, Language
    ↓
Complete Pre-Assessment Survey
    ↓
Search for Tutors
    ↓
Tutors Found? ─── No Offline in 5km ──→ Platform Suggests Online Tutors
    ↓ Yes - Offline
Browse Profiles, Watch Demo Videos, Compare Rates
    ↓
Send Booking Request to Tutor
    ↓
Tutor Accepts? ─── No / Timeout ──→ Auto-cascade to Next Tutor
    ↓ Yes
First Free Session Scheduled
    ↓
Attend Session
    ↓
[If Offline] Upload Session Notes (Optional, Prompted)
    ↓
Continue with Tutor? ─── No ──→ Free Trials Left? ─── No ──→ Book Paid Session with New Tutor
    ↓ Yes                              ↓ Yes
Book Regular Sessions - Paid           (Return to Search)
    ↓
Rate & Review After Each Session
    ↓
Post-Assessment After 1 Quarter
```

**On Tutor Unavailability (Updated Flow):**
```
Tutor Marks Session "Unavailable"
    ↓
Platform Notifies Both Parties
    ↓
Rescheduling Prompt Sent
    ↓
Both Parties Propose/Confirm New Time
    ↓
Agreed Within 48 Hours? ─── No ──→ Session Marked "Missed", Admin Notified
    ↓ Yes
Session Rescheduled, Confirmation Sent
```

### 11.2. Tutor Journey

```
Download App
    ↓
Register - Mobile OTP + Email
    ↓
Fill Profile - Name, Photo, Education, Experience
    ↓
Upload Government ID
    ↓
Specify Subjects, Classes, Board, Languages
    ↓
Upload Demo Class Video
    ↓
Set Availability & Location Preferences
    ↓
Set Base Rate
    ↓
Submit for Verification
    ↓
AI Automated Checks - ID, Duplicates, Consistency
    ↓
Admin Review - Credentials, Demo Video
    ↓
Approved? ─── No ──→ Feedback Sent - Resubmit or Reject
    ↓ Yes
Profile Goes Live with Verified Badge
    ↓
Receive Booking Requests
    ↓
Accept? ─── No ──→ Request Cascades to Next Tutor
    ↓ Yes
Session Confirmed - Notification Sent
    ↓
[If Unavailable] Mark Session "Unavailable" → Rescheduling Flow (Section 6.6)
    ↓
Conduct Session
    ↓
[If Offline] View Uploaded Notes (for continuity)
    ↓
Receive Rating & Review
    ↓
Respond to Review if Desired
```

---

## 12. Risk Assessment & Mitigation

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| Tutor-student disintermediation (going off-platform) | High — revenue loss | High | **Same-tutor continuity model creates platform dependency** — students value the relationship AND the rescheduling convenience; progress tracking data locked to platform; notes history only available on-platform |
| Insufficient tutor supply at launch (Bengaluru) | High — poor student experience | Medium | Aggressive tutor onboarding campaign pre-launch; offer first 3 months subscription-free for early tutors; referral bonuses |
| Safety incident during offline session | Critical — trust & legal | Low | Group setting recommendation for new pairs; post-session safety check-in; emergency report button; admin escalation; session recording for online; **notes upload creates accountability trail** |
| Low student conversion (free → paid) | High — revenue impact | Medium | Cap free trials at 3 per student; ensure high-quality first sessions by featuring top-rated tutors; follow-up notifications after free session |
| Tutor quality inconsistency | Medium — reputation damage | Medium | Multi-step verification; rating system with minimum threshold; admin review triggers; demo class pre-screening |
| Google Meet dependency | Medium — service disruption | Low | Monitor Google Meet API reliability; plan fallback (e.g., Zoom API integration) for MVP2 |
| Data privacy breach | Critical — legal & trust | Low | DPDPA compliance; encryption at rest and in transit; minimal data collection; regular security audits |
| **High rescheduling/cancellation rates** | Medium — user frustration | Medium | **Track cancellation frequency per tutor and student; warnings and admin flags for repeated cancellations; missed session tracking** |

---

## 13. Go-to-Market Strategy (MVP1)

### Phase 1 — Pre-Launch (Weeks 1–4)
- AI-generated social media content targeting Bengaluru parent communities (Facebook groups, WhatsApp groups, Instagram)
- Email outreach to tutoring leads sourced from existing directories and education forums
- Tutor recruitment drive: onboard 50–100 verified tutors across key subjects before student-facing launch
- Landing page (web) with waitlist and app download links

### Phase 2 — Soft Launch (Weeks 5–8)
- Invite-only launch for 200–500 students in select Bengaluru pin codes
- **"Same trusted tutor, flexible scheduling"** prominently marketed alongside "First session free"
- Collect feedback, iterate on matching algorithm and UX
- Referral program: existing users invite friends for bonus free sessions

### Phase 3 — Public Launch (Week 9+)
- Open registration for all Bengaluru (offline) and pan-India (online)
- Sustained social media and WhatsApp marketing via AI-generated content
- Track KPIs weekly; report to stakeholders monthly

---

## 14. Success Criteria — MVP1

| Metric | Target (first 6 months) |
|--------|------------------------|
| Verified tutors onboarded | 200+ |
| Registered students | 1,000+ |
| Sessions completed | 5,000+ |
| Free-to-paid conversion rate | >50% |
| Average tutor rating | >4.0 / 5.0 |
| Tutor retention (6-month) | >60% |
| Student retention (active after 3 months) | >50% |
| Pre/post assessment improvement (early signal) | >20% average improvement |
| Platform NPS | >50 |
| **Rescheduling success rate** | **>80% of cancelled sessions successfully rescheduled** |
| **Notes upload rate (offline sessions)** | **>30% of offline sessions have notes uploaded** |

---

## 15. MVP2 Roadmap Preview

| Feature | Description | Priority |
|---------|-------------|----------|
| AI Exam Engine | Automated question paper generation aligned to CBSE syllabus (Class 9–12); AI-validated student answers with scoring | High |
| AI PTM Automation | Platform analyzes session data and assessment scores to auto-generate PTM reports; schedules parent-tutor meetings | High |
| AI Self-Serve Learning | Personalized topic-specific revision modules; AI identifies weak areas from assessments and recommends micro-lessons | High |
| **AI Notes Analysis** | **AI-powered OCR and content extraction from uploaded session notes; topic coverage mapping against NCERT syllabus; weak area identification** | **High** |
| AI Reminders | Smart reminders for revision, upcoming exams, and practice sessions based on student's learning patterns | Medium |
| Agentic Tutoring AI | AI agents that assess student caliber, provide real-time recommendations, and simulate case study exercises | Medium |
| In-App Payments | Integrated payment gateway (Razorpay/PayU) for seamless in-app transactions | High |
| In-App Messaging | Secure chat between students/parents and tutors within the platform | Medium |
| Multi-Language UI | Hindi and Kannada interface support | Medium |

---

## 16. Assumptions & Dependencies

### Assumptions
- Parents have smartphones (Android or iOS) and basic internet connectivity
- Tutors are willing to undergo a verification process, including Government ID submission
- Google Meet API provides reliable session recording capabilities for MVP1
- Indian postal code data is sufficiently accurate for 5km radius geolocation matching
- The 20% default margin is competitive and acceptable to tutors entering the platform
- **Students/parents will adopt the habit of uploading session notes for offline sessions**
- **Both tutors and students will engage constructively with the rescheduling flow**

### Dependencies
- Google Meet API availability and recording feature access
- WhatsApp Business API approval and integration timeline
- SMS gateway provider setup (MSG91 / Twilio)
- Government ID verification API availability

---

## Appendix: Change Log from v2.0

| Section | Change |
|---------|--------|
| Section 3 — Business Objectives | Updated differentiator from "Backup tutor guarantee" to "Same-tutor continuity guarantee with flexible rescheduling"; added "Post-session notes upload" |
| Section 5.1 — MVP1 Scope | Added "Post-session notes upload for offline sessions"; replaced "Backup tutor arrangement" with "Session rescheduling & continuity mechanism" |
| Section 5.3 — Out of Scope | Added "AI-powered analysis of uploaded session notes" |
| Section 6.5 — Session Management (R5.09) | Updated cancellation handling to route through Section 6.6 |
| Section 6.6 | **Completely replaced** — Former "Backup Tutor Guarantee" (R6.01–R6.04) replaced with "Session Rescheduling & Continuity" (R6.01–R6.13) |
| Section 6.11 — Notifications | Added "reschedule prompts and confirmations" and "notes upload reminder" triggers |
| Section 6.12 — Admin Dashboard | Added rescheduling history, missed session viewing, and manual override for session status |
| **Section 6.13 (NEW)** | Added "Post-Session Notes Upload" requirements (R13.01–R13.09) |
| Section 7 — Non-Functional | Added security requirement for session notes storage |
| Section 8.2 — Architecture | Added "Session Rescheduling Service" and "Session Notes Service" |
| Section 8.4 — Data Model | Added SESSION_NOTES entity; added RESCHEDULE_REQUEST entity; updated SESSION with rescheduling and notes fields; added cancellation_count to TUTOR |
| Section 10 — Competitive Differentiation | Replaced "Backup tutor guarantee" row; added "Post-session notes upload" row |
| Section 11 — User Flows | Updated student journey to include notes upload; updated tutor unavailability path to "Reschedule" instead of "Auto-cascade to backup" |
| Section 12 — Risk Assessment | Updated "Tutor-student disintermediation" mitigation to reference continuity model; added "High rescheduling/cancellation rates" risk |
| Section 13 — Go-to-Market | Updated marketing messaging to "Same trusted tutor, flexible scheduling" |
| Section 14 — Success Criteria | Added "Rescheduling success rate" and "Notes upload rate" metrics |
| Section 15 — MVP2 Roadmap | Added "AI Notes Analysis" feature |
| Section 16 — Assumptions | Added assumptions for notes upload and rescheduling adoption |
