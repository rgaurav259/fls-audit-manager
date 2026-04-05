# 🔐 FLS Audit Manager for Salesforce

> Audit and fix Field-Level Security across all Salesforce profiles — directly from Chrome.

[![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Available-blue?logo=googlechrome)](https://chrome.google.com/webstore)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Manifest V3](https://img.shields.io/badge/Manifest-V3-orange)](https://developer.chrome.com/docs/extensions/mv3/)

---

## What It Does

FLS Audit Manager solves one of the most painful Salesforce admin tasks — auditing Field-Level Security across dozens of profiles. Instead of clicking through Setup for every field on every object, this extension gives you a complete audit matrix in seconds.

### Key Features

| Feature | Description |
|---|---|
| 🔍 **Audit** | See FLS status for every field across all profiles in one table |
| ❌ **Detect Missing** | Instantly find fields invisible to profiles |
| ✅ **Grant FLS** | Click one cell or use "Grant All" per row |
| ⚡ **Bulk Fix** | Fix all missing FLS for all profiles at once |
| 🗑 **Bulk Revoke** | Remove all FLS from selected profiles |
| 📊 **Export CSV** | Full audit report as a downloadable CSV |
| 🔐 **Secure** | No data leaves your browser — direct Salesforce API only |

---

## Screenshots

*(Add screenshots here after publishing)*

---

## Installation

Install from the [Chrome Web Store](#) *(link after publishing)*

---

## How To Use

1. Open your Salesforce org in Chrome and log in
2. Click the 🔐 FLS Audit Manager icon in your toolbar
3. Click **Open FLS Audit Panel**
4. Select an object and one or more profiles
5. Click **▶ Run Audit**
6. View results — click any cell to toggle FLS, or use bulk buttons

---

## Supported Salesforce Environments

- Production orgs (`*.my.salesforce.com`)
- Sandboxes (`*.sandbox.my.salesforce.com`)
- Developer Edition orgs (`*.develop.my.salesforce.com`)
- Scratch orgs (`*.scratch.my.salesforce.com`)

---

## Privacy

This extension collects **zero data**. It makes direct API calls from your browser to your Salesforce org. No external servers. No analytics. No tracking.

Full privacy policy: [View Privacy Policy](https://rgaurav259.github.io/fls-audit-manager/privacy-policy.html)

---

## License

MIT License — free to use, modify and distribute with attribution.

© 2026 Gaurav Kumar

---

## Version History

See [CHANGELOG.md](CHANGELOG.md)
