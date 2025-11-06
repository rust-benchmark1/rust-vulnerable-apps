# rust-vulnerable-apps

This repo contains examples of some common Rust related security vulnerabilities. These currently include:

*  CORS (Cross-Origin Resource Sharing) Misconfiguration: This occurs when improper CORS policies allow unauthorized domains to access resources, leading to potential data leaks or unauthorized actions.

*  Hardcoded Secret: Storing sensitive information such as API keys, passwords, or tokens directly in the source code, which can be exposed if the code is shared or compromised.

*  SQL Injection (SQLi): A vulnerability that allows an attacker to manipulate SQL queries by injecting malicious input, leading to unauthorized access, data leaks, or even database compromise.

*  Server-Side Request Forgery (SSRF): An attacker tricks the server into making requests to internal or external resources that the attacker wouldn’t normally have access to, which could lead to information disclosure or further attacks.

*  Cross-Site Scripting (XSS): A vulnerability that allows attackers to inject malicious scripts into web pages viewed by other users, potentially leading to data theft, session hijacking, or spreading malware.

# Vulnerabilities Overview

## /cors/cors_001_bad_warp/src/main.rs
**Example 1** - CWE-942: Permissive Cross-domain Security Policy with Untrusted Domains (Supported)

Expected to be detected.
- **Source/Sink:** Line 7

---

## /cors/cors_002_bad_iron/src/main.rs
**Example 1** - CWE-942: Permissive Cross-domain Security Policy with Untrusted Domains (Supported)

Expected to be detected.
- **Source/Sink:** Line 13

---

## /cors/cors_003_bad_axum_tower_http/src/main.rs
**Example 1** - CWE-942: Permissive Cross-domain Security Policy with Untrusted Domains (Supported)

Expected to be detected.
- **Source/Sink:** Line 26

---

## /hardcoded_secret/hardcoded_secret_bad_01_age/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 51
- **Sink:** Line 19

**Example 2** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 51
- **Sink:** Line 42

---

## /hardcoded_secret/hardcoded_secret_bad_02_age/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 18

**Example 2** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 40

---

## /hardcoded_secret/hardcoded_secret_bad_03_aes/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 16
- **Sink:** Line 21

---

## /hardcoded_secret/hardcoded_secret_bad_04_aes/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 16
- **Sink:** Line 21

---

## /hardcoded_secret/hardcoded_secret_bad_05_aes/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 14
- **Sink:** Line 20

---

## /hardcoded_secret/hardcoded_secret_bad_06_camellia/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 13
- **Sink:** Line 18

---

## /hardcoded_secret/hardcoded_secret_bad_07_orion/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source:** Line 21
- **Sink:** Line 23

---
## /hardcoded_secret/hardcoded_secret_bad_08_orion/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 13

---

## /hardcoded_secret/hardcoded_secret_bad_10_age/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 17

**Example 2** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 39

---
## /hardcoded_secret/hardcoded_secret_bad_11_age/src/main.rs
**Example 1** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 17

**Example 2** - CWE-321: Use of Hard-coded Cryptographic Key (Not supported)

- **Source/Sink:** Line 39

---
## /sqli/sqli_bad_003_sqlx/src/main.rs
**Example 1** - CWE-89: SQL Injection (Supported)

The source is low probability.
- **Source:** Line 32
- **Sink:** Line 23

---
## /sqli/sqli_bad_004_sqlx/src/main.rs
**Example 1** - CWE-89: SQL Injection (Supported)

The source is low probability.
- **Source:** Line 13
- **Sink:** Line 21

---
## /sqli/sqli_bad_005_diesel/src/main.rs
**Example 1** - CWE-89: SQL Injection (Supported)

The source is low probability.
- **Source:** Line 35
- **Sink:** Line 37

---
## /sqli/sqli_bad_006_diesel/src/main.rs
**Example 1** - CWE-89: SQL Injection (Supported)

The source is low probability.
- **Source:** Line 36
- **Sink:** Line 41

---
## /sqli/sqli_bad_007_postgres/src/main.rs
**Example 1** - CWE-89: SQL Injection (Supported)

The source is low probability.
- **Source:** Line 12
- **Sink:** Line 19

---
## /sqli/sqli_bad_007_postgres/src/Sqli_bad_007.rs
**Example 1** - CWE-89: SQL Injection (Supported)

The source is low probability.
- **Source:** Line 7
- **Sink:** Line 14

---
## /sqli/sqli_bad_009_sqlx/src/main.rs
**Example 1** - CWE-89: SQL Injection (Supported)

Expected to be detected.
- **Source:** Line 21
- **Sink:** Line 26

**Example 2** - CWE-79: Cross-site Scripting (Supported)

Expected to be detected.
- **Source:** Line 21
- **Sink:** Line 32

---
## /ssrf/ssrf_001_bad_iron/src/main.rs
**Example 1** - CWE-918: Server-Side Request Forgery - SSRF (Supported)

Expected to be detected.
- **Source:** Line 16
- **Sink:** Line 18

**Example 2** - CWE-79: Cross-site Scripting (Supported)

Expected to be detected.
- **Source:** Line 16
- **Sink:** Line 24
---

## /ssrf/ssrf_002_bad_reqwest_client/src/main.rs
**Example 1** - CWE-918: Server-Side Request Forgery - SSRF (Supported)

Expected to be detected.
- **Source:** Line 17
- **Sink:** Line 19

**Example 2** - CWE-79: Cross-site Scripting (Supported)

Expected to be detected.
- **Source:** Line 17
- **Sink:** Line 25
---

## /xss/xss_001_bad_warp/src/main.rs
**Example 1** - CWE-79: Cross-site Scripting (Supported)

Expected to be detected.
- **Source:** Line 7
- **Sink:** Line 9
---

## /xss/xss_002_bad_iron/src/main.rs
**Example 1** - CWE-79: Cross-site Scripting (Supported)

Expected to be detected.
- **Source:** Line 8
- **Sink:** Line 11