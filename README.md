# CapMonster Cloud n8n Node: n8n Captcha Solver & Captcha Bypass for reCAPTCHA, Cloudflare Turnstile and GeeTest

> **🔄 Migrating from 2Captcha or Capsolver?** CapMonster Cloud is a fast, cost-effective **2captcha alternative** and **capsolver alternative** for n8n workflows: reCAPTCHA v3 from **$0.90 per 1,000 solves**, which is **up to 38% cheaper than 2Captcha** and **10% cheaper than Capsolver**, with an API response time of **≤ 2 s**. Already have software built for 2Captcha? CapMonster Cloud [supports the 2Captcha API format](https://docs.capmonster.cloud/docs/external-services/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read). Replacing your solver step takes just a few clicks: see the **Migration examples** below. Full comparison and disclaimer are in the comparison section below.

<p align="center">
  <a href="https://capmonster.cloud/en/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read">
    <img src="https://img.shields.io/badge/CapMonster%20Cloud-AI%20Captcha%20Solver-00B2FF?style=for-the-badge&logo=cloud&logoColor=white" alt="CapMonster Cloud n8n node - captcha solver and captcha bypass for n8n workflows" height="40">
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
  <a href="./LICENSE"><img src="https://img.shields.io/badge/License-MIT-orange.svg?style=flat-square" alt="License: MIT"></a>
</p>

---

Easily integrate **CapMonster Cloud** into your n8n workflows to automatically solve and bypass complex protections like **reCAPTCHA v2/v3/Enterprise, Cloudflare Turnstile, DataDome, and GeeTest** in your web scraping and workflow automation pipelines. As the official CapMonster node for n8n, it is a cost-effective 2captcha alternative and capsolver alternative for no-code captcha bypass.

**[👉 Get your Free API Key & Free Trial Balance on CapMonster Cloud](https://dash.capmonster.cloud/Account/SignUp?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)**

---

## ⚡ Highlights

- ⚡ **Fast solving:** AI-based recognition, on average between 1 and 30 seconds depending on the captcha type.
- 🤖 **Zero human workers:** 100% automated machine learning pipeline with no manual latencies.
- 🛡️ **Modern anti-bot bypass:** Support for Cloudflare Turnstile, reCAPTCHA Enterprise, GeeTest, DataDome and more.
- 🧩 **No-code ready:** Drop the node into any workflow, no custom code or HTTP polling logic required.
- 🔁 **Automatic polling:** The node creates the task, polls the result and returns the token in the JSON output.
- 💰 **Cost-effective:** Low-cost pricing structure based on pay-as-you-go balance.
- 📉 **Cheaper than alternatives:** reCAPTCHA v3 from $0.90 per 1,000 solves, versus $1.45 at 2Captcha and $1.00 at Capsolver.
- 🔄 **Easy migration:** replace your 2Captcha or Capsolver solver step and keep the rest of your workflow unchanged.
- 📖 **Official docs:** task types follow the [CapMonster Cloud API documentation](https://docs.capmonster.cloud/docs/captchas/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

---

## 📊 CapMonster Cloud vs 2Captcha vs Capsolver

Looking for a 2captcha alternative or a capsolver alternative for n8n web scraping and workflow automation? Compare price, speed and success rate.

### reCAPTCHA v3

| Parameter | CapMonster Cloud | 2Captcha | CapSolver | DeathByCaptcha |
| :--- | :---: | :---: | :---: | :---: |
| Price per 1,000 solves (from) | **$0.90** | $1.45 | $1.00 | $2.89 |
| API response time | **≤ 2 s** | ≤ 2 s | < 3 s | ≤ 3 s |
| Solving success rate | **up to 99%** | ~77–92% | ~95–98% | ~64–90% |

*Disclaimer: 2Captcha, CapSolver, and DeathByCaptcha are trademarks of their respective owners. CapMonster Cloud is not affiliated with these entities. Performance metrics and pricing comparisons are based on publicly available data and internal benchmarking conducted on 27.09.2026.*

### Cloudflare Turnstile

| Parameter | CapMonster Cloud | 2Captcha | Anti-Captcha | DeathByCaptcha |
| :--- | :---: | :---: | :---: | :---: |
| Price per 1,000 solves (from) | **$1.30** | $1.45 | $2.00 | $2.89 |
| Time to solve | **6.24 s\*** | 16.9 s | 20.33 s | ~13 s |
| Solving success rate | **99%\*** | 96% | 96% | 96% |

*Disclaimer: 2Captcha, Anti-Captcha, and DeathByCaptcha are trademarks of their respective owners. CapMonster Cloud is not affiliated with these entities. Performance metrics and pricing comparisons are based on publicly available data and internal benchmarking as of 12.10.2026.*

**What this means in practice:**

- **reCAPTCHA v3:** $0.90 versus $1.45 at 2Captcha is up to 38% cheaper, and $0.90 versus $1.00 at Capsolver is 10% cheaper.
- **Cloudflare Turnstile:** $1.30 versus $1.45 at 2Captcha is 10% cheaper, and a solving time of 6.24 s versus 16.9 s is more than 60% faster.

---

## 📦 Installation

Unverified community nodes can be installed on self-hosted n8n instances; they are not available on n8n Cloud.

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

### Credentials Setup

1. In n8n, navigate to **Credentials > New Credential**.
2. Search for **CapMonster Cloud API**.
3. Paste your `Client Key` from your [CapMonster Cloud Dashboard](https://dash.capmonster.cloud/Account/SignUp?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).
4. Save credentials.

---

## 🚀 Quick Start: Solve and Bypass Captchas in n8n

You can copy and paste this ready-to-use n8n workflow directly into your canvas:

```json
{
  "nodes": [
    {
      "parameters": {
        "taskType": "RecaptchaV2Task",
        "websiteURL": "[https://lessons.zennolab.com/captchas/recaptcha/v2_simple.php?level=high](https://lessons.zennolab.com/captchas/recaptcha/v2_simple.php?level=high)",
        "websiteKey": "6Lcg7CMUAAAAANphynKgn9YAgA4tQ2KI_iqRyTwd"
      },
      "id": "1e5f8a20-3b42-4f11-9a7c-capmonster01",
      "name": "CapMonster Cloud",
      "type": "@zennolab_com/n8n-nodes-capmonstercloud.capMonsterCloud",
      "typeVersion": 1,
      "position":,[300][460]
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

### UI Setup Reference

#### 1. Selecting CAPTCHA Protection Type
![Select CAPTCHA Type](images/selectCaptcha1.png)

#### 2. Configuring API Key Credentials
![API Key Setup](images/keyNode.png)

---

## 🔄 Migrating from 2Captcha or Capsolver

Already solve captchas in your n8n workflows with 2Captcha or Capsolver? Replace only the solver step and keep the rest of your workflow unchanged. CapMonster Cloud follows the same flow: send the website URL and sitekey, receive the token.

### Migration from the 2Captcha API (HTTP Request node)

If your workflow calls the 2Captcha API with an HTTP Request node, delete that step (and any wait or polling loop you built around it) and add the **CapMonster Cloud** node instead. Set the task type, `websiteURL` and `websiteKey`, then map the token from the node output to your next step.

### Migration from the Capsolver node or API

If your workflow uses the Capsolver node or calls the Capsolver API with an HTTP Request node, replace that step with the **CapMonster Cloud** node. CapMonster Cloud uses the same `createTask` / `getTaskResult` flow, so the inputs are the same: task type, `websiteURL` and `websiteKey`.

### After: CapMonster Cloud

Add the **CapMonster Cloud** node (see the Quick Start workflow above) and pass its output to the step that submits the form: `gRecaptchaResponse` for reCAPTCHA, `token` for Cloudflare Turnstile.

Only the solver step and the credentials change: the token is used exactly as before, so the rest of your workflow stays the same.

### Keep existing 2Captcha-based software

Software that already speaks the 2Captcha API can work with CapMonster Cloud without code changes. See the [guide for connecting other services' APIs](https://docs.capmonster.cloud/docs/external-services/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

---

## 🛡️ Supported CAPTCHA Types: Bypass reCAPTCHA, Cloudflare Turnstile, GeeTest and More

Use this n8n captcha solver for captcha bypass in web scraping and workflow automation: reCAPTCHA bypass (v2, v2 Enterprise, v3), Cloudflare Turnstile solver, DataDome solver, GeeTest solver, Amazon WAF bypass, FunCaptcha solving and image-to-text recognition.

All task types follow the official [CapMonster Cloud API documentation](https://docs.capmonster.cloud/docs/captchas/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read):

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

## 🛠️ How It Works

```text
[ Trigger: Webhook / Schedule ]
              │
              ▼
    [ HTTP Request: Target Page ] ──► Extracts sitekey & pageURL
              │
              ▼
  [ 🤖 CapMonster Cloud Node ] ──► Sends task & polls the solution until it is ready
              │
              ▼
[ HTTP Request: Submit Form ] ──► Injects gRecaptchaResponse / Turnstile token
```

The node automatically handles polling, backoff retries, and token delivery directly into JSON output parameters (`gRecaptchaResponse`, `token`, etc.).

---

## ⚙️ Best Practices

- **Use tokens promptly:** CAPTCHA tokens expire quickly (a reCAPTCHA v2 token is valid for 60 seconds after solving), so make sure your next HTTP Request executes immediately after the CapMonster node.
- **Keep session context consistent:** For Cloudflare Turnstile or DataDome, use residential proxies with the same IP/subnet that makes the initial page request.
- **Use the right task type:** If using custom JSON payloads, follow the official [CapMonster Task API Reference](https://docs.capmonster.cloud/docs/captchas/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).
- **Monitor your balance:** Make sure your dashboard balance is positive. Grab free testing credits from your [Dashboard](https://dash.capmonster.cloud/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

---

## 💡 Use Cases

- **Web scraping and data collection** from websites you are authorized to access, without manual captcha solving.
- **Workflow automation:** solve a captcha inside a scheduled or webhook-triggered n8n workflow and submit the form with the returned token.
- **Automated testing (QA)** of your own website and its captcha-protected forms.
- **No-code backend flows** that need a captcha solving API inside n8n.

---

## ❓ FAQ

**Is CapMonster Cloud a 2Captcha alternative for n8n?**
Yes. It is a captcha solving service with an official n8n node. For reCAPTCHA v3 it starts at $0.90 per 1,000 solves versus $1.45 at 2Captcha, which is up to 38% cheaper. For Cloudflare Turnstile it starts at $1.30 versus $1.45, which is 10% cheaper.

**Is CapMonster Cloud a Capsolver alternative for n8n?**
Yes. For reCAPTCHA v3 it is 10% cheaper than Capsolver ($0.90 versus $1.00 per 1,000 solves) and shows an API response time of ≤ 2 s versus < 3 s. See the comparison table above and its disclaimer.

**How do I migrate from 2Captcha or Capsolver to CapMonster Cloud in n8n?**
Install the community node, create the CapMonster Cloud credentials and replace your solver step with the CapMonster Cloud node. See the migration section above. Software that already supports the 2Captcha API can also be connected through the [CapMonster Cloud guide](https://docs.capmonster.cloud/docs/external-services/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

**Is there an official n8n captcha solver from CapMonster Cloud?**
Yes. This repository is the official n8n community node for the CapMonster Cloud captcha solving service.

**How do I bypass reCAPTCHA v2 in n8n?**
Add the CapMonster Cloud node, choose the reCAPTCHA v2 task type, set `websiteURL` and `websiteKey`, and use the returned `gRecaptchaResponse` in the next step. See the [reCAPTCHA v2 documentation](https://docs.capmonster.cloud/docs/captchas/no-captcha-task/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

**How do I bypass Cloudflare Turnstile in n8n?**
Choose the Cloudflare Turnstile task type in the node, set `websiteURL` and `websiteKey`, and use the returned `token`. According to the [Turnstile documentation](https://docs.capmonster.cloud/docs/captchas/turnstile-task/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read), all Turnstile subtypes are supported automatically: manual, non-interactive and invisible.

**Which captcha types does the n8n node solve?**
reCAPTCHA v2, v2 Enterprise, v3 and v3 Enterprise, Cloudflare Turnstile, GeeTest, FunCaptcha, DataDome, Imperva, Amazon WAF, Binance, TenDI, Castle, TSPD, image-to-text and complex image tasks. See the supported types table above and the [Supported Captchas Overview](https://docs.capmonster.cloud/docs/captchas/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

**How do I get an API key?**
Register on CapMonster Cloud, top up your balance and copy your API key. The [Getting Started Guide](https://docs.capmonster.cloud/docs/getting-start/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read) describes each step.

**Does the node work on n8n Cloud?**
Unverified community nodes are available only on self-hosted n8n instances, so install this node on a self-hosted instance (Docker or npm).

**How fast are captchas solved?**
On average between 1 and 30 seconds, depending on the captcha type. More details are in the [CapMonster Cloud FAQ](https://docs.capmonster.cloud/docs/faq/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

**How long is a reCAPTCHA v2 solution valid?**
According to the [reCAPTCHA v2 documentation](https://docs.capmonster.cloud/docs/captchas/no-captcha-task/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read), the returned token is valid for 60 seconds after the captcha is solved, so use it right away.

**Where is the full API reference?**
See the [API Methods Reference](https://docs.capmonster.cloud/docs/methods/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

---

## ⚖️ Responsible Use

CapMonster Cloud is intended for legitimate business purposes only, such as testing your own website or a website you are authorized to test, and recognizing images you provide. Read more about [ethical and transparent captcha automation](https://capmonster.cloud/en/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read).

---

## 📚 Documentation & Support

- 📖 [Getting Started Guide](https://docs.capmonster.cloud/docs/getting-start/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)
- 🎯 [Supported Captchas Overview](https://docs.capmonster.cloud/docs/captchas/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)
- ⚙️ [API Methods Reference](https://docs.capmonster.cloud/docs/methods/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)
- ❓ [CapMonster Cloud FAQ](https://docs.capmonster.cloud/docs/faq/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)
- 🌐 [Browser Extension Guides](https://docs.capmonster.cloud/docs/extension/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)
- 🧩 [n8n Community Nodes Directory](https://docs.n8n.io/integrations/community-nodes/)
- 💬 [Support & Community](https://capmonster.cloud/en/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read#support)

## Other official SDKs & integrations

- [Python](https://github.com/CapMonsterCloud/capmonster-python-captcha-solver)
- [Node.js](https://github.com/CapMonsterCloud/capmonster-nodejs-captcha-solver)
- [.NET](https://github.com/CapMonsterCloud/capmonster-dotnet-captcha-solver)
- [Go](https://github.com/CapMonsterCloud/capmonster-go-captcha-solver)
- [PHP](https://github.com/CapMonsterCloud/capmonster-php-captcha-solver)
- [Rust](https://github.com/CapMonsterCloud/capmonster-rust-captcha-solver)
- [MCP server](https://github.com/CapMonsterCloud/capmonster-mcp-captcha-solver)
- [MCP server for Patchright](https://github.com/CapMonsterCloud/capmonster-mcp-patchright-captcha-solver)
- [API Docs](https://github.com/CapMonsterCloud/capmonster-captcha-solver-docs)

---

## 📄 License

[MIT](./LICENSE) © [CapMonster Cloud](https://capmonster.cloud/en/?utm_source=github&utm_medium=referral&utm_campaign=n8n_repo_read)
