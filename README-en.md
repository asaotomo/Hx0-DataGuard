# Hx0 DataGuard

[![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-v1.0.6-4285F4?style=flat-square&logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/hx0-%E6%95%B0%E6%8D%AE%E5%8D%AB%E5%A3%AB/hkhjbfajliglkonhfpkfkkdcdobikfig)
![Firefox AMO](https://img.shields.io/badge/Firefox%20AMO-1.0.6-FF7139?style=flat-square&logo=firefoxbrowser&logoColor=white)
![Form](https://img.shields.io/badge/Form-Browser%20Extension-007AFF?style=flat-square)
![Compute](https://img.shields.io/badge/Compute-Local%20First-4CAF50?style=flat-square)
![Capability](https://img.shields.io/badge/Capability-Sensitive%20Data%20Scan-E879F9?style=flat-square)
![Capability](https://img.shields.io/badge/Capability-API%20Path%20Discovery-3B82F6?style=flat-square)
![Capability](https://img.shields.io/badge/Capability-Input%20Leak%20Guard-EC4899?style=flat-square)
![Capability](https://img.shields.io/badge/Capability-Rule%20Center-5856D6?style=flat-square)
![Capability](https://img.shields.io/badge/Capability-Report%20Export-0EA5E9?style=flat-square)

**English** · [简体中文](README.md)

> Your local security assistant in the browser — scan page risks, discover suspicious paths, guard against input leaks, and export reports in one click.

**Now available on [Chrome Web Store](https://chromewebstore.google.com/detail/hx0-数据卫士/hkhjbfajliglkonhfpkfkkdcdobikfig)(v1.0.6)** · **[Firefox Add‑ons](https://addons.mozilla.org/zh-CN/firefox/addon/hx0-数据卫士/)(v1.0.3)** · Firefox version (v1.0.6) submitted for review — coming soon

## What It Is

Hx0 Data Guardian​ is a **local** sensitive data assistant detection extension developed by **Hx0 Team** that runs within your browser. During your daily web browsing, it works quietly in the background to do two things for you:

- **Look outward**: scan the current page and its scripts for exposed secrets and API-style endpoint clues
- **Guard inward**: detect sensitive content in what you type or paste into AI chats, forms, and messaging boxes — **before you send**

Scan results stay on **your device** by default — page content is not uploaded — making it suitable for everyday protection, security self-checks, and report archival.

<img width="1672"  alt="Hx0 数据卫士-宣传海报-en" src="https://github.com/user-attachments/assets/742e90dd-e986-477a-9f3c-6247524103e7" />

---

## Why We Built It

We kept seeing two problems get worse:

**First, AI workflows make accidental leaks easier.** More people paste logs, configs, and customer data straight into ChatGPT, Claude, or similar tools. Once sent, it’s often irreversible; manual redaction is slow and easy to get wrong.

**Second, front-end exposure review is still fragmented.** During authorized security testing, teams jump between tools to find hard-coded keys, debug endpoints, and API paths that shouldn’t live in the browser. For developers and site owners, undetected issues keep widening the attack surface.

Enterprise DLP is heavy and expensive; manual checking doesn’t scale. Hx0 DataGuard fills that gap — **page exposure scanning and input leak protection, inside the browser, local by default, ready when you need it.**

---

## Problems It Solves

| Pain point | How Hx0 DataGuard helps |
|------------|-------------------------|
| Pasting keys, connection strings, or internal docs into AI chats by mistake | **Input leak guard** detects and warns or blocks **before send** — no tedious manual redaction |
| Plaintext secrets hiding in authorized site front-ends | **Page sensitive-data scan** inspects DOM and scripts with hit context |
| API paths, admin routes, or internal URLs exposed in external JavaScript | **API detection** surfaces path assets to shrink unnecessary exposure |
| Hard to keep or hand off scan results | **Report export** to HTML, Markdown, or JSON for tracking and remediation |
| Worry that detection tools upload page content to the cloud | **Local-first** — data stays on your machine; no account sign-up required |

> **Disclaimer**: Outputs are for **assistance only**. They do **not** replace formal penetration testing, secure code review, or compliance verdicts.

---

## New User Offer

**Get a free 1-day VIP trial** on first install — full access to every feature, no account registration required.

After the trial, subscribe from **Settings** in the extension to continue. **Back up your User ID immediately** — in our no-registration model, it is the only credential for recovering your membership.

---

## What’s New in v1.0.3

Highlights since v1.0.2:

| Area | Changes |
|------|---------|
| **Page / JS scan** | Hits show exact source (main document, inline script, external JS, HTML comment, etc.); hover long filenames for full paths; copy uses the **raw matched value** |
| **Rule center** | New **Page comments** category (on by default) scans HTML comments for credentials, env vars, TODO/FIXME markers, and similar clues |
| **API probing** | Batch HTTP probes support custom **interval**, **concurrency**, and **per-request timeout**; with “Include cookies”, request previews show the Cookie header; export to JSON / Markdown / CSV |
| **Input leak guard** | Better coverage on complex AI sites and custom inputs; top-right toast lists **all hits** while typing; center block dialog on send for rules marked “Block on hit” |
| **Fixes** | Firefox side-panel report export; paste/mask toasts follow English UI; smoother Chrome download permission on export |

See **Settings → User manual → v1.0.3 Updates** in the extension for full details.

---

## Core Capabilities

| Capability | What it does |
|------------|--------------|
| **Input leak guard** | Detects phone numbers, keys, tokens, ID numbers, and similar data **before you send** — while typing or pasting into AI chats, forms, or messaging boxes — then warns or blocks |
| **Page sensitive-data scan** | Scans the current page DOM, scripts, and comments for exposed sensitive patterns, with hit context for manual review |
| **API detection** | Extracts API paths, webhooks, internal URLs, and other endpoint clues from pages and external JavaScript; optional probing to verify |
| **Rule center** | Built-in rules plus custom rules, categories, and import/export — tune detection to your team’s standards |
| **Report export** | Export findings as HTML, Markdown, or JSON for archival, handoff, or remediation tracking |

---

## Typical Use Cases

### Chatting with AI without accidentally leaking sensitive data

It’s easy to paste a log snippet, config file, or customer note into ChatGPT, Claude, or other AI tools without noticing an **API key, DB connection string, phone number, or internal document** mixed in — one click and it’s sent.

Manual redaction is slow and error-prone: scan line by line, replace, paste again, and still miss something. **Input leak guard** scans what you type or paste **before send**:

- Alerts you when sensitive patterns are found so you can confirm or cancel
- **Strict mode** can block send entirely to reduce mistakes
- Works out of the box on popular AI sites; other web inputs are covered too

> Enable in the popup: **Input & send monitoring** and **Clipboard paste monitoring**; set strength in side panel **Settings**.

<img width="1956" height="1086" alt="image" src="https://github.com/user-attachments/assets/d2e3214a-9af6-4f8d-95f6-93e732e67ecd" />

<img width="1956" height="1086" alt="image" src="https://github.com/user-attachments/assets/471e46c3-7ca5-4ae9-9988-8483d229cac4" />

<img width="1956" height="1086" alt="image" src="https://github.com/user-attachments/assets/266f9deb-9c16-4fb6-b2e3-61429da5e8e4" />

<img width="1950" height="390" alt="image" src="https://github.com/user-attachments/assets/67e52ea5-5b4b-4d5f-99c7-52d89c9c8c30" />

---

### Security testing: find exposed secrets and API surface on authorized sites

Front-end pages and external scripts often hide **things that shouldn’t be public**: debug endpoints, admin paths, hard-coded tokens, test accounts, or API URLs that belong on the server, not in the browser. Each one widens the attack surface.

Within **properly authorized** test scope, Hx0 DataGuard helps you map exposure quickly in the browser:

1. Open the target page and run **Scan current page for sensitive info & APIs**
2. Review **Page risks** — plaintext keys, phone numbers, ID numbers, etc.
3. Review **API detection** — paths like `/api/admin/`, `/internal/debug`, and similar assets pulled from scripts
4. Export a report for developers or the site owner to fix

You get faster visibility into **unnecessary exposure** without standing up a heavy toolchain — helping sites shrink their attack surface and lower risk.

<img  alt="image" src="https://github.com/user-attachments/assets/a6220189-9006-4a50-8b5e-e54965f2d03c" />

<img  alt="image" src="https://github.com/user-attachments/assets/1f4eb669-83ca-45c8-9cee-03373a88a03a" />

<img  alt="image" src="https://github.com/user-attachments/assets/c9269202-bb67-40f3-8167-bcce0eb46b17" />

<img  alt="image" src="https://github.com/user-attachments/assets/d878ffe5-b1a3-44c7-b035-22c05df8a5be" />

<img  alt="image" src="https://github.com/user-attachments/assets/4bcef54c-37b7-4fb5-a5a7-4cb02b8702f8" />

<img  alt="image" src="https://github.com/user-attachments/assets/27c25e7a-f707-482e-a807-ad06f6833258" />

<img  alt="image" src="https://github.com/user-attachments/assets/da29d29a-b2cc-4c21-b610-408d5a7748ee" />


> Use scanning and probing only on systems you are authorized to test. Always manually verify hits; comments, decoys, and test fixtures can look like real leaks.

---

### Dev & QA: quick check before release

Before shipping or during integration, developers and QA can scan a page to see if test keys, internal URLs, or real user data accidentally made it into the DOM or linked scripts — and fix issues before they go live.

---

## Quick Start

### 1. Download & Install

#### Option A: Chrome Web Store (recommended)

The latest release is live on the Chrome Web Store — **one-click install with automatic updates**, no manual unzip or developer mode required.

👉 **[Install Hx0 DataGuard from the Chrome Web Store](https://chromewebstore.google.com/detail/hx0-%E6%95%B0%E6%8D%AE%E5%8D%AB%E5%A3%AB/hkhjbfajliglkonhfpkfkkdcdobikfig)**

Works on Chrome and other Chromium browsers that support Chrome extensions (e.g. Edge, Brave). Pin the icon to your toolbar after install.

#### Option B: Offline package (CRX / XPI)

If you **cannot access the stores** (e.g. restricted network), download the offline installer from [Releases](../../releases):

| Browser | Package |
|---------|---------|
| Chrome / Edge / Brave, etc. | `Hx0-DataGuard-chrome-*.crx` |
| Firefox | `Hx0-DataGuard-firefox-*.xpi` |

**Chrome / Edge / Brave (`.crx`)**

1. Download **`Hx0-DataGuard-chrome-*.crx`**
2. Open extension management (`chrome://extensions`, `edge://extensions`, or `brave://extensions`)
3. Enable **Developer mode** (top-right)
4. **Drag** the `.crx` file onto the extensions page
5. Click **Add extension** in the confirmation dialog

**Firefox (`.xpi`)**

1. Download **`Hx0-DataGuard-firefox-*.xpi`**
2. Open `about:addons` in Firefox
3. Click the **gear icon** → **Install Add-on From File…**
4. Select the downloaded `.xpi` and confirm

> You can also drag the `.xpi` into a Firefox window to install.  
> Offline installs do not auto-update. Download a new Release when updates ship, or switch to the store build.

#### Firefox

The Firefox build has been submitted to **AMO (Firefox Add-ons)** and will be **available soon**. A store link will be posted here and in [Releases](../../releases) once approved; until then, install the **`.xpi`** from Releases for offline use.

> Pin the extension icon to your toolbar for daily use.

### 2. First Launch

1. Click the toolbar icon and accept the Terms & Privacy Policy
2. If a **User ID** is shown, copy and save it right away
3. New users automatically receive a **1-day VIP trial** with full access

### 3. Scan the Current Page

1. Open the page you want to inspect
2. Click the extension icon and confirm the host
3. Click **Scan current page for sensitive info & APIs**
4. Open the **side panel** and review results under Dashboard, Page risks, API detection, etc.

### 4. Enable Input Leak Guard

In the extension **popup**:

- Turn on **Input & send monitoring** — master switch for text inputs (login pages excluded)
- Optionally turn on **Clipboard paste monitoring** — confirm before pasting sensitive text

In the side panel **Settings**, choose alert/block strength (Light / Standard / Strict) and add trusted sites to the allowlist. **Snooze** in the popup skips the current site for 24 hours.

### 5. Export Reports

After scanning, open **Reports** in the side panel and export HTML, Markdown, or JSON. Export important runs promptly for backup.

---

## Membership

Hx0 DataGuard is **paid software** — full features require an active VIP membership.

| Item | Details |
|------|---------|
| New user offer | **1-day VIP trial** on first install |
| Subscribe | Side panel or popup → **Settings** → **Subscribe** |
| User ID | No sign-up; the User ID shown in the UI is your membership credential — **back it up** |
| Recovery | If you lose your ID, contact support below with your old ID and payment proof |

---

## FAQ

**No scan results?**  
The page may have little scannable content; some external scripts may be skipped due to permissions or timeouts — in-page results are still kept.

**Input guard not working?**  
Ensure **Input & send monitoring** is on in the popup; check allowlist or snooze for the current site.

**Lost membership after reinstall?**  
Contact support with your backed-up User ID; recovery may not be possible without the old ID.

**When will Firefox be available?**  
The Firefox add-on is under AMO review. A store link will be added to this README and Releases once approved.

---

## Feedback & Support

- **Issues**: [Open an Issue](../../issues)
- **Email**: hx0studio@foxmail.com
- **User manual**: **Settings → User manual** inside the extension
- **Legal & privacy**: **Settings → Terms & Privacy Policy** inside the extension

---

## License

See [LICENSE](LICENSE) at the repository root.

