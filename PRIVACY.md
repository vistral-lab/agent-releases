# Vistral Agent Chrome Extension — Privacy Policy

_Last updated: 2026-05-14_

## What this extension does

The Vistral Agent Chrome Extension is a companion to the **Vistral Agent
desktop application**. When you have the desktop app installed and running,
the extension captures the visible text of the page you are currently
viewing and sends it to the desktop app so it can understand your work
context.

## What we collect

When you have the extension installed and the desktop app running, the
extension reads:

- The **visible text content** of your active browser tab (limited to
  ~5,000 characters per page)
- The **URL** of the active tab
- The **page title** of the active tab
- A **timestamp** of when the content was captured

Content is captured when you switch tabs, when the URL changes, when a
page becomes visible after being inactive, and at throttled intervals
(same URL is not re-captured within 30 seconds).

## What we do NOT collect

- Form input values (including text fields, login forms, payment fields)
- Passwords or any credentials
- Cookies or authentication tokens
- Hidden DOM elements (`display: none`, `visibility: hidden`)
- Content from tabs you are not actively viewing
- Browser history outside the current session
- Images, video, audio, or any binary content

## Where the data goes

The extension communicates **only** with the Vistral Agent desktop
application running on your own machine at `http://127.0.0.1:7891`.

**The extension itself does NOT send any data to remote servers.**

The Vistral Agent desktop application may forward this data to your
authenticated account on Vistral's backend (operated by DJAI Lab,
hosted on Google Cloud Run, `us-central1`) — but **only** when:
1. You are signed in to the desktop application, AND
2. You have enabled "Observe" mode in the desktop application.

You can pause Observe mode at any time in the desktop application.
While paused, no data is forwarded to the cloud regardless of what
the extension captures.

If the desktop application is not running, the extension fails
silently and no data is captured anywhere.

## Data retention

- Captured data is stored under your authenticated account in the
  Vistral cloud backend, scoped to your user ID.
- You can delete your account in the desktop application's settings;
  doing so removes all data associated with your account.
- We do not sell, share, or otherwise disclose your data to third
  parties for advertising or marketing purposes.

## Permissions explained

| Permission | Why we need it |
|---|---|
| `activeTab` | Read the title of the tab you are actively viewing. |
| `host_permissions: http://127.0.0.1:7891/*` | POST captured content to the desktop application running on localhost. This is the only network endpoint the extension talks to. |
| `<all_urls>` (content script) | Required because users work across many domains (GitHub, internal docs, Slack, Gmail, etc.) — the extension needs to be able to read text from whichever site is currently active. We do not target specific sites or harvest data cross-site. |

## Changes to this policy

If we make material changes to this policy, we will update the
"Last updated" date at the top and notify users through the desktop
application.

## Contact

For questions about this privacy policy or data practices, contact:
**support@djailab.com**

DJAI Lab
