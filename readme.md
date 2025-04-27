
# 🚀 Databricks Data Intelligence Platform for UberEats

[![Terraform](https://img.shields.io/badge/Terraform-1.2+-5C4EE5?logo=terraform&logoColor=white)](https://www.terraform.io/)  
[![Azure](https://img.shields.io/badge/Azure-Cloud-blue?logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)  
[![Databricks](https://img.shields.io/badge/Databricks-%23007E8E?logo=databricks&logoColor=white)](https://databricks.com/)

This repository contains Terraform code to deploy a **Databricks Data Intelligence Platform** on Microsoft Azure, supporting UberEats' data processing and machine learning use case. The platform utilizes modern **Medallion Architecture** for real-time data processing, machine learning, and **generative AI** capabilities.

## Key Features ✨
- **Azure Databricks Workspaces** for dev and prod environments  
- **Medallion Architecture**: Bronze, Silver, and Gold layers  
- Real-time **Data Processing** and **Machine Learning**  
- **Unity Catalog** for centralized data governance  
- **MLOps** infrastructure for model deployment and management  
- Security via **RBAC** and **network isolation**  
- **Monitoring** for operational visibility and alerting  

## 🚀 Quick Start

For a comprehensive step-by-step guide, check the full [deployment guide](https://github.com/danielwisouza/DatabricksWeek-DataIntelligenceForUberEats/blob/main/terraform/readme.md).


### 1. Prerequisites
Before deploying, ensure you have:
- An **Azure Subscription**
- **Terraform** (v1.2.0+)
- **Azure CLI** and **Databricks CLI** (optional)

### 2. Deployment Options
#### Option A: Using the Makefile (Recommended)
```bash
make init
make dev-deploy
make prod-deploy
```

#### Option B: Local Deployment
For local testing:
```bash
make local-dev-deploy
make local-prod-deploy
```

### 3. Key Resources
- **Databricks Workspaces**: for both development and production environments  
- **Data Lakehouse**: utilizing **Delta Lake** storage  
- **Unity Catalog**: for centralized data governance

### 4. Security & Compliance
- **RBAC** (Role-Based Access Control)  
- **Azure Key Vault** for secrets management  
- **Network Isolation** with private endpoints

---

## 📊 Architecture Overview

| Component         | Description                                                            |
|-------------------|------------------------------------------------------------------------|
| **Databricks Workspaces** | Dev and Prod environments                                            |
| **Data Lakehouse** | Delta Lake storage (Bronze, Silver, Gold layers)                       |
| **Unity Catalog**  | Centralized governance for data management                            |
| **Machine Learning** | Infrastructure for model training and deployment                       |
| **MLOps**           | Model management and CI/CD pipelines                                  |
| **Security**       | RBAC, Network Isolation, Key Vault                                    |
| **Monitoring**     | Azure Monitor integration and custom alerts for operational insights |

## 📚 Further Reading
- [Deployment Guide](https://github.com/danielwisouza/DatabricksWeek-DataIntelligenceForUberEats/blob/main/terraform/readme.md)
- [Databricks Documentation](https://docs.databricks.com/)

## License 📄
MIT License – see the [LICENSE] file for details.

---

### ⚡️ Customize Your Deployment

You can adjust various parameters for different environments in the `variables.tf` file.

**Resource Sizing Example**:
```hcl
env_config = {
  dev = {
    node_type = "Standard_DS3_v2"
    min_workers = 2
    max_workers = 8
  }
}
```

---

### 🔧 Contributing
Feel free to fork this repo and submit Pull Requests!

---
