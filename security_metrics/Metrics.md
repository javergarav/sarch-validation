# Metric

## 1. Baseline (Architectural) Metrics

The following baseline metrics are extracted from the architectural graph and serve as inputs for the computed metric:

- **N_AuthenticatedConnections** = Number of HTTP connections with proper authentication  
- **N_EncryptedConnections** = Number of HTTP connections using encryption (TLS/HTTPS)  
- **N_SecureEndpoints** = Number of endpoints implementing both authentication and CSRF protection  
- **N_Connectors** = Total number of connectors in the architecture  
- **N_Endpoints** = Total number of endpoints  
- **N_APIs** = Total number of exposed APIs  

These metrics capture both **logical and deployment aspects** of the architecture, providing the structural context for security evaluation.

---

## 2. Computed (Security) Metric:

### Overall Secure Communication and Endpoint Ratio (OSCER)

This metric evaluates the **overall security posture of communication channels and endpoints** by combining authentication, encryption, and secure endpoint coverage.

**Formula:**

OSCER(A) = (N_AuthenticatedConnections + N_EncryptedConnections + N_SecureEndpoints)
/ (N_Connectors + N_Endpoints + N_APIs)


Where:

- `N_AuthenticatedConnections` = Number of authenticated HTTP connections  
- `N_EncryptedConnections` = Number of encrypted HTTP connections  
- `N_SecureEndpoints` = Number of endpoints with authentication and CSRF protection  
- `N_Connectors` = Total connectors  
- `N_Endpoints` = Total endpoints  
- `N_APIs` = Total exposed APIs  

---

## 3. Interpretation

- The value of `OSCER(A)` ranges from **0 to 1**.  
- Higher values indicate **better coverage of secure communication channels and endpoint protection**.  
- It provides a **single quantitative indicator** combining multiple security aspects of the architecture.  

---

## 4. Security Rule

A predefined threshold `tau_OSCER` is established to determine compliance:

OSCER(A) >= tau_OSCER

- If `OSCER(A)` meets or exceeds `tau_OSCER`, the architecture is considered compliant with the security policy.  
- If `OSCER(A)` is below the threshold, it indicates **potential weaknesses** in authentication, encryption, or endpoint security, which should be further investigated.


## 5. Usage in Architectural Checking

- Baseline metrics are extracted from the architectural graph (Neo4j).  
- The computed metric `OSCER` is calculated using the formula above.  
- Violations of the threshold (`OSCER < tau_OSCER`) trigger **instantiation of weaknesses** in the knowledge graph, linking them to relevant CWE entries or security rules.
