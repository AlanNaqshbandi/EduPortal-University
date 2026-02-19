# EduPortal University – Secure Azure Production Architecture

Secure, private, production-grade Azure architecture for an e-learning platform, implementing network segmentation, Private Endpoints, Managed Identity, RBAC, and centralized monitoring.

**Architecture Pattern**: Public frontend with fully private backend services using Private Link and RBAC-controlled access.

**Architecture Overview**

The environment follows a secure layered architecture:

- Public-facing App Service.
- Private backend services (SQL, Storage, Key Vault).
- Network segmentation via VNet and subnets.
- Private Endpoints for data services.
- Centralized monitoring via Log Analytics.
- RBAC and Managed Identity for secure access.

**Security by Design Principles**

- No public access to data services.
- Least privilege RBAC model.
- Managed Identity instead of stored credentials.
- Private DNS for internal resolution.
- Centralized logging and alerting.

***Phase 0 – Resource Organization***
1. Created dedicated Resource Groups for Network, App, Data, Security, and Operations.
2. Applied consistent naming standards and tags.
3. Established clean resource separation.

***Phase 1 – Identity & RBAC***
1. Created Microsoft Entra ID security groups.
2. Implemented Role-Based Access Control (RBAC) at Resource Group scope.
3. Enforced group-based access (no direct user permissions).
4. Enabled MFA for privileged roles.

***Phase 2 – Network Segmentation & Private Connectivity***
1. Deployed Virtual Network with segmented subnets.
2. Configured Private DNS zones.
3. Established network boundary for private services.

***Phase 3 – Application Deployment***
1. Deployed Azure App Service (production tier).
2. Enabled Managed Identity.
3. Integrated Web App with Virtual Network.

***Phase 4 – Private SQL Deployment (No Public Exposure)***
1. Deployed Azure SQL Database.
2. Disabled public network access.
3. Configured Private Endpoint for secure connectivity.

***Phase 5 – Secure Storage Deployment***
1. Deployed Azure Storage Account.
2. Disabled public access.
3. Configured Private Endpoint.
4. Enabled soft delete and versioning.

***Phase 6 – Secrets Protection***
1. Deployed Azure Key Vault.
2. Disabled public access.
3. Integrated with Managed Identity.
4. Stored sensitive configuration securely.

***Phase 7 – Monitoring & Alerts***
1. Deployed Log Analytics workspace.
2. Enabled diagnostic settings for all services streaming to a centralized Log Analytics workspace.
3. Configured alert rules for availability and performance.

***Phase 8 – Production Validation***
1. Verified private connectivity across services.
2. Confirmed no public exposure of data services.
3. Validated logging and alert functionality.
4. Reviewed RBAC and security posture.

**Operational Impact**:

This deployment achieves:

- Zero public exposure of backend services.
- Identity-based service-to-service authentication.
- Centralized monitoring and alerting.
- Production-ready governance structure.
--------------------------------------------------------------------------------------
🏗️ Deployment Specifications
| Component          | Configuration                        |
| ------------------ | ------------------------------------ |
| Region             | Canada Central                       |
| Environment        | Production                           |
| Architecture Model | Hub-Spoke (Single VNet segmented)    |
| Network Model      | Private Endpoints + Private DNS      |
| Identity Model     | Entra ID + Managed Identity          |
| Monitoring         | Log Analytics + Azure Monitor Alerts |
| Access Control     | RBAC (Group-Based)                   |
