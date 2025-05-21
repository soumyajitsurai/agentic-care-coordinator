# Agentic-Care-Coordinator
Agentic Care Coordinator - Simple Agent Network
-------------------------------------------------------------------------------------
## Requirement Description: Agentic Care Coordinator
Project Title:
Agentic Care Coordinator AI-powered Clinical Workflow Assistant

## Overview:
The Agentic Care Coordinator is an AI-driven assistant designed to streamline the care coordination process across fragmented healthcare systems. It autonomously integrates patient data from multiple sources, identifies care gaps, and generates actionable messages for healthcare providers and patients using natural language capabilities powered by OpenAI’s GPT.

## Goals and Objectives:
*  Automate the aggregation and summarization of multi-source patient health data.
*  Use a generative AI agent to identify care coordination issues such as overdue tests, unmanaged chronic conditions, and follow-up gaps.
*  Generate professional, contextual messages for providers and simplified, patient-friendly messages for recipients.
*  Reduce administrative burden and enhance decision-making through agentic intelligence.

## Functional Requirements:
1. Data Aggregation Module • Inputs: • Electronic Health Record (EHR): diagnoses, medications, last visit • Lab results: test names, values (e.g., HbA1c), dates • Pharmacy: current prescriptions, refill status • Patient self-reported data: symptoms, appointment history • Output: Unified patient record in structured dictionary format.

2. Summary Generator • Converts structured patient record into a readable summary using predefined templates. • Example: “Patient diagnosed with Type 2 Diabetes is on Metformin. Latest HbA1c: 9.1. Reports symptoms of fatigue. No upcoming appointments scheduled.”

3. GPT Agent Layer • Integrates OpenAI GPT-4 API to: • Detect care gaps • Draft provider communication • Generate empathetic patient messages • Messages are context-aware, role-specific, and generated through structured prompts.

4. Care Gap Detection • Identify: • Lack of scheduled appointments • High lab values (e.g., elevated HbA1c) • No active prescriptions or exhausted refills

5. Communication Generator • Provider Messaging: • Formal tone • Medical risk framing • Action recommendations • Patient Messaging: • Layman-friendly • Encouraging tone • Clear instructions

## Non-Functional Requirements:
*  Performance - API calls to GPT should respond within 2–5 seconds per request
*  Security - Must not log or expose any PHI; use masked/demo data during dev
*  Scalability - Modular agent architecture to support adding more roles (e.g., triage, scheduling)
*  Availability -99.9% uptime (if deployed in production with a web UI or API)
*  Compliance (Optional) - HIPAA-compliant backend for production deployment

## User Roles:
*  Healthcare Provider - Review provider alerts/messages, act on recommendations
*  Patient - Receive simplified instructions, schedule follow-ups
*  Admin/Analyst - Monitor system performance, update GPT prompt templates

##  Integration Points:
OpenAI GPT-4 API
Optional: EHR or FHIR-compliant systems (for real-time data ingestion)
Calendar/Scheduling APIs (e.g., Google Calendar, Outlook)


## Process flow diagram
![Agent Diagram](https://github.com/soumyajitsurai/agentic-care-coordinator/blob/main/agentic%20care%20coordinator%20image.png)

### Note: to run the code in Google Colab - Create Secret with OPENAI_API_KEY
