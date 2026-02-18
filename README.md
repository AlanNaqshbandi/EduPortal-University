# EduPortal-University
📌 Project Goal

Build a secure, production-ready Azure environment to host a university e-learning platform.

***Phase 0 – Resource Organization***
1. Created dedicated Resource Groups for Network, App, Data, Security, and Operations.
2. Applied consistent naming standards and tags.
3. Established clean resource separation.

***Phase 1 – Identity & RBAC***
1. Created Microsoft Entra ID security groups.
2. Implemented Role-Based Access Control (RBAC) at Resource Group scope.
3. Enforced group-based access (no direct user permissions).
4. Enabled MFA for privileged roles.

***Phase 2 – Networking Foundation***
1. Deployed Virtual Network with segmented subnets.
2. Configured Private DNS zones.
3. Established network boundary for private services.

***Phase 3 – Application Deployment***
1. Deployed Azure App Service (production tier).
2. Enabled Managed Identity.
3. Integrated Web App with Virtual Network.

***Phase 4 – Secure Database Deployment***
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
2. Enabled diagnostic logs for all services.
3. Configured alert rules for availability and performance.

***Phase 8 – Production Validation***
1. Verified private connectivity across services.
2. Confirmed no public exposure of data services.
3. Validated logging and alert functionality.
4. Reviewed RBAC and security posture.
--------------------------------------------------------------------------------------
PROJECT METADATA
| Item             | Value                        |
| ---------------- | ---------------------------- |
| Subscription     | Your Production Subscription |
| Region           | Canada Central               |
| Secondary Region | Canada East                  |
| Address Space    | 10.10.0.0/16                 |
| App Name Prefix  | eduportal                    |
| Environment      | prod                         |
| Naming Pattern   | `<type>-eduportal-prod`      |

