# Metric (Formalization)

## Baseline (Architectural) Metrics

To define this computed metric, we need the following baseline metrics extracted from the architectural graph:

| Metric | Description |
|--------|-------------|
| **N_Components** | Total number of components in the architecture |
| **N_Connectors** | Total number of connectors (communication links) |
| **N_Endpoints** | Total number of service endpoints |
| **N_AuthenticatedConnections** | Number of HTTP connections that are properly authenticated |
| **N_EncryptedConnections** | Number of HTTP connections that use encryption |
| **N_SecureEndpoints** | Number of endpoints that implement both authentication and CSRF protection |
| **N_APIs** | Total number of exposed APIs |

---

## Computed Metric: Overall Secure Communication and Endpoint Ratio (OSCER)

This metric evaluates the **overall security posture of communication channels and endpoints** by combining authentication, encryption, and secure endpoint coverage.

\[
\text{OSCER}(A) =
\frac{
\text{N\_AuthenticatedConnections} + \text{N\_EncryptedConnections} + \text{N\_SecureEndpoints}
}{
\text{N\_Connectors} + \text{N\_Endpoints} + \text{N\_APIs}
}
\]

Where:

- \( \text{N\_AuthenticatedConnections} \) = number of HTTP connections with proper authentication  
- \( \text{N\_EncryptedConnections} \) = number of HTTP connections using encryption (TLS/HTTPS)  
- \( \text{N\_SecureEndpoints} \) = number of endpoints implementing authentication **and** CSRF protection  
- \( \text{N\_Connectors} \) = total number of connectors in the architecture  
- \( \text{N\_Endpoints} \) = total number of endpoints  
- \( \text{N\_APIs} \) = total number of exposed APIs  

**Interpretation:**  

- The value of `OSCER(A)` ranges between 0 and 1.  
- Higher values indicate better coverage of secure communication and endpoint protection across the architecture.

**Security Rule:**  

\[
\text{OSCER}(A) \geq \tau_{\text{OSCER}}
\]

Where \( \tau_{\text{OSCER}} \) is a predefined threshold representing the minimum acceptable security posture.
