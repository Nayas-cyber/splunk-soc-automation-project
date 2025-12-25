SOC Automation Project – Splunk + n8n + LLM + Slack

Overview
This project demonstrates a SOC automation workflow for detecting failed authentication attempts from Windows logs and automating initial alert triage using Splunk, n8n, an LLM model, and Slack.

Architecture
1. Windows event logs are forwarded to Splunk using the Universal Forwarder.
2. Splunk detects failed login attempts (Event ID 4625) and triggers an alert.
3. The alert is sent to n8n via webhook.
4. n8n enriches and analyzes the alert using an LLM model.
5. The final alert summary is sent to Slack.

Tools & Technologies
- Splunk Enterprise
- Splunk Universal Forwarder (Windows)
- n8n
- LLM (via OpenRouter – mistral-7b-instruct:free)
- Slack Webhooks
- Windows Security Event Logs (Event ID 4625)

Use Case
- Detect multiple failed login attempts
- Automate initial alert analysis
- Send SOC-style alert summaries to Slack

Learning Outcomes
- Understanding SOC alert workflows
- Writing basic SPL queries for authentication events
- Automating alert enrichment using n8n
- Generating SOC-style summaries using an LLM

Disclaimer
This project is built in a lab environment for learning purposes and is not intended for production use.
