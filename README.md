# n8n Workflow Automation

n8n workflow automation service for TravelAdvisor project.

## Setup

### Prerequisites

- Docker and Docker Compose
- Node.js (for local development)

### Running with Docker

```bash
docker-compose up -d
```

n8n will be available at: http://localhost:5678

Default credentials:
- Username: `admin`
- Password: `admin123`

### Workflows

Workflows are stored in the `workflows/` directory and are automatically loaded into n8n.

## Development

### Install Dependencies

```bash
npm install
```

### Custom Nodes

This project uses custom n8n nodes:
- `n8n-nodes-globals` - Global constants and utilities

## Configuration

Environment variables can be configured in `docker-compose.yml`:

- `N8N_BASIC_AUTH_ACTIVE` - Enable/disable basic authentication
- `N8N_BASIC_AUTH_USER` - Basic auth username
- `N8N_BASIC_AUTH_PASSWORD` - Basic auth password
- `DB_TYPE` - Database type (postgresdb)
- `DB_POSTGRESDB_*` - PostgreSQL connection settings

## Database

The service uses PostgreSQL for workflow storage. The database is automatically initialized when the container starts.

## Volumes

- `n8n_data` - Stores n8n data, workflows, and credentials
- `postgres_data` - PostgreSQL data directory

