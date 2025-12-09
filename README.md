# 🤖 n8n LINE Webhook Starter

A minimal, ready-to-import n8n workflow template to quickly set up a webhook listener and automated text response for the LINE Messaging API.

This template is perfect for developers or businesses needing a simple, serverless solution for basic LINE chatbot interactions.

## 🚀 Workflow Overview

1.  **Webhook Trigger:** Listens for incoming POST requests (messages) from the LINE server.
2.  **Function Node:** Parses the complex LINE JSON structure to extract the `replyToken` and the user's `text` message.
3.  **LINE Node:** Uses the extracted `replyToken` to send a simple, customized text reply back to the user.

## 🛠️ Setup Guide

### 1. Prerequisites
* An active n8n instance (Self-hosted or Cloud).
* A **LINE Official Account** (LINE OA) with the Messaging API enabled.
* Your **Channel Access Token** and **Secret** from the LINE Developers Console.

### 2. Import Workflow to n8n
1.  Open your n8n workspace.
2.  Go to the **Workflows** page.
3.  Click **"New"** then **"Import from File"** and upload the `n8n_workflow.json` file.
4.  Activate the workflow (Toggle ON).

### 3. Configure LINE Node
1.  In the workflow, double-click the **LINE** node.
2.  Click **"Create New Credential"** and paste your LINE **Channel Access Token** and **Channel Secret**.
3.  Ensure the operation is set to **"Reply"**.

### 4. Configure LINE Webhook
1.  Double-click the **Webhook** node and copy the generated **Webhook URL**.
2.  Go to your **LINE Developers Console** for your Messaging API channel.
3.  Paste the URL into the **Webhook URL** field and ensure **"Use webhook"** is enabled.
4.  Test the connection!

## License
This project is licensed under the MIT License.
