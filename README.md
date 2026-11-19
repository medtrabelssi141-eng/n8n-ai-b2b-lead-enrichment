# n8n-ai-b2b-lead-enrichment
# 🚀 AI-Powered B2B Lead Enrichment & Outreach Pipeline

An end-to-end automated workflow built with **n8n** and **Google Gemini** that extracts contact details from company websites, summarizes their business offerings, and generates tailored B2B cold emails directly inside **Google Sheets**.

## 🛠️ Tech Stack
* **Orchestration:** n8n
* **AI / LLM:** Google Gemini Chat Model + Structured Output Parser
* **Data Extraction & Cleaning:** HTTP Request & Custom JavaScript (Regex & HTML parsing)
* **Database / CRM:** Google Sheets

## ⚙️ How It Works
1. **Trigger & Fetch:** Reads company names and website URLs from a Google Sheet.
2. **Web Scraping:** Fetches raw HTML content for each website via HTTP Request (with error-handling fallback).
3. **Data Cleaning & Regex:** A custom JavaScript node strips `<script>`/`<style>` tags, extracts valid email addresses using Regex (filtering out image assets), and trims clean text.
4. **AI Personalization:** Google Gemini analyzes the website copy and outputs a structured JSON containing a 1-sentence company summary and a hyper-personalized cold email (<70 words).
5. **Auto-Sync:** Updates the corresponding row in Google Sheets with the extracted email, summary, and ready-to-send email copy.

## 🚀 Setup
1. Download `My workflow.json`.
2. Import it into your n8n instance (`Workflows` -> `Import from File`).
3. Connect your **Google Sheets OAuth2** and **Google Gemini API** credentials.
4. <img width="1807" height="806" alt="image" src="https://github.com/user-attachments/assets/190623b7-f58b-1e0-bdd6-a4acda36a3df" />

