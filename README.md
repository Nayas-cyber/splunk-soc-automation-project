# SOC Automation Project – Splunk + n8n + LLM + Slack

## Overview
This project demonstrates a basic SOC automation workflow for detecting failed authentication attempts from Windows logs and automating alert triage using Splunk, n8n, an LLM model, and Slack.

## Architecture
Windows event logs are forwarded to Splunk using the Universal Forwarder.  
Splunk detects failed login attempts and triggers an alert.  
The alert is sent to n8n via webhook, where it is enriched and analyzed using an LLM model.  
The final alert summary is sent to Slack.

## Tools & Technologies
- Splunk Enterprise
- Splunk Universal Forwarder (Windows)
- n8n
- LLM (via OpenRouter / mistral-7b-instruct:free model)
- Slack Webhooks
- Windows Security Event Logs (Event ID 4625)

## Use Case
- Detect multiple failed login attempts
- Automate alert analysis
- Send SOC-style alert summaries to Slack

## Disclaimer
This project is built in a lab environment for learning purposes and is not intended for production use.
