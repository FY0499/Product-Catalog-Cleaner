# AI Product Catalog Cleaner

An n8n workflow that scans product records for missing fields or inconsistent product names, uses AI to suggest cleaned names, categories, and descriptions, and updates the matching rows in Google Sheets.

## How it works

1. A scheduled trigger retrieves product records from Google Sheets.
2. JavaScript filters records with missing category, description, or price fields, or product names containing extra whitespace.
3. A Gemini-powered AI agent proposes a cleaned product name, a suitable category, and a short description.
4. JavaScript parses the response and pairs it with the product SKU.
5. The workflow updates the matching product row in Google Sheets.

## Technologies

- n8n
- Google Sheets
- Google Gemini
- JavaScript
- AI Agent

## Setup

1. Import workflow.json into n8n.
2. Configure Google Sheets and Gemini credentials.
3. Connect your product sheet and verify that SKU, productName, category, description, and price columns exist.
4. Test on a copy of your product data first, and review the AI-generated values before using them in production.

## Notes

This repository contains the exported n8n workflow. Configure your own credentials and integrations in n8n before running it.
