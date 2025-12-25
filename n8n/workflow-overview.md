## n8n Workflow Overview

1. Receives alert payload from Splunk via webhook
2. Formats the alert data
3. Sends data to an LLM for SOC-style analysis
4. Generates severity assessment and recommendations
5. Sends the final alert summary to Slack

This simulates automated Tier-1 SOC alert triage.
