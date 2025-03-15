# ApexLOS Infrastructure

This repository contains the Infrastructure as Code (IaC) for the ApexLOS system, a comprehensive mortgage loan origination system.

## Infrastructure Components

The infrastructure for ApexLOS consists of the following components:

1. **PostgreSQL Database** - Primary data store with logical replication for ElectricSQL
2. **ElectricSQL Sync Service** - Handles data synchronization between clients and server
3. **MinIO Document Storage** - S3-compatible storage for documents and files
4. **RabbitMQ Message Broker** - Orchestrates workflow and message passing
5. **Redis Cache** - Caching layer for improved performance
6. **Monitoring and Logging** - Infrastructure monitoring and observability

## Getting Started

This repository uses Terraform to manage infrastructure. The infrastructure is organized in modules for better maintainability and reusability.

### Prerequisites

- Terraform 1.5 or later
- AWS CLI (for AWS deployments)
- Docker and Docker Compose (for local development)

### Directory Structure

```
apexlos-infrastructure/
├── environments/            # Environment-specific configurations
│   ├── dev/                 # Development environment
│   ├── staging/             # Staging environment
│   └── prod/                # Production environment
├── modules/                 # Reusable infrastructure modules
│   ├── database/            # PostgreSQL database module
│   ├── document-storage/    # MinIO document storage module
│   ├── message-broker/      # RabbitMQ message broker module
│   ├── cache/               # Redis cache module
│   └── monitoring/          # Monitoring and logging module
├── local/                   # Local development environment using Docker Compose
└── scripts/                 # Helper scripts
```

## TO DO (Next Steps)

- [ ] Set up PostgreSQL database with logical replication
- [ ] Create database schema and migrations
- [ ] Configure ElectricSQL sync service
- [ ] Set up MinIO document storage
- [ ] Configure RabbitMQ message broker
- [ ] Set up Redis cache
- [ ] Implement infrastructure monitoring
