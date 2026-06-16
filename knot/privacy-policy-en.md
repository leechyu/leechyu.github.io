# Privacy Policy


## 1. Overview

Knot ("the App") values your privacy. This Privacy Policy explains how we collect, use, disclose, and protect your personal information. Please read this policy carefully to understand our practices regarding your data and your rights.

The App serves users of all ages globally. We comply with applicable privacy laws, including but not limited to the U.S. California Consumer Privacy Act (CCPA/CPRA), the Children's Online Privacy Protection Act (COPPA), the EU General Data Protection Regulation (GDPR), and other applicable regulations.

## 2. Information We Collect

### 2.1 Information You Provide

| Data Category | Details | Purpose |
|--------------|---------|---------|
| Account Information | Email address, hashed password (bcrypt) | Identity verification and login authentication |
| Third-Party Login | Identity token from Apple ID or Google account (used solely for authentication; third-party passwords are never stored) | Apple Sign-In / Google Sign-In |
| Profile | Display name (user-configurable) | Account personalization |
| Note Content | Note body text, tags, attachments (images, audio) | Core note-taking service |
| Voice Data | Audio recordings and speech-to-text transcripts (processing occurs on-device) | Voice note feature |
| Reminder Settings | Reminder times set for notes | Local notification scheduling |

### 2.2 Information Collected Automatically

| Data Category | Details | Purpose |
|--------------|---------|---------|
| Device Information | Device name, platform type (Android/iOS) | Multi-device management and security audit |
| Association Vectors | 384-dimensional embeddings computed from note content | Automatic note link discovery (fully automated; no human review) |
| Crash Logs | Error stack traces collected via Sentry SDK (note content is never included) | Improving app stability |
| Version History | Auto-saved historical versions of notes during editing | Version rollback functionality |

### 2.3 Information We Do NOT Collect

- **Precise Geolocation**: We do not collect GPS location data.
- **Contacts**: We do not access your device contacts.
- **Browsing History**: We do not track your activity on other apps or websites.
- **Biometric Data**: We do not collect fingerprints, facial scans, or other biometric identifiers.

## 3. Data Storage & Security

- All data is stored on our self-hosted servers (PostgreSQL + pgvector database with cloud object storage).
- For users under the China edition, servers are deployed in mainland China; for all other users, servers are deployed in the United States, ensuring low-latency access.
- **Transit Security**: All API communication is encrypted via HTTPS (TLS 1.2+).
- **Storage Security**: Passwords are stored using bcrypt salted hashing; attachments use private storage buckets with signed URL access.
- **Access Control**: All API requests require a JWT token for authentication, with automatic token refresh support.
- **Version History**: Notes are auto-saved with historical versions, viewable and restorable in the versions drawer.

## 4. How We Use Your Data

- **For Your Personal Use Only**: Your note data and association vectors serve solely to provide you with note management, automatic link discovery, fuzzy full-text search, and knowledge graph visualization.
- **Automatic Association**: The system uses an embedding model to convert note content into vectors for automatic discovery of related notes — this process is fully automated with no human review.
- **Local Reminders**: Reminder notifications are scheduled locally on your device; reminder data is not sent to any third-party push notification service.
- **No Advertising**: We do not use your data for advertising or user profiling.
- **No Automated Decision-Making**: We do not make automated decisions that produce legal or similarly significant effects concerning you.

## 5. Data Sharing & Disclosure

### 5.1 Sharing with Third Parties

We **do not sell** your personal information (as "sale" is defined under the CCPA). Except as described below, we do not share your personal data with any third party:

| Disclosure Scenario | Description |
|-------------------|-------------|
| Legal Obligations | Disclose necessary information to law enforcement or regulatory authorities as required by law |
| Service Providers | Disclose necessary data to contractually bound service providers (e.g., cloud storage) to operate the service |
| With Your Consent | Disclose to specific third parties with your explicit consent |

### 5.2 Third-Party SDKs & Services

The App uses the following third-party SDKs, each of which has its own privacy policy:

| SDK | Purpose | Data Collected | Privacy Policy |
|-----|---------|---------------|----------------|
| `sign_in_with_apple` | Apple Sign-In | Identity token (provided by Apple) | [Apple Privacy Policy](https://www.apple.com/legal/privacy/) |
| `google_sign_in` | Google Sign-In | Identity token (provided by Google) | [Google Privacy Policy](https://policies.google.com/privacy) |
| `speech_to_text` | Speech-to-text | Audio recording (processed entirely on-device; not uploaded) | Uses device native API |
| `sentry_flutter` | Crash reporting | Error stack traces, device model, OS version (does NOT include note content or PII) | [Sentry Privacy Policy](https://sentry.io/privacy/) |
| `flutter_local_notifications` | Local notifications | Reminder time (stored locally on device only) | No network communication |

## 6. Data Retention Periods

| Data Type | Retention Period | Notes |
|----------|-----------------|-------|
| Active Account Data | Duration of account activity | Data retained as long as your account remains active |
| Deleted Notes | 30 days (Trash) | Notes enter Trash upon deletion; permanently deleted after 30 days |
| Note Version History | Coextensive with note retention | Automatically deleted when the note is deleted |
| Account Deletion | 30-day cooling-off period, then permanent deletion | Recoverable upon request during cooling-off; irreversible thereafter |
| Export Files | Download link valid for 24 hours | Re-initiate export after link expiration |
| Crash Logs (Sentry) | 90 days | Sentry's default retention policy |

## 7. Your Privacy Rights

Depending on your jurisdiction and applicable law (including CCPA/CPRA), you may have the following rights:

| Right | Description | How to Exercise |
|-------|-------------|-----------------|
| Right to Know | You have the right to know what personal information we collect and how we use it | Review this Privacy Policy |
| Right to Access | You have the right to request a copy of the personal information we hold about you | Use the in-app export feature (Settings → Export Data); the exported zip contains all notes (Markdown) + attachments |
| Right to Delete | You have the right to request deletion of your personal information | Settings → Delete Account; or delete individual notes (cleared from Trash after 30 days) |
| Right to Correct | You have the right to correct inaccurate personal information | Edit display name and password in Settings |
| Right to Data Portability | You have the right to obtain your data in a portable format and transfer it to another service | Exported zip files can be re-imported on another Knot server |
| Right to Opt Out of Sale | You have the right to opt out of the "sale" of your personal information | We do not sell personal information, so no opt-out is necessary |
| Right to Non-Discrimination | Exercising your rights will not result in denial of service or different pricing | — |

### 7.1 California Resident-Specific Rights

If you are a California resident, under the CCPA/CPRA you additionally have the right to:
- Request disclosure of the categories and specific pieces of personal information we have collected (response within 45 days)
- Request disclosure of the categories of sources from which personal information is collected, the business or commercial purpose for collecting or selling, and the categories of third parties with whom we share it
- Limit the use and disclosure of sensitive personal information (we do not currently collect "sensitive personal information" as defined by the CCPA)

To exercise these rights, please contact us using the information in Section 12. We will respond to verifiable requests within 45 days.

### 7.2 Authorized Agents

You may designate an authorized agent to submit a CCPA request on your behalf. The agent must provide proof of your written authorization.

## 8. Children's Privacy (COPPA)

The App is open to users of all ages. Children under the age of 13 may use the App with the guidance and consent of a parent or legal guardian. We comply with the Children's Online Privacy Protection Act (COPPA). If you believe we may have information from a child under 13 without appropriate parental consent, please contact us.

## 9. Do Not Track

Our service does not respond to "Do Not Track" (DNT) signals from browsers, as we do not track user behavior across websites or applications.

## 10. Data Breach Notification

In the event of a data breach involving your personal information, we will notify you and relevant regulatory authorities within the timeframe required by applicable law.

## 11. Policy Updates

This Privacy Policy may be updated from time to time. For significant changes, we will notify you through:
- An in-app notification
- Where changes involve new data collection purposes, we will seek your consent again

Your continued use of the App after such changes constitutes acceptance of the updated Privacy Policy.

## 12. Contact Us

For privacy-related inquiries or to exercise your rights, please contact us at:

- 📧 Email: leechyu89@gmail.com
- ⏱ Response Time: We will respond within 7 business days


