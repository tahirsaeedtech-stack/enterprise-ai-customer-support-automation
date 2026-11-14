# Enterprise AI Customer Support Automation

**AI-Powered Ticket Classification, Priority Routing & Automated Tracking**

## Project Overview

An AI-powered customer support automation prototype built with n8n and Google Gemini. The system receives customer requests through a webhook, classifies support issues, assigns priority levels, routes tickets to appropriate support queues, and records ticket information in Google Sheets.

## Live Project Demonstration

**Watch the AI Customer Support Automation in action:**

[▶ Watch the Workflow Demonstration on YouTube](https://youtu.be/4vqllY8Q-ZY)

This demonstration showcases an AI-powered customer support workflow developed using n8n Cloud, Google Gemini, Webhooks, JavaScript, and Google Sheets.

### Demonstrated Capabilities

- Automated customer support ticket intake through an API webhook
- AI-powered ticket classification and prioritization
- Conditional routing for high-priority and routine requests
- Human-review queue for urgent support tickets
- Automated ticket tracking through Google Sheets
- End-to-end workflow execution and testing

**Business Use Case:** Demonstrates how AI automation can streamline customer support ticket processing, reduce repetitive manual classification, and provide a foundation for scalable customer service operations.

**Project Status:** Functional prototype with demonstrated workflow execution. Production deployment would require additional security, monitoring, and helpdesk integration.

## Business Problem

Customer support teams spend significant time manually reviewing, categorizing, and prioritizing incoming requests.

This creates operational challenges:

- Delayed responses to urgent customer complaints
- Repetitive manual ticket classification
- Inconsistent ticket prioritization
- Limited visibility into customer support requests

## Proposed Solution

An automated workflow that:

1. Receives customer requests through an HTTP webhook.
2. Validates incoming customer messages.
3. Uses Google Gemini to classify support requests.
4. Extracts structured AI classification results.
5. Routes high-priority requests for human review.
6. Directs other requests to routine support.
7. Records ticket details in Google Sheets.
8. Uses ticket IDs to update existing records rather than blindly appending duplicates.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n Cloud | Workflow orchestration |
| Google Gemini | AI ticket classification |
| Webhooks | External application integration |
| Google Sheets | Ticket tracking prototype |
| JavaScript | JSON response parsing |
| Hoppscotch | API testing |

## Workflow Architecture

```text
Customer Request
       |
   POST Webhook
       |
  Data Preparation
       |
  Ticket Validation
       |
  Google Gemini AI
       |
  JSON Parsing
       |
  Priority Routing
       |
  +----------------------+
  |                      |
High Priority       Medium / Low
  |                      |
Human Review         Routine Queue
  |                      |
Google Sheets        Google Sheets
```

Invalid requests follow a separate validation path. AI failures are intended to be handled through the workflow's fallback and human-review mechanisms.

## Demonstrated Features

- Webhook-based customer request intake
- AI-powered support ticket classification
- Priority-based ticket routing
- Human review escalation
- Google Sheets integration
- Ticket ID-based record updates
- API testing with sample customer requests

## Testing

The prototype has been manually tested with billing complaints and routine customer support requests.

Verified scenarios include:

- High-priority billing requests routed to human review
- Routine requests routed to the routine support queue
- Customer ticket records saved to Google Sheets
- Existing ticket IDs updated without creating an additional row in the tested scenario

## Business Applications

This workflow can serve as a starting point for customer support automation in e-commerce, SaaS, online services, and other support-intensive businesses.

## Current Limitations

This is a portfolio prototype, not a production-certified enterprise system. Further work is needed for authentication, privacy safeguards, persistent logging, monitoring, comprehensive error handling, load testing, and integration with a dedicated helpdesk or CRM.

## Future Improvements

- CRM/helpdesk integrations
- SLA-based escalation
- Support performance dashboards
- Automated customer acknowledgments
- AI classification evaluation and monitoring

## Project Status

**Working prototype — portfolio documentation in progress.**

## Author

AI Automation & Agentic AI Solutions Developer
