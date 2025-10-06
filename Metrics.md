# Metrics

## 1. Authentication Architecture

**Metric: Secure Authentication Mechanism Ratio (SAMR)**

Measures the proportion of authentication mechanisms that comply with secure design principles.

\[
\text{SAMR}(A) = \frac{\text{N\_SecureAuth}(A)}{\text{N\_Auth}(A)}
\]

- **N_SecureAuth(A)**: Number of authentication mechanisms in architecture \(A\) that comply with secure standards.
- **N_Auth(A)**: Total number of authentication mechanisms in architecture \(A\).

Security rule:  
\[
\text{SAMR}(A) \geq \tau_{\text{SAMR}}
\]

---

## 2. Access Control Architecture

**Metric: Effective Access Control Ratio (EACR)**

Evaluates the effectiveness of access control implementations.

\[
\text{EACR}(A) = \frac{\text{N\_EffectiveAC}(A)}{\text{N\_AC}(A)}
\]

- **N_EffectiveAC(A)**: Number of access control mechanisms properly implemented.
- **N_AC(A)**: Total number of access control mechanisms.

Security rule:  
\[
\text{EACR}(A) \geq \tau_{\text{EACR}}
\]

---

## 3. Input and Output Architecture

**Metric: Input Validation Coverage Ratio (IVCR)**

Measures the extent of input validation applied across the system.

\[
\text{IVCR}(A) = \frac{\text{N\_ValidatedInputs}(A)}{\text{N\_Inputs}(A)}
\]

- **N_ValidatedInputs(A)**: Number of input points with proper validation.
- **N_Inputs(A)**: Total number of input points.

Security rule:  
\[
\text{IVCR}(A) \geq \tau_{\text{IVCR}}
\]

---

## 4. Cryptographic Architecture

**Metric: Cryptographic Strength Ratio (CSR)**

Assesses the proportion of cryptographic implementations using strong algorithms and secure key management.

\[
\text{CSR}(A) = \frac{\text{N\_StrongCrypto}(A)}{\text{N\_Crypto}(A)}
\]

- **N_StrongCrypto(A)**: Number of cryptographic implementations that are strong and secure.
- **N_Crypto(A)**: Total number of cryptographic implementations.

Security rule:  
\[
\text{CSR}(A) \geq \tau_{\text{CSR}}
\]

---

## 5. Data Protection and Privacy Architecture

**Metric: Data Protection Compliance Ratio (DPCR)**

Measures compliance with data protection regulations.

\[
\text{DPCR}(A) = \frac{\text{N\_CompliantDataHandling}(A)}{\text{N\_DataHandling}(A)}
\]

- **N_CompliantDataHandling(A)**: Number of compliant data handling processes.
- **N_DataHandling(A)**: Total number of data handling processes.

Security rule:  
\[
\text{DPCR}(A) \geq \tau_{\text{DPCR}}
\]

---

## 6. Communication Architecture

**Metric: Secure Communication Protocol Ratio (SCPR)**

Evaluates the proportion of communication channels using secure protocols.

\[
\text{SCPR}(A) = \frac{\text{N\_SecureCommChannels}(A)}{\text{N\_CommChannels}(A)}
\]

- **N_SecureCommChannels(A)**: Number of channels using secure protocols (e.g., TLS).
- **N_CommChannels(A)**: Total number of communication channels.

Security rule:  
\[
\text{SCPR}(A) \geq \tau_{\text{SCPR}}
\]

---

## 7. Business Logic Architecture

**Metric: Business Logic Validation Ratio (BLVR)**

Measures how much of the business logic has been validated to prevent logical flaws.

\[
\text{BLVR}(A) = \frac{\text{N\_ValidatedBusinessLogic}(A)}{\text{N\_BusinessLogic}(A)}
\]

- **N_ValidatedBusinessLogic(A)**: Number of validated business logic components.
- **N_BusinessLogic(A)**: Total number of business logic components.

Security rule:  
\[
\text{BLVR}(A) \geq \tau_{\text{BLVR}}
\]

---

## 8. API Architecture

**Metric: API Security Coverage Ratio (ASCR)**

Assesses the proportion of APIs implementing security measures.

\[
\text{ASCR}(A) = \frac{\text{N\_SecuredAPIs}(A)}{\text{N\_APIs}(A)}
\]

- **N_SecuredAPIs(A)**: Number of APIs with proper security measures.
- **N_APIs(A)**: Total number of APIs.

Security rule:  
\[
\text{ASCR}(A) \geq \tau_{\text{ASCR}}
\]

---

## 9. Configuration Architecture

**Metric: Secure Configuration Ratio (SCR)**

Evaluates how many system configurations adhere to security best practices.

\[
\text{SCR}(A) = \frac{\text{N\_SecureConfigs}(A)}{\text{N\_Configs}(A)}
\]

- **N_SecureConfigs(A)**: Number of secure configurations.
- **N_Configs(A)**: Total number of configurations.

Security rule:  
\[
\text{SCR}(A) \geq \tau_{\text{SCR}}
\]

---

These metrics provide a structured, quantifiable way to evaluate security in each architectural category. By establishing minimum thresholds (\(\tau\)) for each ratio, organizations can systematically identify vulnerabilities and guide architectural security verification.
