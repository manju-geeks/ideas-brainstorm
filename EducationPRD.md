#B2B or B2C or B2B.
#1 - Education platform(Both);
    vision - Helping students with the right education maximizing the results with minimal time. 
    KPI    - 30-50% improvement in child's ability to grasp, memorize and apply logic.
    mvp    -  find local (5kms radius) tutors for students (online/offline).
              usually parents prefer offline instead of online, provide options to choose place.
              online is also an option for 1-1.
              primarlily serve the academics - cbse (class 4 onwards) NCERT commmon syllabus, also tailored to local school books for below class 9.
              specialized tution on languages - english upskilling, kannada, hindi.
              use AI for registration, marketing, building the app.
    mvp2 - AI based tooling primarlily serve the academics - cbse (class 9, 10, 11, 12) NCERT commmon syllabus.
           AI based to conduct exam validate and provided automated opportunties for ptm.
           AI based reminders and self serve classes for improving particular topic.
        
Business Requirements Document: Education Platform
1. Introduction
This document outlines the business requirements for a new education platform designed to connect students with reliable and skilled tutors in India. The platform's core objective is to maximize student learning outcomes and results while minimizing time investment. This BRD details the initial Minimum Viable Product (MVP) focusing on tutor discovery and connection, with future phases incorporating advanced AI-driven academic support.

2. Vision & Goals
Vision Statement: Helping students with the right education, maximizing results with minimal time.

Key Performance Indicators (KPIs):

30-50% improvement in a child's ability to grasp, memorize, and apply logic in academic subjects.
Increased student engagement and reduced learning time for specific topics.
High tutor and student retention rates.
Positive feedback from parents regarding tutor reliability and effectiveness.
3. Business Objectives
To provide an accessible and efficient platform for parents/students to find verified, consistent, and high-quality academic and language tutors.
To enable quick connections with relevant tutors, especially for offline learning within a specified radius.
To offer flexible learning options (offline and online 1-to-1) to cater to diverse parent preferences.
To leverage AI for streamlined platform operations, including tutor/student registration and targeted marketing.
To differentiate from competitors like UrbanPro by focusing on "tutor when needed," self-help continuity, and robust tutor vetting.
To create a scalable foundation for future AI-driven personalized learning and assessment tools.
4. Scope
4.1. In-Scope for MVP1
The initial MVP will focus on establishing a functional marketplace connecting students with tutors, primarily covering academic subjects and specialized language upskilling.

Tutor Recruitment & Verification: Onboarding and thorough verification of tutors.
Student-Tutor Matching: Functionality to search for and connect with tutors based on specified criteria.
Offline/Online Tutoring Facilitation: Tools to arrange and manage both offline and online 1-to-1 sessions.
Core Academic Subjects: CBSE (Class 4 onwards) NCERT common syllabus, with adaptation for local school books below Class 9.
Specialized Language Tutoring: English upskilling, Kannada, and Hindi.
Platform Operations Support: AI-assisted registration and marketing.
Basic Monetization: Subscription for tutors, commission from student payments.
4.2. Out-of-Scope for MVP1 (Planned for future phases, e.g., MVP2)
Advanced AI-based academic tooling (e.g., automated exam validation, PTM opportunities, self-serve class reminders as described in MVP2).
AI-driven agentic tutoring or advanced student caliber assessment.
Complex pricing models beyond the initial flat commission.
In-platform chat or communication tools beyond initial booking requests.
Integrated payment gateway for direct student-tutor financial transactions.
5. Functional Requirements (MVP1)
5.1. User Management & Onboarding
5.1.1. Student/Parent Onboarding
R1.1.1: The platform shall allow students/parents to register using their mobile number (OTP verification) and email.
R1.1.2: The platform shall capture student's name, age/class, and school name during registration.
R1.1.3: The platform shall capture the student's residential address (including postal code) to facilitate geo-location-based tutor search.
R1.1.4: The platform shall allow students/parents to specify their academic board (e.g., CBSE) and specific class level (e.g., Class 7).
R1.1.5: For students below Class 9, the platform shall provide an option to upload local school book names and topics for adaptation by tutors.
R1.1.6: The platform shall allow students/parents to specify their preferred mode of learning (offline, online, or both).
R1.1.7: If offline is preferred, the platform shall allow students/parents to specify preferred tutoring location options (student's home, tutor's home, or potentially a neutral public space if implemented).
R1.1.8: The platform shall allow students/parents to specify subject preferences and any language preferences for tutoring (e.g., instruction in English).
5.1.2. Tutor Onboarding & Verification
R1.2.1: The platform shall allow tutors to register using their mobile number (OTP verification) and email.
R1.2.2: The platform shall capture the tutor's personal details (name, photograph).
R1.2.3: The platform shall capture tutor's identity proof (e.g., Government ID) for verification.
R1.2.4: The platform shall collect detailed information on the tutor's educational background (degrees, institutions).
R1.2.5: The platform shall collect details of the tutor's teaching experience (years, subjects taught).
R1.2.6: The platform shall require tutors to specify subjects, academic boards (e.g., CBSE), and class levels they teach (e.g., Class 4-12 Math, Science).
R1.2.7: The platform shall require tutors to specify language proficiency for teaching (e.g., English, Hindi, Kannada).
R1.2.8: The platform shall allow tutors to upload/record a demo class video to showcase their teaching style.
R1.2.9: The platform shall allow tutors to specify their availability (days, time slots).
R1.2.10: The platform shall allow tutors to specify their preferred mode of teaching (offline, online, or both).
R1.2.11: If offline, the platform shall capture the tutor's residential/teaching address (including postal code) and options for tutoring location (tutor's home, student's home).
R1.2.12: The platform shall allow tutors to set their tutoring rates, which will be visible only to platform administrators initially.
R1.2.13: The platform shall implement a robust administrative verification process for all tutor credentials, including identity, educational background, and demo class review.
R1.2.14: The platform shall assign a "Verified" status to tutors who successfully pass all verification checks.
5.2. Tutor Discovery & Matching
R1.2.15: The platform shall allow students/parents to search for tutors based on:
Subject
Class Level
Academic Board (e.g., CBSE)
Location (for offline, within a 5km radius of the student's address based on postal code/GPS)
Mode of teaching (offline, online)
Language of instruction
R1.2.16: The platform shall rank search results primarily based on:
Subject expertise
Availability of timing
Tutor ratings/reviews (once available)
Coverage of subjects that match student needs
Proximity (for offline tutors)
R1.2.17: If no offline tutors are available within the 5km radius for a student's preferred criteria, the platform shall automatically suggest suitable online tutors as an alternative.
R1.2.18: The platform shall display detailed tutor profiles including their verified credentials, experience, subjects taught, demo class video, and availability.
5.3. Session Management & Booking
R1.3.1: The platform shall allow students/parents to send tutoring requests to selected tutors.
R1.3.2: Tutoring requests shall include preferred subject, class, mode (offline/online), desired start date/time, and preferred location details (for offline).
R1.3.3: Tutors shall be able to accept or decline tutoring requests based on their availability and preferences.
R1.3.4: Upon acceptance, the platform shall facilitate sharing of contact information (if appropriate and compliant with privacy policies) to finalize session logistics.
R1.3.5: For online 1-to-1 sessions, the platform shall generate and provide Google Meet links for scheduled sessions.
R1.3.6: The platform shall allow for basic scheduling and tracking of past and upcoming sessions.
5.4. Content & Curriculum
R1.4.1: The platform shall support academic tutoring for CBSE (Class 4 onwards) following the NCERT common syllabus.
R1.4.2: For students below Class 9, tutors shall be expected to adapt their teaching to local school books and topics, which students can provide details for.
R1.4.3: The platform shall facilitate specialized language tutoring including English upskilling (grammar, spoken English, exam writing skills, handwriting), Kannada, and Hindi.
R1.4.4: Language tutors shall cater to the same age/class groups as academic tutors.
5.5. AI-Assisted Platform Operations
R1.5.1: AI for Registration: AI components shall assist in validating registration details for both students and tutors (e.g., checking for valid mobile numbers, structured data parsing from documents, cross-referencing information where possible).
R1.5.2: AI for Marketing: AI tools shall be used to generate initial marketing content for social media posts, email outreach campaigns, and target audience identification based on educational trends and demographics. This will focus on go-to-market strategies and lead generation.
6. Non-Functional Requirements (MVP1)
Performance:
Tutor search results should load within 2 seconds.
Platform navigation should be responsive and fluid.
Security:
All user data (personal information, addresses, credentials) must be securely stored and transmitted (e.g., encryption at rest and in transit).
Robust authentication (OTP) and authorization mechanisms.
Compliance with relevant Indian data privacy regulations.
Scalability:
The platform architecture should be designed to handle a growing number of users (students and tutors) and tutoring sessions.
Usability:
Intuitive and easy-to-use interface for both students/parents and tutors.
Clear instructions and feedback for all user actions.
Availability:
The platform should aim for 99.5% uptime.
Maintainability:
The codebase should be well-structured, documented, and easy to maintain and extend for future features.
7. Technical Requirements (MVP1 - High-Level Architecture Considerations)
Frontend Technologies: To be determined (e.g., React, Angular, Vue.js for web; React Native, Flutter for mobile app). The goal is a highly functional web and mobile application.
Backend Technologies: To be determined (e.g., Python/Django, Node.js/Express, Java/Spring Boot).
Database: To be determined (e.g., PostgreSQL, MongoDB) capable of handling structured and semi-structured data for user profiles, session data, and verification documents.
Cloud Platform: To be determined (e.g., AWS, Azure, GCP) for hosting, scalability, and AI services integration.
AI Integration Frameworks: Integration with relevant AI/ML libraries and APIs for registration validation, content generation, and potentially initial recommender systems.
Google Meet API: Integration for scheduling and launching online sessions.
Geolocation Services: Integration with mapping APIs (e.g., Google Maps API) for address validation and radius-based search.
8. Monetization Strategy (MVP1)
Tutor Subscription Fees: Tutors will pay a monthly or annual subscription fee to be listed and accessible on the platform.
Commission-Based Revenue: The platform will take a predefined percentage commission from the fees paid by students/parents to tutors for successful sessions.
Pricing Consistency: For MVP1, a consistent pricing structure will be applied where tutors provide rates, and the platform calculates its commission.
9. Success Criteria
The MVP1 will be considered successful if it achieves the following:

Successful onboarding and verification of a target number of tutors across key regions in India.
Successful registration of an initial user base of students/parents.
A measurable number of successful tutoring connections and completed sessions.
Positive feedback from early adopters regarding ease of use and tutor quality.
Demonstrable use of AI for streamlining registration and generating initial marketing output.
Establishment of foundational metrics for tracking KPI progress towards the 30-50% improvement goal in later phases.
10. Future Enhancements (MVP2 and Beyond)
AI-Based Academic Tooling (Class 9-12):
Automated assessment tools (e.g., exam validation, personalized practice questions).
AI-generated automated opportunities for Parent-Teacher Meetings (PTM) based on student progress.
AI-based reminders and self-serve classes/modules for improving specific weak topics.
Advanced AI-Driven Tutoring:
Agentic AI models to assess student caliber and provide personalized recommendations to parents/students.
Case study simulations for enhanced learning.
AI-driven question paper pattern generation.
In-App Communication: Secure messaging system between students/parents and tutors.
Integrated Payment Gateway: Facilitate seamless in-app payments for tutoring sessions.
Rating & Review System: Comprehensive feedback mechanism for students/parents to rate tutors.
Broader Subject/Board Coverage: Expansion to other academic boards or competitive exam preparation.
Enhanced Reporting: Detailed progress reports for students and insights for parents.
