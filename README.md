# n8n CAPTCHA Solver Node by CapMonster Cloud

[![npm version](https://img.shields.io/npm/v/@zennolab_com/n8n-nodes-capmonstercloud.svg)](https://www.npmjs.com/package/@zennolab_com/n8n-nodes-capmonstercloud)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The ultimate **CAPTCHA solver and anti-bot bypass node** for n8n. 

Easily integrate CapMonster Cloud into your n8n workflows to automatically bypass complex protections like reCAPTCHA, Cloudflare Turnstile, and DataDome in your web scraping and automation pipelines. The fastest AI-powered recognition API on the market.

**[👉 Get your Free API Key and Start Bypassing CAPTCHAs](https://dash.capmonster.cloud/Account/SignUp?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_readme)**

---

## ⚡ Supported CAPTCHAs to Bypass

This node provides ready-to-use operations to solve the following challenges:
- **reCAPTCHA** (v2, v2 Enterprise, v3, v3 Enterprise)
- **Cloudflare Turnstile** (Token, Managed Challenge, Waiting Room bypass)
- **FunCaptcha**
- **GeeTest** (V3 and V4)
- **Image-to-Text** (Standard image captchas)
- **Complex image tasks** (Click and recognition)
- **Enterprise Anti-Bot Systems:** DataDome, Imperva, Amazon variants, Binance, Basilisk, TenDI, Prosopo, Temu, Yidun, MTCaptcha, Altcha, Castle, TSPD, and Hunt.

*Note: Some task types support optional proxy parameters for residential/mobile routing to avoid IP bans.*

## ⚙️ Requirements

- n8n with community nodes enabled
- A CapMonster Cloud account
- A valid CapMonster Cloud API key

## 📦 Installation

Install the solver package as a community node directly in n8n via npm:

```bash
npm install @zennolab_com/n8n-nodes-capmonstercloud
```
*(You can also search and install it directly from the n8n Community Nodes UI).*

## 🔐 Credentials Setup

This node uses one credential to connect to our solver API:

- **CapMonster Cloud API**
  - `Client Key`: Your unique API key from the [CapMonster Cloud Dashboard](https://dash.capmonster.cloud/Account/SignUp?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_readme)

## 🚀 How to use the CAPTCHA Solver

1. Add the **CapMonster Cloud** node to your n8n workflow.
2. Select or create your **CapMonster Cloud API** credentials.
3. Choose the target protection system in **Task Type** (e.g., Cloudflare or reCAPTCHA).
4. Fill in the required fields (e.g., target `websiteURL`, `websiteKey` / `sitekey`).
5. Execute the node.

The node automatically submits the task to CapMonster, polls the API, and returns the bypass token directly in the node output for your next HTTP Request.

### Custom JSON Task Example

When using the generic JSON operation, provide a valid CapMonster task object (without the `clientKey`):

```json
{
  "type": "RecaptchaV2Task",
  "websiteURL": "https://lessons.zennolab.com/captchas/recaptcha/v2_simple.php?level=high",
  "websiteKey": "6Lcg7CMUAAAAANphynKgn9YAgA4tQ2KI_iqRyTwd"
}
```

## 📊 Output Response

The node returns the solved task response directly from the CapMonster Cloud API, including the `gRecaptchaResponse` or Turnstile token needed to bypass the target form.

## 🛠 Troubleshooting

- Verify your API key is active and has balance in your CapMonster dashboard.
- Confirm all required fields (like `sitekey`) are scraped correctly from the target page.
- For JSON tasks, ensure the payload strictly matches the [API schema](https://docs.capmonster.cloud/docs/captchas/).
- If a task requires proxy data (e.g., for Turnstile or DataDome), ensure you provide a clean, working proxy host and port.

## 🖼 UI Configuration Examples

Use the screenshots below as a quick visual reference for setting up the node in n8n.

### Selecting the CAPTCHA Type
![n8n Cloudflare and reCAPTCHA bypass node](images/selectCaptcha1.png)

### API Credentials Setup
![CapMonster Cloud API key setup in n8n](images/keyNode.png)

## 📚 Official Documentation

- [CapMonster Cloud Main Documentation](https://docs.capmonster.cloud/)
- [CAPTCHA Task Reference & Bypass Guides](https://docs.capmonster.cloud/docs/captchas/)
- [n8n Community Nodes Guide](https://docs.n8n.io/integrations/community-nodes/)

## 📄 License
[MIT](LICENSE)
