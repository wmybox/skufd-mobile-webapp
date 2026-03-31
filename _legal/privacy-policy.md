---
layout: page
title: Privacy Policy
permalink: /legal/privacy-policy/
---

*Last updated: March 30, 2026*

# SKUFD Privacy Policy

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Who We Are](#2-who-we-are)
3. [Information We Collect](#3-information-we-collect)
4. [How We Use Your Information](#4-how-we-use-your-information)
5. [How We Store Your Information](#5-how-we-store-your-information)
6. [How We Share Your Information](#6-how-we-share-your-information)
7. [Third-Party Services](#7-third-party-services)
8. [Device Permissions](#8-device-permissions)
9. [Data Retention](#9-data-retention)
10. [Your Rights and Choices](#10-your-rights-and-choices)
11. [Children's Privacy](#11-childrens-privacy)
12. [International Data Transfers](#12-international-data-transfers)
13. [Security](#13-security)
14. [California Residents (CCPA/CPRA)](#14-california-residents-ccpacpra)
15. [European Economic Area Residents (GDPR)](#15-european-economic-area-residents-gdpr)
16. [Google Play Data Safety Alignment](#16-google-play-data-safety-alignment)
17. [Changes to This Policy](#17-changes-to-this-policy)
18. [Contact Us](#18-contact-us)

---

## 1. Introduction

This Privacy Policy explains how SKUFD ("we," "us," or "our") collects, uses, stores, shares, and protects your personal information when you use the SKUFD mobile application (the "App"). SKUFD is a multi-community outdoor activity discovery platform where users from communities such as skateboarding, birding, disc golf, photography, geocaching, street art, and others discover, share, and organize locations ("spots") on a shared map.

We are committed to protecting your privacy. Please read this policy carefully. By using the App, you agree to the collection and use of information as described here. If you do not agree, please do not use the App.

---

## 2. Who We Are

SKUFD is developed and operated by:

**[Your Company Name / Your Legal Name]**
[Business Address]
[Contact Email]
[Website URL, if applicable]

---

## 3. Information We Collect

### 3.1 Information You Provide Directly

- **Account Information.** When you create an account, we collect your email address (used for authentication) and a public handle (a display name you choose, such as @boobookitty). Authentication is provided through Supabase, supporting email/password and Google OAuth sign-in.

- **Profile Information.** You select community interests during onboarding (e.g., "skateboarding," "birding") to personalize your map experience. These selections are stored with your account.

- **Spot Content.** When you create or edit a spot, we collect the data you provide: spot name (label), description, geographic coordinates (latitude and longitude of the spot's location), and tags you assign to the spot.

- **Photos and Media.** When you upload photos to a spot, the image files are stored locally on your device and synced to our cloud storage. We store the photos themselves plus metadata such as file size and display order. We accept JPEG, PNG, and WebP image formats, with a maximum file size of 10 MiB per image.

- **Comments.** Text content you write as comments on spots, including any @mentions of other users.

- **Endorsements and Bookmarks.** When you endorse or bookmark a spot, we record which spot you endorsed or bookmarked and when.

- **Spot Lists.** Names and descriptions of lists you create to organize spots.

### 3.2 Information Collected Automatically

- **Location Data.** With your permission, we collect your device's precise GPS location using Google Play Services FusedLocationProvider. This is used to show your position on the map and to enable you to create spots at your current location. Location data is collected only while the App is in use and you have granted location permission. We do not collect location data in the background.

- **Device Identifier.** We generate and store a device identifier used for sync operations. This identifier ensures data synchronization between your device and our servers is consistent and conflict-free. It is used in idempotency keys for sync operations and is not used for advertising or cross-app tracking.

- **Analytics Events.** We collect anonymized usage analytics through PostHog to understand how the App is used and to improve the product. These events are non-personally-identifiable. We explicitly do NOT log: spot labels, GPS coordinates, comment text, tag names, usernames, email addresses, or search queries in analytics. Analytics events are limited to interaction patterns (e.g., "screen viewed," "spot created") without any content or location details.

- **Crash Reports and Error Data.** We use Sentry to collect crash reports and error logs. These may include device model, operating system version, app version, stack traces, and breadcrumbs (a sequence of recent app actions leading to the error). Crash reports help us identify and fix bugs. Sentry data may incidentally include device state information but does not intentionally capture personal content.

- **Network State.** We detect whether your device has an active network connection to manage offline/online sync behavior. This information is not stored or transmitted.

### 3.3 Information We Do NOT Collect

- We do not collect contacts, call logs, SMS messages, or browsing history.
- We do not collect biometric data.
- We do not collect financial or payment information (the App does not currently have in-app purchases).
- We do not use advertising SDKs or collect advertising identifiers.
- We do not collect location data in the background.

---

## 4. How We Use Your Information

We use the information we collect for the following purposes:

| Purpose | Data Used | Legal Basis (GDPR) |
|---------|-----------|---------------------|
| Provide and operate the App | Account info, spot content, media, comments, endorsements, bookmarks, lists | Performance of contract |
| Display your spots and content to other users | Spot data, media, comments, handle | Performance of contract |
| Personalize your map view based on community interests | Interest selections | Performance of contract / Consent |
| Enable offline use and cloud sync | All user-created content, device ID | Performance of contract |
| Resolve sync conflicts between devices | Device ID, entity versions, timestamps | Legitimate interest |
| Show your position on the map | Device GPS location | Consent |
| Display and load images | Media files | Performance of contract |
| Improve the App and understand usage patterns | Anonymized analytics events | Legitimate interest |
| Diagnose and fix bugs and crashes | Crash reports, error logs | Legitimate interest |
| Communicate with you about your account | Email address | Performance of contract |
| Enforce our Terms of Service | Account info, usage data | Legitimate interest |
| Comply with legal obligations | As required | Legal obligation |

We do NOT use your information for:

- Targeted advertising
- Selling to third parties
- Building advertising profiles
- Automated decision-making or profiling that produces legal effects

---

## 5. How We Store Your Information

### 5.1 Local Storage (On-Device)

SKUFD is built with an offline-first architecture. Your data is stored locally on your device in a SQLite database (via Android Room) and in local file storage for media. This local copy is the primary source of truth for your experience -- the App works even without an internet connection.

Local storage includes: your account data, spots, comments, endorsements, bookmarks, lists, media files, tags, sync queue entries, and preferences.

### 5.2 Cloud Storage

When your device has network connectivity, data syncs to our cloud backend hosted on Supabase. Supabase provides:

- **Database hosting** (PostgreSQL) for structured data (spots, comments, tags, user data, etc.)
- **Object storage** for media files (photos)
- **Authentication services** for account management

Supabase infrastructure is hosted on Amazon Web Services (AWS). For information on Supabase's own security and data handling practices, see [Supabase's Privacy Policy](https://supabase.com/privacy) and [Security documentation](https://supabase.com/security).

### 5.3 Data at Rest

Data stored in Supabase PostgreSQL is encrypted at rest using AES-256 encryption provided by the underlying AWS infrastructure. Media files in Supabase Storage are similarly encrypted at rest. Local data on your device is protected by your device's own encryption and lock screen security.

---

## 6. How We Share Your Information

### 6.1 With Other SKUFD Users

SKUFD is a community platform. The following information is visible to other authenticated SKUFD users:

- Your public handle
- Spots you create (including label, description, location, tags, and photos)
- Comments you post on spots
- Your endorsements of spots

Your email address is NOT visible to other users.

### 6.2 Shareable Spot Links

When a spot is shared via a link outside the App, a public web preview page displays limited information: the spot's image, title, community tag, and a mini map. This preview is publicly accessible to anyone with the link. Full spot details are only accessible within the App after authentication.

### 6.3 With Service Providers

We share data with the following third-party service providers who process data on our behalf:

| Provider | Purpose | Data Shared |
|----------|---------|-------------|
| **Supabase** (backed by AWS) | Backend infrastructure: database, authentication, file storage, realtime sync | All user-created content, account data, media files |
| **PostHog** | Product analytics | Anonymized usage events (no PII, no content, no location coordinates) |
| **Sentry** | Crash reporting and error tracking | Device info, OS version, app version, stack traces, error breadcrumbs |
| **Google** (Play Services) | Location services, Google OAuth sign-in | Location data (processed on-device), OAuth tokens (during sign-in) |

### 6.4 We Do NOT Sell Your Data

We do not sell, rent, or trade your personal information to third parties. We do not share your data with data brokers. We do not provide data to advertisers.

### 6.5 Legal Requirements

We may disclose your information if required to do so by law, regulation, legal process, or governmental request, or when we believe in good faith that disclosure is necessary to protect our rights, your safety, the safety of others, or to investigate fraud or respond to a government request.

### 6.6 Business Transfers

If SKUFD is involved in a merger, acquisition, or sale of assets, your information may be transferred as part of that transaction. We will notify you of any such change via a prominent notice in the App or by email.

---

## 7. Third-Party Services

The App integrates the following third-party SDKs and services. Each has its own privacy policy governing its data practices:

### 7.1 Supabase (Authentication, Database, Storage)

- **Purpose:** User authentication (email/password and Google OAuth), cloud database, media file storage, realtime data sync
- **Data processed:** Account credentials, all user-created content, media files
- **Privacy policy:** [https://supabase.com/privacy](https://supabase.com/privacy)

### 7.2 PostHog (Analytics)

- **Purpose:** Product usage analytics to understand feature adoption and app performance
- **Data processed:** Anonymized event data only. No PII is sent to PostHog. We do not send spot labels, GPS coordinates, comment text, tag names, usernames, email addresses, or search queries.
- **Privacy policy:** [https://posthog.com/privacy](https://posthog.com/privacy)

### 7.3 Sentry (Error Tracking)

- **Purpose:** Crash reporting and error monitoring to identify and fix bugs
- **Data processed:** Device model, OS version, app version, stack traces, error breadcrumbs
- **Privacy policy:** [https://sentry.io/privacy/](https://sentry.io/privacy/)

### 7.4 Google Play Services (Location)

- **Purpose:** Precise location via FusedLocationProvider for map positioning and spot creation
- **Data processed:** GPS coordinates (processed primarily on-device; Google Play Services may transmit location data per its own policies)
- **Privacy policy:** [https://policies.google.com/privacy](https://policies.google.com/privacy)

### 7.5 Google Sign-In (OAuth)

- **Purpose:** Optional sign-in method using your Google account
- **Data processed:** OAuth tokens, email address (from your Google account, used to create or link your SKUFD account)
- **Privacy policy:** [https://policies.google.com/privacy](https://policies.google.com/privacy)

### 7.6 Google Fonts

- **Purpose:** Typography rendering within the App
- **Data processed:** Font files are fetched from Google servers. Google may collect standard request metadata (IP address, user agent). See [Google Fonts privacy FAQ](https://developers.google.com/fonts/faq/privacy).
- **Privacy policy:** [https://policies.google.com/privacy](https://policies.google.com/privacy)

---

## 8. Device Permissions

The App requests the following Android permissions:

| Permission | Why We Need It | When Requested |
|------------|---------------|----------------|
| **Internet** (`INTERNET`) | Sync data with cloud backend, load images, authenticate | Always required |
| **Network State** (`ACCESS_NETWORK_STATE`) | Detect connectivity to manage offline/online sync | Always required |
| **Fine Location** (`ACCESS_FINE_LOCATION`) | Show your position on the map; enable spot creation at your current location | Requested at runtime when you use the map. You can deny this and still use the App with reduced functionality. |
| **Coarse Location** (`ACCESS_COARSE_LOCATION`) | Approximate location as fallback when fine location is unavailable | Requested alongside fine location |
| **Camera** (`CAMERA`) | Capture photos to attach to spots | Requested at runtime when you use the camera feature. You can deny this and still add spots without photos. |

All sensitive permissions (location, camera) are requested at runtime with clear explanations. You can revoke any permission at any time through your device's Settings. Revoking permissions may limit certain features but will not prevent you from using the App entirely.

---

## 9. Data Retention

### 9.1 Active Account Data

We retain your data for as long as your account is active and as needed to provide you with the App's services.

### 9.2 Soft Deletes

When you delete content (spots, comments, list entries), the content is "soft deleted" -- marked with a deletion timestamp rather than immediately removed. This enables sync operations to propagate the deletion to all your devices and to the server. Soft-deleted content is not visible in the App.

### 9.3 Domain Events (Audit Log)

Changes to your content are recorded as domain events (an internal audit log). Local domain event records are retained for 30 days on-device or until successfully synced, whichever comes first. Server-side domain events are retained indefinitely and may be archived to cold storage.

### 9.4 Analytics and Crash Data

- **PostHog analytics data:** Retained according to PostHog's data retention policies. We do not configure indefinite retention of analytics events.
- **Sentry crash data:** Retained according to Sentry's default retention period (typically 90 days for event data).

### 9.5 Account Deletion

You may request deletion of your account and all associated data. See Section 10 for details on how to exercise this right. Upon account deletion:

- Your account record will be permanently removed
- Your spots, comments, endorsements, bookmarks, and lists will be permanently deleted
- Your media files will be permanently deleted from cloud storage
- Local data on your device can be cleared by uninstalling the App
- Some data may persist in encrypted backups for a limited period consistent with our infrastructure provider's backup schedule
- Anonymized analytics data that has already been collected cannot be attributed back to you and may persist

---

## 10. Your Rights and Choices

Regardless of where you live, we provide the following rights to all SKUFD users:

- **Access.** You can request a copy of the personal data we hold about you.
- **Correction.** You can update your profile information (handle, interests) directly in the App. For other corrections, contact us.
- **Deletion.** You can request deletion of your account and associated data by contacting us at [Contact Email]. We will process deletion requests within 30 days.
- **Data Portability.** You can request your data in a structured, machine-readable format.
- **Withdraw Consent.** Where we rely on consent (e.g., location permission), you can withdraw it at any time through your device settings or by contacting us.
- **Opt Out of Analytics.** [If you provide an in-app toggle, describe it here. Otherwise: "Contact us at [Contact Email] to opt out of analytics data collection."]

To exercise any of these rights, contact us at [Contact Email]. We will verify your identity before processing requests and will respond within 30 days.

---

## 11. Children's Privacy

SKUFD is not directed at children under the age of 13 (or under the age of 16 in the European Economic Area). We do not knowingly collect personal information from children under these ages. If we learn that we have collected personal information from a child under the applicable age, we will take steps to delete that information promptly.

If you are a parent or guardian and believe your child has provided us with personal information, please contact us at [Contact Email].

---

## 12. International Data Transfers

SKUFD's cloud infrastructure is hosted on Supabase, which uses Amazon Web Services (AWS). Your data may be stored and processed in the United States or other countries where AWS operates data centers. If you are located outside the United States, your data will be transferred internationally.

Where required by law (e.g., for transfers from the EEA), we rely on:

- Standard Contractual Clauses (SCCs) as adopted by the European Commission
- Our service providers' compliance frameworks (Supabase, AWS, PostHog, and Sentry each maintain their own data transfer mechanisms)

---

## 13. Security

We implement reasonable technical and organizational measures to protect your personal information:

- **Encryption in transit:** All communication between the App and our servers uses HTTPS/TLS.
- **Encryption at rest:** Cloud database and storage are encrypted using AES-256 via AWS infrastructure.
- **Authentication security:** Passwords are hashed by Supabase Auth (bcrypt). We never store plaintext passwords. OAuth tokens are handled securely via Google's authentication flow.
- **Row-Level Security (RLS):** Supabase PostgreSQL policies ensure users can only access data they are authorized to view or modify.
- **No service role keys in the App:** Server-side secrets are never embedded in the mobile application.
- **Local device security:** Local data is protected by your device's encryption and lock screen.
- **Backup security:** `android:allowBackup="false"` is set in the App manifest, preventing Android backup services from copying app data to Google Drive.

No method of transmission or storage is 100% secure. While we strive to protect your data, we cannot guarantee absolute security.

---

## 14. California Residents (CCPA/CPRA)

If you are a California resident, you have additional rights under the California Consumer Privacy Act (CCPA) as amended by the California Privacy Rights Act (CPRA):

- **Right to Know.** You may request the categories and specific pieces of personal information we have collected about you, the sources, the purposes, and the categories of third parties with whom we share it.
- **Right to Delete.** You may request deletion of your personal information, subject to certain exceptions.
- **Right to Correct.** You may request correction of inaccurate personal information.
- **Right to Opt Out of Sale/Sharing.** We do not sell your personal information. We do not share your personal information for cross-context behavioral advertising.
- **Right to Non-Discrimination.** We will not discriminate against you for exercising your CCPA/CPRA rights.

**Categories of personal information collected (CCPA categories):**

| CCPA Category | Examples from SKUFD | Sold? | Shared for Advertising? |
|---------------|---------------------|-------|------------------------|
| Identifiers | Email address, public handle, device ID | No | No |
| Geolocation data | GPS coordinates (for spot creation and map display) | No | No |
| Internet/electronic network activity | Anonymized analytics events, crash reports | No | No |
| User-generated content | Spots, comments, photos, tags, lists | No | No |

To exercise your rights, contact us at [Contact Email]. We will verify your identity and respond within 45 days.

---

## 15. European Economic Area Residents (GDPR)

If you are located in the European Economic Area (EEA), United Kingdom, or Switzerland, the General Data Protection Regulation (GDPR) applies to our processing of your personal data.

### 15.1 Legal Bases for Processing

Our legal bases for processing are described in the table in Section 4. In summary:

- **Performance of contract:** Processing necessary to provide the App's services (account management, content creation, sync)
- **Consent:** Location access, camera access, optional Google sign-in
- **Legitimate interest:** Analytics (to improve the product), crash reporting (to fix bugs), sync conflict resolution

### 15.2 Your GDPR Rights

In addition to the rights listed in Section 10, you have:

- **Right to Restrict Processing.** You can request that we limit how we process your data in certain circumstances.
- **Right to Object.** You can object to processing based on legitimate interests. We will cease processing unless we have compelling legitimate grounds.
- **Right to Lodge a Complaint.** You have the right to lodge a complaint with your local supervisory authority (Data Protection Authority).

### 15.3 Data Protection Officer

[If you have appointed a DPO, provide their contact information here. If not required, state: "We have not appointed a Data Protection Officer as we do not meet the threshold requirements under GDPR Article 37. For privacy inquiries, contact us at [Contact Email]."]

### 15.4 Data Controller

The data controller for the purposes of GDPR is [Your Company Name / Your Legal Name], contactable at [Contact Email].

---

## 16. Google Play Data Safety Alignment

This section summarizes our data practices in the format aligned with Google Play's Data Safety section requirements.

### Data Collected

| Data Type | Collected | Shared | Purpose | Optional |
|-----------|-----------|--------|---------|----------|
| Email address | Yes | No | Account management, authentication | No (required for account) |
| User name (handle) | Yes | Yes (visible to other users) | App functionality (public identity) | No |
| Location (precise) | Yes | No | App functionality (map, spot creation) | Yes (can deny permission) |
| Photos | Yes | Yes (visible to other users on spots) | App functionality | Yes (spots can be created without photos) |
| User-generated content | Yes | Yes (visible to other users) | App functionality | No (core feature) |
| App interactions | Yes | No (sent to PostHog, anonymized) | Analytics | No (but no PII collected) |
| Crash logs | Yes | No (sent to Sentry) | App diagnostics | No |
| Device ID | Yes | No | Sync functionality | No |

### Data Handling

- **Encrypted in transit:** Yes (HTTPS/TLS)
- **Encrypted at rest:** Yes (AES-256 via AWS)
- **Deletion mechanism:** Users can request account and data deletion
- **Data not sold to third parties**

---

## 17. Changes to This Policy

We may update this Privacy Policy from time to time. When we make material changes, we will:

- Update the "Last Updated" date at the top of this policy
- Notify you through the App (e.g., an in-app notice) or by email for significant changes
- Provide you with the opportunity to review the changes before they take effect

Your continued use of the App after changes are posted constitutes your acceptance of the revised policy.

---

## 18. Contact Us

If you have questions, concerns, or requests related to this Privacy Policy or your personal data, contact us at:

**[Your Company Name / Your Legal Name]**
Email: [Contact Email]
Address: [Business Address]

We aim to respond to all inquiries within 30 days.

---

**IMPORTANT DISCLAIMER:** This Privacy Policy is a draft prepared for review purposes. It should be reviewed and approved by a qualified attorney licensed in your jurisdiction before publication. Privacy law requirements vary by jurisdiction and change frequently. This document does not constitute legal advice.

