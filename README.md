# AI Product Catalog Cleaner

I built this n8n workflow to review product records, identify missing or inconsistent information, and use AI to suggest cleaner product names, categories, and descriptions.

<img width="627" height="215" alt="image" src="https://github.com/user-attachments/assets/48ceaf6b-ef75-4aa0-a0a9-d8c8f9765734" />

## How it works

1. The workflow reads product records from Google Sheets on a schedule.
2. JavaScript filters products with missing category, description, or price information, as well as product names with extra spaces or inconsistent formatting.
3. Google Gemini reviews each selected product and suggests a cleaned name, a suitable category, and a short description.
4. JavaScript processes the AI response and keeps the product SKU to identify the matching record.
5. The workflow updates the corresponding product row in Google Sheets.

## Main features

- Scheduled product catalog review.
- Detection of missing product information.
- Product name cleanup.
- AI-suggested categories and descriptions.
- Google Sheets updates matched by SKU.

## Technologies

n8n, Google Sheets, Google Gemini, JavaScript, and AI Agent.

## Setup

Import [workflow.json](./workflow.json) into n8n, configure your Google Sheets and Gemini credentials, then connect your product sheet and make sure it includes SKU, productName, category, description, and price columns. Test it on a copy of your data before using it on your main catalog.
