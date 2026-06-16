# Technology Fingerprinting Report

## Target

**Domain:** testfire.net  
**IP Address:** 65.61.137.117

---

## Port and Service Enumeration

### Nmap Results

| Port | State | Service | Version |
|--------|--------|---------|---------|
| 80 | Open | HTTP | Apache Tomcat/Coyote JSP Engine 1.1 |
| 443 | Open | HTTPS | Apache Tomcat/Coyote JSP Engine 1.1 |
| 8080 | Open | HTTP | Apache Tomcat/Coyote JSP Engine 1.1 |

---

## HTTP Fingerprinting

### Response Headers

```http
HTTP/1.1 200 OK
Server: Apache-Coyote/1.1
Set-Cookie: JSESSIONID=<value>; Path=/; HttpOnly
Content-Type: text/html;charset=ISO-8859-1
```

### Observations

- Backend appears to be Java-based.
- Apache-Coyote indicates Apache Tomcat deployment.
- Session management uses JSESSIONID cookies.
- HttpOnly cookie attribute is enabled.

---

## WhatWeb Analysis

### Site Information

| Attribute | Value |
|------------|---------|
| Title | Altoro Mutual |
| IP Address | 65.61.137.117 |
| Country | United States |

### Detected Technologies

| Technology | Evidence |
|-------------|------------|
| Apache Tomcat | Apache-Coyote/1.1 |
| Java | Server behavior and JSESSIONID |
| Cookies | JSESSIONID |
| HttpOnly | Session cookie protection |

---

## Service Enumeration Details

### Port 80

- HTTP Service
- Apache Tomcat/Coyote JSP Engine 1.1
- Website Title: Altoro Mutual

### Port 443

- HTTPS Service
- Apache Tomcat/Coyote JSP Engine 1.1
- SSL Enabled

### Port 8080

- HTTP Service
- Apache Tomcat/Coyote JSP Engine 1.1
- Website Title: Altoro Mutual

---

## SSL Certificate Information

| Field | Value |
|---------|---------|
| Common Name | demo.testfire.net |
| Issuer | Sectigo RSA Domain Validation Secure Server CA |
| Key Size | RSA 2048-bit |
| Signature Algorithm | SHA256WithRSAEncryption |
| Valid From | 2025-05-21 |
| Valid Until | 2026-06-21 |

---

## Technology Summary

### Web Stack

- Apache Tomcat
- Apache-Coyote/1.1
- Java/JSP Application
- HTTPS Enabled

### Session Management

- JSESSIONID Cookie
- HttpOnly Attribute Enabled

### Hosting

- Rackspace Infrastructure
- Akamai DNS Services

---

## Key Findings

- Application is running on Apache Tomcat.
- Java technology stack is confirmed.
- Session cookies are protected with HttpOnly.
- Multiple web services are exposed on ports 80, 443, and 8080.
- SSL/TLS is configured using a Sectigo-issued certificate.
