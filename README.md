# FAQ Chatbot — n8n + Claude API

A WhatsApp FAQ chatbot for Dentacare Centre, Abu Dhabi.
Built in one day as a Week 1 project.

## What it does
- Receives messages via webhook
- Sends them to Claude API with a dental clinic system prompt
- Logs every conversation to Google Sheets (timestamp, sender, question, answer)
- Returns Claude's answer as the webhook response

## Tech Stack
- n8n (workflow automation)
- Claude API (claude-sonnet-4-20250514)
- Google Sheets (conversation logging)

## Flow
Webhook → HTTP Request (Claude API) → Google Sheets → Respond to Webhook

## Setup
1. Import `FAQ Chatbot.json` into n8n
2. Add your Anthropic API key in the HTTP Request node headers
3. Connect your Google Sheets account
4. Publish the workflow and use the Production URL

## Test Results
15 questions tested covering services, hours, booking, and off-topic redirects.
All conversations logged automatically to Google Sheets.
