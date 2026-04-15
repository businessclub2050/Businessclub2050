# 🏠 Home Lab Configuration

## Overview

This document describes Gerald January's home lab setup — a personal infrastructure for AI development, data engineering experimentation, and systems architecture prototyping.

---

## 🖥️ Core Components

### Hardware Infrastructure

- **Primary Workstation**: High-performance CPU-optimized system for LLM inference
- **Portable AI Nodes**: Flash drive-based deployments for distributed testing
- **Network Storage**: Centralized data repository for ETL testing and model artifacts

### Software Stack

#### AI & Machine Learning
- **Janus AI Node**: Local LLM deployment using Llama.cpp
  - Optimized for CPU inference
  - Tuned models for offline operation
  - Portable deployment via flash drive toolkit

- **Flash Deploy Kit**: Modular system for repeatable AI/OS setups
  - Automated provisioning scripts
  - Version-controlled configurations
  - Quick deployment for testing environments

#### Data Engineering
- **Database Systems**:
  - SQL Server (development instances)
  - Oracle Database (test environments)
  - MySQL (lightweight projects)
  - PostgreSQL (analytics workloads)

- **ETL Tools**:
  - SAS DI Studio workflows
  - Python-based data pipelines
  - Custom connectors for healthcare data formats

- **Analytics & Visualization**:
  - SAS Visual Analytics
  - Custom reporting dashboards
  - Compliance monitoring tools

#### Development Tools
- **Version Control**: Git/GitHub for all projects
- **Containerization**: Docker for isolated environments
- **Orchestration**: Scripts for automated deployment
- **Monitoring**: System metrics and performance tracking

---

## 🎯 Use Cases

### 1. AI Model Development & Testing
- Fine-tuning LLMs locally without cloud dependency
- Testing portable AI deployments
- Benchmarking CPU inference performance

### 2. Data Pipeline Prototyping
- Validating ETL workflows before production deployment
- Testing multi-source data integration
- Healthcare data format validation

### 3. Systems Architecture Experimentation
- Testing distributed system designs
- Network configuration validation
- Security posture assessment

### 4. Learning & Certification
- Hands-on cybersecurity practice (Google Cybersecurity Certification)
- Threat modeling exercises
- Data integrity testing scenarios

---

## 📁 Related Projects

| Project | Home Lab Role |
|--------|---------------|
| `janus-ai-node` | Primary LLM inference node |
| `flash-deploy-kit` | Deployment automation framework |
| `datawarehouse-optimizer` | ETL workflow testing environment |
| `data-pipelines` | Multi-database integration testing |
| `tradingview-auto-feed` | Financial data backtesting sandbox |

---

## 🔐 Security & Best Practices

- **Isolated Networks**: Separate VLANs for testing vs. production-like environments
- **Data Sanitization**: No PHI or sensitive data in test databases
- **Regular Backups**: Automated snapshots of configurations and critical data
- **Access Controls**: Principle of least privilege across all systems
- **Monitoring**: Continuous logging and alerting for anomalies

---

## 🚀 Getting Started

### Prerequisites
- Linux-based OS (Ubuntu/Debian preferred)
- Minimum 16GB RAM for AI workloads
- SSD storage for database performance
- Network connectivity for updates and package management

### Quick Setup
1. Clone the `flash-deploy-kit` repository
2. Run the provisioning script for your target environment
3. Follow role-specific setup guides in each project repository
4. Validate deployment with included test suites

---

## 📝 Documentation

Additional documentation for specific components:
- [Janus AI Node Setup](./docs/janus-setup.md) _(coming soon)_
- [ETL Pipeline Configuration](./docs/etl-config.md) _(coming soon)_
- [Database Environment Guide](./docs/database-setup.md) _(coming soon)_
- [Security Hardening Checklist](./docs/security.md) _(coming soon)_

---

## 🔄 Maintenance Schedule

- **Weekly**: System updates and security patches
- **Monthly**: Performance benchmarking and optimization
- **Quarterly**: Full backup verification and disaster recovery testing
- **Annually**: Hardware refresh evaluation and capacity planning

---

_Last Updated: 2026-04-15_
