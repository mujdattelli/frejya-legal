---
title: Privacy Policy — Frejya
layout: default
---

# Frejya — Privacy Policy

**Effective Date:** May 14, 2026
**Last Updated:** June 11, 2026

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
- **Profile photo** (mandatory; processed via AI as detailed below). Photos are stored **privately** in Supabase Storage; they are not handed directly to your match but are revealed gradually through the in-chat **"scratch"** mechanic as both sides exchange words.
- **Voice introduction recording** (optional). When you record one, your real frequency is concealed via **voice-pitch masking** (Deep / Bass / Dynamic / Warm).
- **Year of birth** (required for 18+ age verification; **cannot be changed after registration**)
- **Gender** (used by the matching algorithm; **cannot be changed after registration**)
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
- **Your messages (End-to-End Encrypted — E2EE):** Messages exchanged with other users are protected by **genuine end-to-end encryption (NaCl / Curve25519, `nacl.box`)**. Each user-device pair has its own key pair; the **private key lives only on your device** (`expo-secure-store`) and is never sent to the server. Only the **public key** is stored on the server. Messages can be decrypted only on the sender's and recipient's devices; **our servers and database administrators (including us) cannot read message content in plain text.**
  - **Key backup:** So that you can access your old messages on a new device, your private key is encrypted (wrapped) with a key derived from **your login password** and backed up on the server. Because the server does not know your password in plain text, it cannot decrypt this backup; it is unwrapped only when you enter the correct password. (For password-less accounts that sign in with Google/Apple, a dedicated **recovery key** is used instead.)
  - **Password reset / change warning:** If you **reset** your password (forgot password) or change it, the key wrapped with the old password may become invalid, so **your old messages may become unrecoverable / unreadable.** This is an intentional design choice to protect your privacy.
- **Message metadata:** Sender ID, receiver ID, timestamp, read status, and word count (for the scratch mechanic) are stored for service functionality.
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
- **What is checked:** In a single call the AI assesses whether the photo is a **real human** (not animation/illustration/AI-generated/object/landscape), **face visibility**, absence of **nudity/explicit content (NSFW)**, that it is not a **minor / child**, and **consistency with your declared gender**. There is no on-device pre-scan; all checks run server-side.
- **Attractiveness score:** Approved photos receive an objective 1-10 quality score from the AI (lighting, sharpness, expression, framing) used for match ranking. The AI is instructed **not to discriminate based on skin tone, age, or race**. This score is not shown to other users.
- **Consent:** You are asked to consent to AI processing during profile creation. Without consent, you cannot use Frejya (since profile photo verification is mandatory).
- **Outcome:** Your photo is approved, rejected, or queued for manual review. Rejected photos are deleted from Storage. If a photo is **rejected 5 times in a row**, the account is temporarily (1 day) restricted from uploading a new photo; this counter resets when a photo is approved or automatically after 30 days.

**Important:** Biography (bio), hobbies, and other text fields are screened separately for content appropriateness but are **NOT** included in attractiveness/match scoring.

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
| **Cloudflare Turnstile** | Bot / automated-abuse protection (captcha) | Global (Cloudflare network) | IP address + browser/device signals (not linked to your identity) |

Data Processing Agreements (DPAs) are in effect or being established with each service provider.

> **🛡️ Bot protection (Cloudflare Turnstile):** Cloudflare Turnstile is used during sign-up, login, password reset, and account deletion to prevent automated (bot) access. It processes your IP address and browser/device signals; this data is not linked to your identity and is not used for advertising. Turnstile runs in "invisible" mode, so a verification step usually does not appear on screen. For Cloudflare's data processing in this context, see the **Cloudflare Turnstile Privacy Addendum**: https://www.cloudflare.com/turnstile-privacy-policy/

---

## 6. Data Retention Periods

| Data Type | Retention Period |
|---|---|
| Active account data | As long as the account is active |
| Text & image messages (E2EE) | Kept while the chat is open. On chat end, removed from the user view and retained **encrypted for 15 days** (for potential forensic/legal evidence), then permanently deleted |
| **Voice messages** | **Automatically deleted 15 days after sending** (even if the chat is still open) |
| Blocking after a chat ends | **No automatic block**; the user may permanently block the other party via "End & block" if they choose |
| Anonymous hold (grace) after account deletion | **15 days** (for legal notice / fraud claim review) — then permanently deleted including `auth.users` |
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
6. **To request deletion of your data** (initiated via the "Delete My Account" button inside the app; data is permanently deleted at the end of the 15-day grace/undo period — see §6),
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

- **End-to-end encryption (E2EE — NaCl / Curve25519):** Messages are protected by genuine end-to-end encryption. Each user-device pair has a separate key pair; the **private key exists only on your device** (`expo-secure-store`) and is never sent to the server. The server stores only the public key. As a result, **no one — including database administrators — can read message content in plain text.** The server backup of your private key is wrapped only with a key derived from your password (or your recovery key on OAuth accounts); since the server does not know your password, it cannot decrypt this backup (see §2.4).
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

Since Frejya is a mobile app, it **does not use cookies**. Our website (https://frejya.app) may use only functional cookies (since you are not logged in, no user tracking takes place).

**No advertising SDKs. No analytics SDKs. No Facebook / Google Analytics.**

---

## 12. Changes to This Policy

We may update this Policy from time to time. For significant changes, we will notify you via in-app notification and/or email. The current version is always published at:

**https://mujdattelli.github.io/frejya-legal/legal/privacy.en.html**

---

## 13. Contact

For questions, complaints, or KVKK / GDPR requests:

**Müjdat TELLİ**
Email: **iletisim@frejya.app**

For formal KVKK applications, **written submission** or **registered electronic mail (KEP)** is preferred.

---

*This document has been prepared as a draft for legal review. It is recommended that a qualified attorney review the text before it enters into force.*
