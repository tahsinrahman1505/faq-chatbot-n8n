# FAQ Chatbot — n8n + Claude

A WhatsApp FAQ chatbot for Dentacare Centre, Abu Dhabi.
Built with n8n and Claude API.

## What it does
Receives messages via webhook, sends them to Claude with a dental clinic system prompt, logs every conversation to Google Sheets, and returns the answer.

## Flow
Webhook → HTTP Request (Claude API) → Google Sheets → Respond to Webhook

## Screenshots
[add your screenshots here]

## Setup
1. Import `faq-chatbot-v1.json` into n8n
2. Add your Anthropic API key in the HTTP Request node
3. Connect your Google Sheets account
4. Activate the workflow
