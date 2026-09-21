# AI-Powered Knowledge Base & RAG Automation

An n8n workflow that turns business knowledge into a searchable vector knowledge base for AI assistants and semantic search.

The workflow uses Google Gemini embeddings and Supabase Vector Store to prepare business information for retrieval-augmented generation (RAG).

## What it does

Businesses often have useful information spread across documents, FAQs, policies, product information, and internal resources.

This workflow provides a simple foundation for turning that information into an AI-ready knowledge base.

The demo workflow:

1. Starts with structured business knowledge
2. Loads the content as a document
3. Generates vector embeddings with Google Gemini
4. Stores the embedded document in Supabase Vector Store
5. Makes the information available for semantic retrieval by downstream AI workflows

## Workflow Architecture

```text
Business Knowledge
       ↓
Document Loader
       ↓
Google Gemini Embeddings
       ↓
Supabase Vector Store
       ↓
Semantic Retrieval
       ↓
AI Assistant / RAG Workflow
```

The knowledge-base workflow can be used as the ingestion layer for a larger RAG system.

## Key Capabilities

- Business knowledge ingestion
- Document loading
- Google Gemini embeddings
- Supabase vector storage
- Semantic search foundation
- RAG knowledge-base preparation
- AI-ready business information
- Integration with downstream AI agents and assistants

## Example Knowledge

The public demo uses fictional **Demo Electronics** information covering:

- Company information
- Refund policy
- Shipping
- Warranty
- Customer support
- Human escalation guidance

The example content is intentionally generic and fictional so the workflow can be shared publicly without exposing private business information.

## Business Use Cases

This type of knowledge base can support AI workflows for:

- Customer support
- Product questions
- FAQ assistants
- Refund and return policies
- Shipping questions
- Warranty information
- Internal company knowledge
- Employee support
- Service information
- AI agents that need access to business-specific context

## Tech Stack

- **n8n** for workflow automation
- **Google Gemini** for text embeddings
- **Supabase Vector Store** for storing and retrieving vectorized knowledge
- **RAG** for grounding AI workflows with business-specific information

## Repository Structure

```text
.
├── README.md
└── workflow/
    └── knowledge-base.json
```

## How to Use

### 1. Import the workflow

Import `workflow/knowledge-base.json` into your n8n instance.

### 2. Configure credentials

Connect your own:

- Google Gemini credentials
- Supabase credentials

The public workflow does not contain API keys, passwords, or private credential values.

### 3. Configure Supabase

Create or configure the vector store used by the workflow and make sure it matches the table configured in the n8n workflow.

The demo workflow uses a table named `documents`.

### 4. Replace the demo knowledge

Update the knowledge content with information from the business or project you are building for.

Examples include product documentation, FAQs, policies, SOPs, service descriptions, or internal resources.

### 5. Run the workflow

Execute the workflow to load the content, generate embeddings, and store the resulting vectors.

### 6. Connect it to a RAG workflow

The resulting vector store can then be queried from an AI agent or another n8n workflow to retrieve relevant information before generating a response.

## Security

This repository is intended for public portfolio and learning use.

The workflow has been sanitized before publication. Do not commit:

- API keys
- Access tokens
- Passwords
- Database credentials
- Webhook secrets
- Private customer information
- Confidential business documents

Use n8n's credential manager or environment variables for sensitive configuration.

## Related Project

This knowledge base can be used as the retrieval layer for an AI customer support workflow.

See the related project:

**AI Customer Support Agent with n8n, Gemini, RAG, Supabase, and Human Escalation**

## About

Built as part of my AI and workflow automation portfolio to demonstrate how business knowledge can be connected to AI workflows using n8n, embeddings, vector search, and RAG.

Portfolio: https://ojo-israel-portfolio.lovable.app

LinkedIn: https://www.linkedin.com/in/israel-ojo-514661394

GitHub: https://github.com/ojoisrael
