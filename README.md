# 🤖 n8n LINE Webhook Starter

![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)
![Status](https://img.shields.io/badge/status-pre--release-yellow.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A minimal, ready-to-import **n8n workflow template** designed to quickly set up a webhook listener and automated text response for the **LINE Messaging API**.

Built by [WisdomFirm](https://github.com/WisdomFirm) for developers needing a serverless solution for basic chatbot interactions.

---

## ⚠️ Development Notice (v0.1.0)
This template is released as a **pre-release** version (`v0.1.0`). It is intended for educational and testing purposes to demonstrate webhook logic.

---

## 🚀 Workflow Logic

This template automates the following pipeline:

1.  **Webhook Trigger:** Listens for incoming `POST` requests from the LINE Messaging API.
2.  **JSON Parser (Function Node):** Processes the complex JSON payload to extract:
    * `replyToken`: Required to send a response.
    * `text`: The actual message sent by the user.
3.  **LINE Response:** Uses the `replyToken` to send a customized text reply back to the user instantly.

---

## 📂 Repository Content

```text
n8n-line-webhook-starter/
├── n8n_workflow.json   # The core workflow file (Import this to n8n)
├── README.md           # Documentation
└── LICENSE             # MIT License
```
## 🛠️ Setup Guide

### 1. Prerequisites
* An active **n8n instance** (Self-hosted or n8n Cloud).
* A **LINE Official Account** (LINE OA) with Messaging API enabled.
* Your **Channel Access Token** and **Channel Secret** (from LINE Developers Console).

### 2. Import Workflow
1.  Download the `n8n_workflow.json` file from this repository.
2.  Open your n8n workspace.
3.  Go to the **Workflows** page -> Click **"Add workflow"**.
4.  Click the **three dots (...)** menu -> **"Import from File"** -> Select `n8n_workflow.json`.

### 3. Configure Credentials
1.  Double-click the **LINE** node in the editor.
2.  Under **Credential to connect with**, select **Create New Credential**.
3.  Paste your **Channel Access Token** and **Channel Secret**.
4.  Save the credential.

### 4. Activate Webhook
1.  Double-click the **Webhook** node.
2.  Copy the **Production URL** (or Test URL if developing locally).
3.  Go to the **LINE Developers Console** -> Messaging API tab.
4.  Paste the URL into the **Webhook URL** field and enable **"Use webhook"**.
5.  **Toggle the Workflow to "Active"** (Top right switch in n8n).
### 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

## License
This project is licensed under the MIT License.
