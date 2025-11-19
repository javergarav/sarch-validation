## Unified Architectural Security Metrics Table

| # | Name | Description | CWE | Threshold | Formula |
|---|------|-------------|-----|-----------|---------|
| 1 | Elements | Set of architectural elements present in the system. | — | — | \(E\) |
| 2 | Components | Architectural elements classified as components. | — | — | \(C = \{ c \in E \mid \text{type}(c) = \text{component} \}\) |
| 3 | Components by Type | Component elements grouped by type. | — | — | \(C(t) = \{ c \in E \mid \text{type}(c) = t \}\) |
| 4 | Connectors | Architectural elements classified as connectors. | — | — | \(K = \{ k \in E \mid \text{type}(k) = \text{connector} \}\) |
| 5 | Connectors by Type | Connector elements grouped by type. | — | — | \(K(t) = \{ k \in E \mid \text{type}(k) = t \}\) |
| 6 | Connectors by Component | Connectors associated with a component \(c\). | — | — | \(K(c) = \{ k \in K \mid \text{connected}(k,c) \}\) |
| 7 | Average Connectors per Component | Average number of connectors per component. | — | — | \(\text{CpC} = \frac{|K|}{|C|}\) |
| 8 | TLS-enabled HTTP Connections | Proportion of HTTP connectors using TLS. Detects unencrypted endpoints. | CWE-319 | < 1 | \(M_1 = \frac{|K_{\text{tls}} \cap K(HTTP)|}{|K(HTTP)|}\) |
| 9 | Authentication Between Internal Services | Proportion of internal service-to-service connectors with strong authentication. | CWE-306 | < 1 | \(M_2 = \frac{|K_{\text{int\_auth\_strong}}|}{|K_{\text{int\_total}}|}\) |
| 10 | Trusted Certificates on External Interfaces | Proportion of TLS connectors using trusted CA certificates. | CWE-295 | < 1 | \(M_3 = \frac{|K_{\text{ext\_trusted}}|}{|K_{\text{ext\_TLS}}|}\) |
| 11 | Encryption of Internal Communications | Proportion of internal connectors using encrypted protocols. | CWE-319 | < 1 | \(M_4 = \frac{|K_{\text{int\_encrypted}}|}{|K_{\text{int\_total}}|}\) |
| 12 | API Gateway Coverage | External connectors routed through API Gateway. | CWE-693 | < 1 | \(M_5 = \frac{|K_{\text{via\_gateway}}|}{|K_{\text{ext\_total}}|}\) |
| 13 | Public Exposure of Sensitive Components | Sensitive components directly connected to external interfaces. | CWE-284 | < 1 | \(M_6 = \frac{|C_{\text{sensitive\_ext\_exposed}}|}{|C_{\text{sensitive}}|}\) |
| 14 | Lack of Segregation Between Frontend and Backend | Backend components reachable directly from frontend without intermediate layers. | CWE-501 | < 1 | \(M_7 = \frac{|C_{\text{frontend\_to\_backend\_direct}}|}{|C_{\text{backend}}|}\) |
| 15 | Use of Secure Messaging Channels | Encrypted/authenticated asynchronous communication. | CWE-319 | < 1 | \(M_8 = \frac{|K_{\text{broker\_secure}}|}{|K_{\text{broker\_total}}|}\) |
| 16 | Authentication Centralization | Flows processed by a dedicated authentication service. | CWE-287 | < 1 | \(M_10 = \frac{|K_{\text{via\_auth\_service}}|}{|K_{\text{auth\_total}}|}\) |
| 17 | Databases in Private Subnets | Database components deployed in private subnets. | CWE-200 | < 1 | \(M_11 = \frac{|DB_{\text{private}}|}{|DB_{\text{total}}|}\) |
| 18 | Frontend Components in DMZ | Frontend components deployed in DMZ / edge networks. | CWE-284 | < 1 | \(M_12 = \frac{|C_{\text{frontend\_DMZ}}|}{|C_{\text{frontend}}|}\) |
| 19 | Segregation of Network Zones | Connections crossing zones protected by firewalls / security groups. | CWE-284 | < 1 | \(M_13 = \frac{|K_{\text{zone\_filtered}}|}{|K_{\text{zone\_total}}|}\) |
| 20 | Isolation of Administrative Interfaces | Admin interfaces deployed in isolated management networks. | CWE-284 | < 1 | \(M_14 = \frac{|C_{\text{admin\_isolated}}|}{|C_{\text{admin}}|}\) |
| 21 | Load Balancer Protection of Public Endpoints | Public endpoints behind a load balancer / reverse proxy. | CWE-693 | < 1 | \(M_15 = \frac{|EP_{\text{behind\_LB}}|}{|EP_{\text{public}}|}\) |
| 22 | Encryption Between Network Zones | Encrypted traffic across network zones. | CWE-319 | < 1 | \(M_16 = \frac{|K_{\text{interzone\_encrypted}}|}{|K_{\text{interzone\_total}}|}\) |
