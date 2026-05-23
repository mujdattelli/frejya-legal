---
title: Privacy Policy — Frejya
layout: default
---

# Frejya — Privacy Policy

**Effective Date:** May 14, 2026
**Last Updated:** May 14, 2026

This Privacy Policy describes how **Müjdat TELLİ** (hereinafter "we", "Frejya", or "Service Provider") collects, uses, and protects personal data of users (hereinafter "you" or "User") of the **Frejya** mobile application (hereinafter "Application").

Contact: **iletisim@frejya.app**

This Policy is prepared in compliance with **Turkey's Personal Data Protection Law No. 6698 (KVKK)** and, where applicable, the **European Union General Data Protection Regulation (GDPR)**.

---

## 1. Data Controller

The data controller of the Frejya application is **Müjdat TELLİ** as a natural person. You may submit your KVKK / GDPR-related requests to the email address above.

---

## 2. Personal Data We Collect

When you use Frejya, we collect the following categories of data:

### 2.1. Identity and Contact Information
- **Email address** (for account creation and recovery)
- **Phone number** (for SMS verification and account security, optional)
- **Username / Display name** (chosen by you during profile creation)
- **Password** (never stored in plain text; hashed with bcrypt and salted)

### 2.2. Profile Information (Provided by You)
- **Profile photo** (mandatory; processed via AI as detailed below)
- **Voice introduction recording** (optional)
- **Year of birth** (required for 18+ age verification)
- **Gender** (used by the matching algorithm)
- **Height, weight, marital status** (optional profile data)
- **Education, profession** (optional)
- **Lifestyle preferences:** drinking, smoking, pets, dance, religion, tattoos, LGBT status, mobile gaming, travel (all optional; "Skip" available for each)
- **Hobbies, three-word description, biography** (free text)

### 2.3. Location Data
- During registration we request **your GPS coordinates (latitude, longitude)**. These coordinates are used **only for reverse geocoding** to derive **city, district, and country** information.
- **Raw GPS coordinates are NOT stored in your profile and are NOT visible to any other user.**
- The database stores only: **city, district, country** as text fields.
- Exception: For fraud detection and "Impossible Travel" anomaly analysis, **last login coordinates** and **timestamp** are stored briefly in a separate field; this data is read by the system only for security violation analysis and is never shown to any user.

### 2.4. Communication and Content Data
- **Your messages:** Messages exchanged with other users are encrypted **with AES-256 (at-rest storage)**. Our servers **cannot decrypt** message content. Message **metadata** (sender ID, receiver ID, timestamp, read status) is stored for service functionality.
- **Posts:** Content you share to the Frejya Aura social feed (symbols / SVG references). Visible to other users.
- **Interactions:** Likes, comments, matches, doorbell-ring records (who, whom, when).
- **Blocking / report lists:** For your personal safety.

### 2.5. Technical Data
- **Device identifier (Device ID):** To prevent Sybil (fake account) attacks. The Device ID is an anonymous identifier provided by Apple/Google and is **not used for advertising tracking**.
- **Push notification token:** Routed via Expo Push Service to Apple APNs / Google FCM for delivering notifications.
- **App version, OS version:** For debugging and compatibility checks.

### 2.6. Automatically Collected Data
- **Crash / error reports:** When the app crashes, stack traces and device info are collected anonymously (via Sentry, on EU / Germany servers).
- **Usage statistics:** Counters such as daily interaction counts (likes, comments, matches) are kept for rate limiting.

---

## 3. AI-Based Content Review

For user safety, Frejya analyzes **your profile photo** using automated AI services. This review:

- **AI services used:** Profile photos are sent **anonymously** (without your user identity) to Google Gemini AI. The exact model version is selected by Frejya administration based on current needs (e.g., Gemini 1.5 Flash or Gemini 3). Groq is configured as a fallback service.
- **Location:** This service runs on Google's servers outside Turkey. After processing, photos are not retained per Google's Gemini API privacy policy (data sent via the Gemini API is not used for model training and is processed transiently).
- **Face detection:** Face detection is performed by the AI service in a single combined call (no on-device pre-scan). The AI checks both face presence and content appropriateness together.
- **Consent:** You are asked to consent to AI processing during profile creation. Without consent, you cannot use Frejya (since profile photo verification is mandatory).
- **Outcome:** Your photo is approved, rejected, or queued for manual review. Rejected photos are deleted from Storage.

**Important:** Biography (bio), hobbies, and other text fields are **NOT** analyzed by AI.

---

## 4. Purposes of Personal Data Processing

We process your data **only** for the following purposes:

1. **Service provision:** Matching algorithm, messaging, social feed.
2. **Account security:** Fake account prevention (Device ID), fraud detection (Impossible Travel), suspicious activity logging.
3. **Content moderation:** Profile photo AI review, report / block systems.
4. **Communication:** Notifications, account recovery emails.
5. **Service improvement:** Anonymous crash reports (Sentry).
6. **Legal obligations:** Court orders, fraud reports, etc.

**We NEVER:**
- Sell your data to third parties for advertising or marketing.
- Process your data for political, religious, or commercial profiling.
- Transfer your email list to third parties.

---

## 5. Third-Party Service Providers

We use the following service providers, each subject to their own privacy policies:

| Service | Purpose | Location | Data Type |
|---|---|---|---|
| **Supabase** | Database, auth, storage, realtime | EU (Frankfurt / Ireland) | All profile data, message metadata, photos |
| **Sentry** | Crash & error tracking | EU (Germany) | Anonymous crash reports, user UUID |
| **Google Gemini API** | Profile photo AI review | USA / EU | Photo only (anonymous, no user identity) |
| **Groq API** | Profile photo AI review (fallback) | USA | Photo only (anonymous) |
| **Expo Push Service** | Push notification delivery | USA (Apple APNs / Google FCM transit) | Only push token + message title |
| **Apple App Store / Google Play** | App distribution | Global | Download data (not shared with us; only statistics) |

Data Processing Agreements (DPAs) are in effect or being established with each service provider.

---

## 6. Data Retention Periods

| Data Type | Retention Period |
|---|---|
| Active account data | As long as the account is active |
| Text & image messages (E2EE) | Kept during the chat; deleted when the chat ends |
| **Voice messages** | **Automatically deleted 15 days after sending** (even if the chat is still open) |
| Anonymous record after account deletion | **15 days** (for legal notice / fraud claim review) — then permanently deleted including `auth.users` |
| Crash logs (Sentry) | 90 days |
| Audit logs (legal obligation) | 1 year (anonymous — UUID + action + timestamp) |
| Rejected profile photos | Deleted immediately |

---

## 7. Your Rights (KVKK / GDPR)

Per KVKK Article 11 (and GDPR Articles 15-22), you have the following rights:

1. To learn whether your personal data is being processed,
2. To request information if processing has occurred,
3. To learn the purpose of processing and whether the data is used in accordance with that purpose,
4. To know third parties to whom data is transferred (domestic or abroad),
5. To request correction of incomplete or inaccurate data,
6. **To request deletion of your data** (instantly available via the "Delete My Account" button inside the app),
7. To request that corrections / deletions be notified to third parties,
8. To object to outcomes generated against you through automated systems,
9. To claim damages if you suffer loss due to unlawful processing.

To exercise these rights, send a **written request** to **iletisim@frejya.app**. Your request will be answered **free of charge within 30 days** at the latest.

---

## 8. Children's Privacy

Frejya is for users **18 years of age or older**. **Persons under 18 are prohibited** from creating an account. You are required to declare your age during registration; **false declarations result in immediate account deletion**. If you discover that a person under 18 has created an account on Frejya, please report it to **iletisim@frejya.app** and we will delete the account within 24 hours.

---

## 9. Data Security

To protect your data, we apply the following technical and administrative measures:

- **At-rest encryption (AES-256):** Message content is encrypted with AES-256 on the device before being written to our servers. This ensures messages cannot be read in plain text from database backups or unauthorized access. NOTE: Our current implementation uses a single shared application key; therefore, this mechanism does not technically qualify as "end-to-end encryption" (E2EE). A future migration to full E2EE (e.g., Signal Protocol) is planned.
- **Password security:** Bcrypt hash + salt; plain-text passwords are never stored.
- **Database security:** Supabase Row Level Security (RLS) enforces per-row permission checks.
- **SSL/TLS:** All traffic is HTTPS-encrypted; SSL pinning is active.
- **Access control:** Only authorized system services can access the database; **no personnel, including us, can read user passwords**.
- **Rate limiting:** Protection against brute-force and spam attacks.
- **Anomaly detection:** Suspicious login attempts are detected.

**In case of a data breach:** Pursuant to KVKK Art. 12/5 and GDPR Art. 33, we will notify the Personal Data Protection Authority and affected users **within 72 hours** of discovering unauthorized acquisition of personal data.

---

## 10. International Data Transfer

Some of our service providers (Gemini, Groq, Expo) are located outside Turkey. Therefore:

- Your profile photo may be transferred anonymously to USA / EU for AI review.
- Your push notification token is transmitted via Apple APNs (USA) or Google FCM (USA).

These transfers occur under KVKK Art. 9 with your **explicit consent**, which is requested at registration with full information about the transfer.

---

## 11. Cookies and Tracking

Since Frejya is a mobile app, it **does not use cookies**. Our website (https://mujdattelli.github.io/velvet/) may use only functional cookies (since you are not logged in, no user tracking takes place).

**No advertising SDKs. No analytics SDKs. No Facebook / Google Analytics.**

---

## 12. Changes to This Policy

We may update this Policy from time to time. For significant changes, we will notify you via in-app notification and/or email. The current version is always published at:

**https://mujdattelli.github.io/velvet/legal/privacy.en.html**

---

## 13. Contact

For questions, complaints, or KVKK / GDPR requests:

**Müjdat TELLİ**
Email: **iletisim@frejya.app**

For formal KVKK applications, **written submission** or **registered electronic mail (KEP)** is preferred.

---

*This document has been prepared as a draft for legal review. It is recommended that a qualified attorney review the text before it enters into force.*
