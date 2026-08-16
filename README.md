# AI-Powered Supply Chain RFQ Email Parser

An AI-powered n8n automation that monitors supplier emails, extracts structured Request for Quotation (RFQ) information using a Groq-powered LLM, validates the extracted JSON, and automatically logs the structured data into Google Sheets.

## Demo

**Workflow:** n8n automation

**Input:** Supplier RFQ email

**Processing:** LLM-based information extraction + JSON validation

**Output:** Structured RFQ record in Google Sheets

## Architecture

Email Trigger (IMAP)
        ↓
Basic LLM Chain
        ↓
Groq Chat Model
        ↓
Parse & Validate JSON
        ↓
Google Sheets

## Features

- Automated supplier email monitoring
- AI-powered RFQ information extraction
- Structured JSON generation
- JSON validation and normalization
- Automatic Google Sheets logging
- Extracts supplier, product, quantity, pricing and delivery information
- Reduces manual RFQ data entry

## Extracted Data

The workflow extracts:

- Supplier name
- Supplier email
- Product
- Quantity
- Unit
- Delivery date
- Price
- Currency
- Notes

## Tech Stack

- n8n
- Groq
- LLM
- IMAP
- Google Sheets
- JSON

## Workflow Screenshots

### Workflow Architecture

![Workflow Architecture](screenshots/workflow-overview.png)

### Successful Execution

![Successful Execution](screenshots/execution-success.png)

### Google Sheets Output

![Google Sheets Output](screenshots/google-sheets-output.png)

## Example Input

```text
Subject: RFQ – AXC-1200 Components – 100 Units

Dear Supplier,

We are requesting a quotation for the following component:

Product: AXC-1200 Industrial Control Module
Quantity: 100 units
Required Delivery Date: 25 August 2026
Target Price: 1250 USD per unit

Please confirm product availability, delivery schedule,
and your final quotation.

Supplier: ABC Industrial Components Pvt Ltd
Supplier Email: sales@abcindustrial.com

Regards,
Procurement Team
