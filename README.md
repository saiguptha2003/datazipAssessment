# DevOps Assessment: Clickhouse and Superset Deployment on Minikube

## Overview

This repository contains Kubernetes configurations to deploy Clickhouse and Superset on Minikube. Clickhouse serves as an open-source data warehouse, while Superset is utilized for business intelligence purposes, enabling visualization and analysis of data stored in Clickhouse.

## Prerequisites

Before getting started, ensure you have the following installed:

- **Minikube**: Local Kubernetes cluster management tool.
- **kubectl**: Kubernetes command-line tool for interacting with clusters.
- **Docker**: Containerization platform knowledge for building and managing images.

## Components

### Clickhouse Deployment

- **Description**: StatefulSet deployment for Clickhouse with persistent storage of 10GB.
- **Image**: Uses `yandex/clickhouse-server:latest`.
- **Ports**: Exposes port 9000 for native Clickhouse communication.

### Superset Deployment

- **Description**: Deployment of Superset, a BI tool for creating reports and visualizations.
- **Image**: Uses `apache/superset:latest`.
- **Ports**: Exposes port 8088 for accessing the Superset UI.

## Deployment Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/saiguptha2003/datazipAssessment.git
   cd datazipAssessment


2. **Deploy ClickHouse and apache superset**:
     ```bash
     kubectl apply -f clickhouse.yaml
     kubectl apply -f superset.yaml
    ```
3. **Accessing Superset:**:
   ```bash
   kubectl describe service superset | grep NodePort
```
connecting Clickhouse to Superset:

    In Superset UI, navigate to Data > Databases.
    Add a new database connection for Clickhouse using the provided connection string.
Notes

    Ensure Docker is running and accessible to Minikube for pulling images.
    Adjust YAML configurations for production deployments as necessary.

Contact Information

For any questions or assistance, please contact:

    Name: V D Panduranga Sai Guptha
    Email: saiguptha_v@srmap.edu.in
    GitHub: saiguptha2003
    LinkedIn: saiguptha2003
