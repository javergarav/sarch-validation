## 1. Baseline (Architectural) Metrics

Baseline metrics capture **structural properties** of the architecture. These metrics are extracted directly from the architectural graph and describe the configuration of components, connectors, and deployments.

| Metric | Description | Formula / Computation |
|--------|-------------|----------------------|
| **N\_Components** | Total number of components in the architecture | `COUNT(Component)` |
| **N\_Connectors** | Total number of connectors (communication links) | `COUNT(Connector)` |
| **N\_Endpoints** | Total number of service endpoints | `COUNT(Endpoint)` |
| **N\_Databases** | Total number of databases in the architecture | `COUNT(Database)` |
| **N\_Deployments** | Number of deployment nodes / execution environments | `COUNT(DeploymentNode)` |
| **N\_APIs** | Total number of exposed APIs | `COUNT(API)` |

These baseline metrics provide the **raw counts and structural context** necessary for computing security metrics.

---

## 2. Computed (Security) Metrics

Computed metrics are derived from baseline metrics and **combine multiple architectural characteristics** to evaluate specific security properties. Each metric is compared against a **predefined threshold** \( \tau \) to determine compliance.

| Metric | Description | Computation | Threshold Condition |
|--------|-------------|------------|------------------|
| **UAC (Unauthenticated Connections)** | Number of HTTP connections without authentication | `UAC = COUNT(unauthenticated_connections)` | `UAC <= τ_UAC` |
| **UEC (Unencrypted Communications)** | Number of communication links without encryption | `UEC = COUNT(unencrypted_connections)` | `UEC <= τ_UEC` |
| **CSRF (CSRF Vulnerable Endpoints)** | Endpoints lacking CSRF protection | `CSRF = COUNT(csrf_vulnerable_endpoints)` | `CSRF <= τ_CSRF` |
| **MA (Missing Authentication)** | Endpoints without authentication mechanisms | `MA = COUNT(unauthenticated_endpoints)` | `MA <= τ_MA` |
| **MAC (Missing Access Control)** | Endpoints without proper authorization | `MAC = COUNT(unauthorized_endpoints)` | `MAC <= τ_MAC` |
| **SDE (Sensitive Data Exposure)** | Endpoints exposing sensitive data | `SDE = COUNT(sensitive_endpoints)` | `SDE <= τ_SDE` |
| **SQLi (SQL Injection Vulnerability)** | Databases not using parameterized queries | `SQLi = COUNT(sql_injection_vulnerable_dbs)` | `SQLi <= τ_SQLi` |
| **UPC (Unprotected Credentials)** | Databases with unprotected credentials | `UPC = COUNT(unprotected_credentials_dbs)` | `UPC <= τ_UPC` |
| **EDC (Exposed Diagnostic Components)** | Monitoring components without security | `EDC = COUNT(exposed_diagnostic_components)` | `EDC <= τ_EDC` |
| **VD (Vulnerable Dependencies)** | Dependencies with known vulnerabilities | `VD = COUNT(vulnerable_dependencies)` | `VD <= τ_VD` |
| **UEI (Unprotected Eureka Instances)** | Eureka registry instances without access control | `UEI = COUNT(unprotected_eureka_instances)` | `UEI <= τ_UEI` |
| **UIC (Unauthenticated Inter-Component Communication)** | Inter-service communication without authentication | `UIC = COUNT(unauthenticated_inter_component_connections)` | `UIC <= τ_UIC` |
| **EP (Excessive Privileges)** | Connections where components exceed required privileges | `EP = COUNT(excessive_privilege_connections)` | `EP <= τ_EP` |

---