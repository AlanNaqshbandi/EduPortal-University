# EduPortal-University
📌 Project Goal

Build a secure, production-ready Azure environment to host a university e-learning platform.


*Phase 1 – Identity & RBAC*

Created Microsoft Entra ID security groups.

Implemented Role-Based Access Control (RBAC) at Resource Group scope.

Enforced group-based access (no direct user permissions).

Enabled MFA for privileged roles.

*Phase 2 – Networking Foundation*

Deployed Virtual Network with segmented subnets.

Configured Private DNS zones.

Established network boundary for private services.

*Phase 3 – Application Deployment*

Deployed Azure App Service (production tier).

Enabled Managed Identity.

Integrated Web App with Virtual Network.

*Phase 4 – Secure Database Deployment*

Deployed Azure SQL Database.

Disabled public network access.

Configured Private Endpoint for secure connectivity.

*Phase 5 – Secure Storage Deployment*

Deployed Azure Storage Account.

Disabled public access.

Configured Private Endpoint.

Enabled soft delete and versioning.

*Phase 6 – Secrets Protection*

Deployed Azure Key Vault.

Disabled public access.

Integrated with Managed Identity.

Stored sensitive configuration securely.

*Phase 7 – Monitoring & Alerts*

Deployed Log Analytics workspace.

Enabled diagnostic logs for all services.

Configured alert rules for availability and performance.

*Phase 8 – Production Validation*

Verified private connectivity across services.

Confirmed no public exposure of data services.

Validated logging and alert functionality.

Reviewed RBAC and security posture.
