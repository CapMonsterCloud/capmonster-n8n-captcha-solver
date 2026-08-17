# n8n CAPTCHA Solver Node by CapMonster Cloud

<p align="center">
  <a href="https://capmonster.cloud/en/?utm_source=github&utm_medium=readme&utm_campaign=n8n_repo">
    <img src="https://raw.githubusercontent.com/CapMonsterCloud/capmonster-captcha-solver-docs/main/assets/capmonster_logo.png" alt="CapMonster Cloud Logo" width="320">
  </a>
</p>

<p align="center">
  <strong>Fast, AI-powered CAPTCHA solver and anti-bot bypass community node for n8n.</strong>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@zennolab_com/n8n-nodes-capmonstercloud"><img src="https://img.shields.io/npm/v/@zennolab_com/n8n-nodes-capmonstercloud.svg?style=flat-square&color=blue" alt="npm version"></a>
  <a href="https://www.npmjs.com/package/@zennolab_com/n8n-nodes-capmonstercloud"><img src="https://img.shields.io/npm/dm/@zennolab_com/n8n-nodes-capmonstercloud.svg?style=flat-square&color=green" alt="npm downloads"></a>
  <a href="https://github.com/CapMonsterCloud/capmonster-n8n-captcha-solver/stargazers"><img src="https://img.shields.io/github/stars/CapMonsterCloud/capmonster-n8n-captcha-solver?style=flat-square&color=yellow" alt="GitHub Stars"></a>
  <a href="https://github.com/CapMonsterCloud/capmonster-n8n-captcha-solver/network/members"><img src="https://img.shields.io/github/forks/CapMonsterCloud/capmonster-n8n-captcha-solver?style=flat-square" alt="GitHub Forks"></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-orange.svg?style=flat-square" alt="License: MIT"></a>
</p>

---

Easily integrate **CapMonster Cloud** into your n8n workflows to automatically solve and bypass complex protections like **reCAPTCHA v2/v3/Enterprise, Cloudflare Turnstile, DataDome, GeeTest, and hCaptcha** in your web scraping and workflow automation pipelines.

**[👉 Get your Free API Key & Free Trial Balance on CapMonster Cloud](https://dash.capmonster.cloud/Account/SignUp?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_readme)**

---

## ⚡ Quick Start: 30-Second Workflow Setup

You can copy and paste this ready-to-use n8n workflow directly into your canvas:

```json
{
  "nodes": [
    {
      "parameters": {
        "taskType": "RecaptchaV2Task",
        "websiteURL": "https://lessons.zennolab.com/captchas/recaptcha/v2_simple.php?level=high",
        "websiteKey": "6Lcg7CMUAAAAANphynKgn9YAgA4tQ2KI_iqRyTwd"
      },
      "id": "1e5f8a20-3b42-4f11-9a7c-capmonster01",
      "name": "CapMonster Cloud",
      "type": "@zennolab_com/n8n-nodes-capmonstercloud.capMonsterCloud",
      "typeVersion": 1,
      "position": [460, 300],
      "credentials": {
        "capMonsterCloudApi": {
          "id": "1",
          "name": "CapMonster Cloud Account"
        }
      }
    }
  ],
  "connections": {}
}
```

> **How to import:** Copy the JSON snippet above, open your n8n editor canvas, and press `Ctrl+V` (or `Cmd+V`).

---

## 📦 Installation

### Method 1: Via n8n Community Nodes UI (Recommended)
1. Go to **Settings > Community Nodes** in your n8n instance.
2. Select **Install**.
3. Enter `@zennolab_com/n8n-nodes-capmonstercloud` in the npm package name field.
4. Check the box agreeing to the risks of community nodes and click **Install**.

### Method 2: Via Command Line (Docker / Self-hosted)
Inside your n8n root directory:
```bash
npm install @zennolab_com/n8n-nodes-capmonstercloud
```

---

## 🔐 Credentials Setup

1. In n8n, navigate to **Credentials > New Credential**.
2. Search for **CapMonster Cloud API**.
3. Paste your `Client Key` from your [CapMonster Cloud Dashboard](https://dash.capmonster.cloud/Account/SignUp?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_readme).
4. Save credentials.

---

## 🛡️ Supported CAPTCHA Types & Anti-Bot Protections

| Protection Type | Supported Task Variants | Proxy Required? |
| :--- | :--- | :--- |
| **Cloudflare Turnstile** | Managed Challenge, Token, Waiting Room | Optional / Recommended for strict mode |
| **reCAPTCHA** | v2, v2 Enterprise, v3, v3 Enterprise | Optional |
| **GeeTest** | v3, v4 | Optional |
| **FunCaptcha (Arkose Labs)** | Standard & Audio challenges | Optional |
| **Image-to-Text** | Classic standard image text | No |
| **Complex Image Grid** | Coordinates click, bounding boxes | No |
| **Enterprise Anti-Bot** | DataDome, Imperva, Amazon WAF, Binance, TenDI, Castle, TSPD | Yes (Custom Proxy) |

---

## 🚀 How It Works in Your Pipeline

```text
[ Trigger: Webhook / Schedule ]
              │
              ▼
    [ HTTP Request: Target Page ] ──► Extracts sitekey & pageURL
              │
              ▼
  [ 🤖 CapMonster Cloud Node ] ──► Sends task & polls solution asynchronously (< 1s)
              │
              ▼
[ HTTP Request: Submit Form ] ──► Injects gRecaptchaResponse / Turnstile token
```

The node automatically handles polling, backoff retries, and token delivery directly into JSON output parameters (`gRecaptchaResponse`, `token`, etc.).

---

## 🖼️ UI Setup Reference

### 1. Selecting CAPTCHA Protection Type
![Select CAPTCHA Type](images/selectCaptcha1.png)

### 2. Configuring API Key Credentials
![API Key Setup](images/keyNode.png)

---

## 🛠️ Troubleshooting & Best Practices

- **Token Expiration:** CAPTCHA tokens typically expire in 120 seconds. Ensure your next HTTP Request executes immediately after the CapMonster node.
- **Proxy Matching:** For Cloudflare Turnstile or DataDome, use residential proxies with the same IP/subnet that makes the initial page request.
- **Custom JSON Payload:** If using custom JSON payloads, follow the official [CapMonster Task API Reference](https://docs.capmonster.cloud/docs/captchas/).
- **Zero Balance:** Make sure your dashboard balance is positive. Grab free testing credits from your [Dashboard](https://dash.capmonster.cloud/?utm_source=github&utm_medium=readme&utm_campaign=n8n_repo).

---

## 📚 Documentation & Community

- 📖 [Official CapMonster Cloud Documentation](https://docs.capmonster.cloud/)
- 🎯 [Task API Reference & Payload Specs](https://docs.capmonster.cloud/docs/captchas/)
- 🧩 [n8n Community Nodes Directory](https://docs.n8n.io/integrations/community-nodes/)
- 💬 [CapMonster Community & Support](https://capmonster.cloud/en/?utm_source=github&utm_medium=readme&utm_campaign=n8n_repo#support)

---

## ⭐ Star History

If you find this node helpful for your web scraping and automation workflows, please consider giving us a star on GitHub!

[![Star History Chart](https://api.star-history.com/svg?repos=CapMonsterCloud/capmonster-n8n-captcha-solver&type=Date)](https://star-history.com/#CapMonsterCloud/capmonster-n8n-captcha-solver&Date)

---

## 📄 License

[MIT](LICENSE) © [CapMonster Cloud](https://capmonster.cloud/)
