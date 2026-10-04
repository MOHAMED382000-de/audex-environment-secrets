# Audex - Week 3: Environment Variables & Secret Handling

## Overview
This repository contains the environment configuration, secret handling policies, and environment matrix for the Audex project.

## Protected Data & Security Rules
1. Compass mode operates on isolated mock data to prevent production database exposure.
2. Personally Identifiable Information (PII) is masked using `MASK_PII_DATA=true`.
3. Secret values are injected through environment files and are ignored in version control.

## Execution Steps

1. Create the local development environment file:
```bash
cp .env.example .env.dev