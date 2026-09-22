# Security Policy

## Scope

This repository contains a public, sanitized n8n workflow demonstrating a knowledge base and RAG ingestion pattern.

## Supported Version

The latest version on the default `main` branch is the supported version for security reports.

## Reporting a Security Issue

If you discover a security issue related to this repository, please contact me through:

https://ojo-israel-portfolio.lovable.app

Please include:

- A clear description of the issue
- Steps to reproduce it
- Potential impact
- Sanitized logs or screenshots

Do not include secrets or private data in the report.

## Credential and Secret Handling

Never commit:

- API keys
- Access tokens
- Passwords
- Supabase credentials
- Google Gemini credentials
- Webhook secrets
- Database connection strings
- Private business or customer data

Use n8n's credential manager or environment variables for sensitive values.

## Public Workflow

The workflow JSON in this repository has been sanitized for public sharing. It contains fictional demo knowledge and does not include live credentials.

## Responsible Disclosure

Please allow reasonable time to investigate and address reported issues before public disclosure of a vulnerability.
