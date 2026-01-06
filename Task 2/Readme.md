# ZenQuotes Multi-Container Application

## Overview
A Python application that fetches daily inspirational quotes and sends them via email to subscribed users.

## Architecture
- **App Container**: Python application that fetches quotes and sends emails
- **Database Container**: PostgreSQL 16 for storing user data and email logs
- **Network**: Custom bridge network for inter-container communication
- **Volume**: Persistent storage for database data

## Prerequisites
- Docker Desktop installed
- Docker Compose V2+

## Environment Variables
Copy `.env.example` to `.env` and configure:
- Database credentials
- SMTP settings for email delivery

## Quick Start

### Start the application
```bash
docker compose up -d
```

### View logs
```bash
docker compose logs -f
```

### Stop the application
```bash
docker compose down
```

## Verification
- Application successfully connects to database: ✅
- Quotes fetched from ZenQuotes API: ✅
- Emails delivered to active users: ✅
- Database data persists across restarts: ✅

## Ports
- App: 8000 (configurable)
- Database: 5433 (external), 5432 (internal)

## Volumes
- `postgres_data`: Persistent PostgreSQL data storage