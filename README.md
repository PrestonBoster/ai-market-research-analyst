# ai-market-research-analyst

AI-Powered Lead Enrichment & Scoring Engine

A multi-agent Revenue Operations workflow built in Make that automatically researches companies, enriches CRM records, prevents duplicates, and assigns AI-driven lead scores based on buying intent and company fit.

This project simulates a lightweight HubSpot + Clay + AI SDR stack using no-code automation.

Overview

This workflow ingests company submissions from a Fillout form, performs web research and website scraping, enriches company profiles, checks for existing records, and uses AI to prioritize leads based on predefined qualification criteria.

The system is designed to demonstrate modern RevOps concepts including:

Lead enrichment
CRM deduplication
AI-driven lead qualification
Multi-agent workflow orchestration
Automated data management
Features
AI Market Research Agent
Performs web searches
Scrapes company websites using Firecrawl
Extracts and structures company data
Generates company profiles automatically
CRM Deduplication
Searches existing records by company name
Prevents duplicate company creation
Updates existing records when matches are found
AI Lead Scoring Agent

Evaluates:

Industry fit
Company size
Revenue
Contact title
Buying intent
Service offerings
Growth indicators

Assigns:

Lead Score (0-100)
Lead Rating (Hot / Warm / Cold)
Buying Intent (High / Medium / Low)
AI-generated reasoning
Mock CRM

Uses Google Sheets to simulate HubSpot company records and store:

Company information
Contact details
Revenue and employee estimates
Research notes
Lead scores and ratings
Workflow Architecture
Fillout Form
    │
    ▼
Market Research Agent
 ├── AI Web Search
 └── Firecrawl Website Scraping
    │
    ▼
JSON Parsing
    │
    ▼
Search Existing Companies
    │
    ▼
Router
├────────────── Existing Company ──────────────┐
│                                              │
│      Update Existing Record                  │
│                                              │
└──────────────────────────────────────────────┤
                                               ▼
                                          Lead Scoring Agent
                                               │
                                               ▼
                                          JSON Parsing
                                               │
                                               ▼
                                        Update Score Fields
                                               ▲
┌──────────────────────────────────────────────┤
│                                              │
│           Create New Company                 │
│                                              │
└────────────── New Company ───────────────────┘
Technologies Used
Make
Make AI Agents
OpenAI GPT-4.1 Mini
Firecrawl
Google Sheets
Fillout Forms
Example Data Collected
Company Name
Domain
Industry
Employee Count
Annual Revenue
City
State
Country
Primary Contact
Job Title
Email
Phone Number
Lead Source
Website Activity
Lifecycle Stage
Lead Score
Lead Rating
AI Reasoning
Example Lead Score Output
{
  "Lead Score": 91,
  "Lead Rating": "Hot",
  "Buying Intent": "High",
  "Reason": "Strong industry fit, owner-level contact, and clear growth indicators suggest a high probability opportunity."
}
Use Cases
Revenue Operations
Sales Operations
CRM Automation
AI Lead Qualification
Company Enrichment
Pipeline Prioritization
Mock HubSpot Workflows
Portfolio Projects
Skills Demonstrated
Revenue Operations
Lead lifecycle management
Lead scoring methodologies
CRM design
Data enrichment
Deduplication workflows
Automation
Multi-agent architecture
Conditional routing
JSON parsing
API integrations
Workflow orchestration
AI Applications
AI-assisted market research
AI lead qualification
Structured data extraction
Reasoning and prioritization
Inspiration

This project was designed to emulate capabilities commonly found in:

HubSpot
Clay
Apollo
ZoomInfo
AI SDR platforms

while demonstrating how similar functionality can be built using no-code tools and AI agents.

Future Improvements
Native HubSpot integration
Email sequencing
Slack notifications
Automated task creation
AI-generated account summaries
Intent signal monitoring
QBR reporting
Dashboarding and analytics
Author

Preston Boster

AI • Revenue Operations • Sales Operations • Automation • Business Systems
