# Theresa Chrome Extension — Privacy Policy

_Last updated: 2026-05-19_

## What the extension is

The Theresa Chrome extension is a companion to the Theresa desktop app. Its
sole purpose is to capture the content of the web page you are actively
viewing and hand it to your locally installed Theresa desktop app, so the
app can use that content as context for AI work assistance.

## What we collect

When you visit a web page, the extension reads:

- The page **URL**
- The page **title**
- The **visible text content** of the page (up to 5,000 characters)

That is the entire data set the extension touches.

## What we do NOT collect

- Form input values, passwords, credit card numbers, or hidden fields
- Cookies, authentication tokens, or session identifiers
- Browsing history outside of pages you are actively viewing
- Data from background tabs you are not looking at
- Mouse movements, keystrokes, scroll position, or click events
- Anything from pages you have not opened

## Where the data goes

The extension sends captured page data **only** to the Theresa desktop
application running on your own machine, via the loopback address
`http://127.0.0.1:7891`. The extension itself does **not** contact any
remote server, cloud service, analytics provider, or third party.

What the desktop app does with the data after it receives it:

- The Theresa desktop app may forward content to your account on
  Theresa's backend service (`*.us-central1.run.app`) **only when you are
  signed in and observing is enabled**.
- You can pause observing at any time from the desktop app's UI.
- All data is stored under your authenticated account and is scoped to
  your organization.

## Data retention and deletion

Data is retained under your authenticated Theresa account. You can:

- Pause data capture at any time from the desktop app
- Uninstall the Chrome extension to immediately stop new capture
- Request account deletion through the desktop app or by contacting
  support, which removes associated stored content

## Privacy controls built into the extension

- **Per-URL throttling**: the same URL is not re-captured within
  30 seconds, even if you switch tabs back and forth.
- **Length cap**: only the first 5,000 characters of visible text are
  extracted from any page.
- **Visible text only**: form fields, password inputs, and hidden DOM
  nodes are never read.
- **Local-only transport**: outbound network calls go exclusively to
  `127.0.0.1` (your own machine). The extension cannot reach the
  public internet on its own.

## Permissions explained

| Permission | Why it's needed |
|---|---|
| `host_permissions: http://127.0.0.1:7891/*` | To send captured content to the Theresa desktop app running on your own machine. |
| `content_scripts` on `<all_urls>` | The extension needs to be able to capture content on whatever work-related page you happen to be on (intranet sites, SaaS dashboards, docs, etc.). It does not pre-target any specific site, and it does not run on pages you have not opened. |

The extension does **not** request `activeTab`, `tabs`, `cookies`,
`history`, `storage`, `webRequest`, or any other Chrome API permission.

## Remote code

The extension does not load, evaluate, or execute any code fetched from
a remote source at runtime. All extension JavaScript ships inside the
Chrome Web Store package and is reviewed by the Web Store at upload time.

## Contact

Questions or requests about this policy:
**support@theresa.app**
