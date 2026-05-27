# Evoke Privacy Policy

**Last updated: May 27, 2026**

Evoke is a relationship maintenance app that helps you stay connected with the people who matter. This policy explains what data Evoke handles, how it's stored, and what rights you have.

**The short version: your relationship data — your contacts, check-ins, notes, and preferences — is private to you. It lives on your device and in your personal iCloud account so it can sync across your iPhones, iPads, and Macs. We have no servers that hold it, can't read it, and never share or sell it. Evoke does collect anonymous usage and diagnostic data to fix bugs and improve the app — never your contacts, names, or messages — and you can turn that off in Settings.**

---

## What data does Evoke store?

Evoke stores the following information:

- **Contact information** you add to the app: names, phone numbers, email addresses, relationship labels, and any notes you write about your contacts
- **Connection history**: dates and methods of your check-ins with each contact
- **Reminders**: scheduled notification times and frequencies you configure
- **Preferences**: your display name, notification settings, appearance preferences, and onboarding choices
- **Contact photos**: thumbnail images imported from your device's Contacts app (only for contacts you explicitly add to Evoke)

## Where is my data stored?

Your data lives in **two places, both private to you**:

1. **Locally on your device**, using Apple's SwiftData framework. This is the primary store; the app reads and writes here first.
2. **In your personal iCloud account** (Apple's CloudKit private database), so the same data is available across all your iPhones, iPads, and Macs signed into the same Apple ID.

Evoke does **not** have servers, databases, or cloud storage of its own. The CloudKit private database is part of Apple's infrastructure under your Apple ID — Apple's privacy and security policies apply, and **the developer of Evoke has no access to your synced data**. We can't read it, can't query it, and can't share it.

If you're not signed into iCloud, or if you turn off iCloud sync in Settings → iCloud Sync, the app continues to work fully — your data just stays on a single device.

The Evoke widget uses a shared App Group container on each device to display your contacts on your home screen. The widget reads a local snapshot only; it does not have its own iCloud connection.

## Does Evoke collect analytics or diagnostics?

Yes — but only anonymous usage and diagnostic data, and you can turn it off. This is **separate from your relationship data**, which never leaves your private iCloud (see above).

Here is exactly what's collected and by whom:

### Anonymous product analytics (PostHog)

Evoke records anonymous product-interaction events to understand how the app is used — for example, which screens are viewed, where people start and finish key flows (onboarding, recording a check-in, sending a message suggestion), and how often features like the paywall are reached. These events carry only **non-identifying properties**: counts and category labels such as a contact count, a check-in outcome (confirmed/declined), a plan name (monthly/annual), or a milestone day number.

These events **never include your name, your contacts' names, phone numbers, email addresses, message contents, notes, or photos.**

- Events are processed by **PostHog**, in PostHog's **EU region** (`eu.i.posthog.com`).
- Evoke uses PostHog in **anonymous mode**. We never call PostHog's user-identification API, so analytics events are **not linked to your name, your Apple ID, or any account**. PostHog assigns a random anonymous identifier to the install.
- **Session replay is turned off.** PostHog does not record your screen.
- Automatic on-screen element capture is turned off — Evoke only sends the specific, named events it instruments deliberately.

### Anonymous diagnostics and crash reporting (Luciq)

Evoke uses **Luciq** for engineering health monitoring so we can find and fix crashes and performance problems:

- **Crash reports** — if the app crashes, Luciq captures the technical crash diagnostics.
- **Performance / app responsiveness data** (APM) — load times, hangs, and similar metrics.
- **Network request diagnostics** — timing and status of the app's network calls. Evoke makes no network requests that carry your personal data in them (your data syncs only through Apple's CloudKit, which Luciq does not see).
- Luciq is also sent the same anonymous usage event **names** described above (without the property details).

Luciq identifies your install with an **anonymous, auto-generated identifier** that persists for the life of the install. It is **not** linked to your name or Apple ID — Evoke never sends Luciq any user attributes or identifying information. **Session replay is turned off** in Luciq as well.

The in-app **bug reporter** (shake-to-report, which can capture a screenshot and an optional name/email when you choose to file a report) is **enabled only in our internal TestFlight/beta builds**. It is **not active in the App Store version of Evoke**, so the production app does not collect bug-report screenshots, names, or emails.

### You can turn analytics and diagnostics off

Analytics and diagnostics are **on by default but optional**. You can turn them off at any time in **Settings → "Diagnostic Analytics"**. When you turn the toggle off:

- Evoke stops sending events and tells PostHog and Luciq to stop collecting.
- Any usage events buffered on your device are cleared.

Whether the toggle is on or off, all of this data is **anonymous** — it is never tied to your identity, and Evoke uses **no advertising, no cross-app or cross-site tracking, no data brokers, and never sells your data**.

## Does Evoke access my device contacts?

Only if you choose to import contacts. During onboarding or later in the app, you can import contacts from your device's Contacts app. This requires your explicit permission via the iOS Contacts permission prompt.

When you import a contact:
- Evoke copies their name, phone number, email, and thumbnail photo into its local database (and your iCloud, if iCloud Sync is on)
- Evoke does **not** continuously sync with your iOS Contacts app — imports are one-time snapshots
- Evoke does **not** transmit your contacts to any developer-controlled server. Synced data goes to your personal iCloud account, which only you can access.
- You can delete imported contacts from Evoke at any time without affecting your iOS Contacts app

If you deny contact access, Evoke works fine. You can add contacts manually.

## Does Evoke send notifications?

Only if you enable them. Evoke uses iOS local notifications to send you reminders about reaching out to your contacts. These notifications are:

- Generated entirely on your device
- Not sent through any external push notification service
- Customizable (timing, frequency, weekday-only)
- Easy to disable at any time from the app or iOS Settings

## Who does Evoke share data with?

Evoke **never shares, sells, or rents your relationship data** (contacts, check-ins, notes, photos, preferences) to anyone. That data stays in your private iCloud and on your device.

The only data shared with third parties is the **anonymous usage and diagnostic data** described above, and only with these two service providers:

- **PostHog** — receives anonymous product-interaction events (non-identifying counts and labels only). PostHog's privacy policy: <https://posthog.com/privacy>
- **Luciq** — receives anonymous crash reports, performance/diagnostics data, network-request diagnostics, and anonymous usage event names. Luciq's privacy policy: <https://www.luciq.ai/privacy>

There are **no advertising SDKs, no data brokers, no social login, and no cross-app tracking.** Both services receive only anonymous, non-identifying data, never used to track you across other apps or sites.

## What about the export feature?

Evoke lets you export all your data as a JSON file. When you use this feature:
- The file is generated locally on your device
- You control where it goes (AirDrop, Files, email, etc.)
- Evoke does not retain a copy or transmit the export anywhere

You can also import a previously exported file to restore your data.

## Your rights

You have full control over your data:

- **View**: All your data is visible within the app at all times
- **Export**: Download a complete copy of your data in JSON format from Settings
- **Delete**: Use "Delete All Data" in Settings to permanently erase everything. This removes all contacts, connections, reminders, preferences, scheduled notifications, and widget data
- **Modify**: Edit or remove any contact, connection, or setting at any time
- **Opt out of analytics**: Turn off "Diagnostic Analytics" in Settings to stop all anonymous usage and diagnostic collection

Since Evoke stores your relationship data only on your device and in your personal iCloud, there is no Evoke-controlled account to delete and no server request needed. "Delete All Data" removes the data from the local device immediately. If iCloud Sync is on, the deletion propagates to your iCloud and then to your other devices. To remove data from iCloud entirely without re-syncing it, you can also delete Evoke's data from iCloud via iOS Settings → [your name] → iCloud → Manage Account Storage → Evoke.

## Children's privacy

Evoke is not directed at children under 13 and does not knowingly collect information from children. If you believe a child has provided data to Evoke, the parent or guardian can delete all data using the "Delete All Data" option in Settings.

## Changes to this policy

If this privacy policy changes, the updated version will be available within the app (Settings > Privacy Policy) and at this URL. The "Last updated" date at the top will reflect the most recent revision.

## Contact

If you have questions about this privacy policy or your data, you can reach us through the Evoke app (Settings > Privacy > Privacy Questions).

---

*Evoke is made by Fares Nabil in Cairo, Egypt.*
