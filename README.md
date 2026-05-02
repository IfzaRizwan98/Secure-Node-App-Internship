# 🔐 Secure Node.js Application – Cybersecurity Internship (Weeks 1–6)

> **Intern Name:** Ifza Rizwan  
> **Intern ID:** DHC-3176  
> **Organization:** Developers Hub Corporation  
> **GitHub Repository:** [Secure-Node-App-Internship](https://github.com/IfzaRizwan98/Secure-Node-App-Internship)  
> **LinkedIn Profile:** [Ifza Rizwan – LinkedIn](https://www.linkedin.com/in/ifza-rizwan)  

---

## 📌 Project Overview

This repository contains a **Node.js web application** that was initially vulnerable to OWASP Top 10 security risks. Over 6 weeks, I performed:

- Vulnerability assessment  
- Security hardening  
- Real-time threat detection  
- Ethical hacking & exploitation  
- Advanced security audits  

The final application is **secure, audited, and deployment-ready**.

---

## 📅 Week 1 – Vulnerability Assessment

**Goal:** Identify vulnerabilities in the application.

**Performed:**
- Manual code review
- XSS (Cross-Site Scripting) testing
- SQL injection testing
- Broken authentication checks

**Findings:**
- SQL injection possible in login
- No rate limiting
- Missing security headers
- No CSRF protection

---

## 📅 Week 2 – Security Implementation (Basic Hardening)

**Implemented:**
- **Helmet.js** – secure HTTP headers
- **Validator & Bcrypt** – input sanitization + password hashing
- **JWT (JSON Web Token)** – secure authentication
- **Winston Logger** – persistent security logging

---

## 📅 Week 3 – Security Auditing & Logging

**Implemented:**
- Persistent logging with Winston (all failed/suspicious actions logged)
- ZAP scan analysis saved
- GitHub repository with full documentation

---

## 📅 Week 4 – Advanced Threat Detection & API Security

| Feature | Implementation | Purpose |
|---------|----------------|---------|
| Rate Limiting | `express-rate-limit` (5 req / 15 min) | Prevent brute force / DDoS |
| CORS | `cors` middleware (allow only localhost:3000) | Restrict unauthorized origins |
| API Key Auth | Custom middleware for `/api` routes | Secure API endpoints |
| CSP + HSTS | Helmet.js (default CSP, HSTS) | Prevent XSS + force HTTPS |

---

## 📅 Week 5 – Ethical Hacking & Exploitation Fixes

### ✅ SQL Injection Prevention
- **Before:** String concatenation in SQL queries  
    ```js
    let query = "SELECT * FROM users WHERE email = '" + email + "'";
    ```

- **After:** Parameterized queries using `?` placeholders  
    ```js
    let query = "SELECT * FROM users WHERE email = ? AND password = ?";
    executeQueryWithParam(query, [email, password]);
    ```

### ✅ CSRF Protection
- Used `csurf` middleware
- CSRF token generated per session and validated on POST requests
- Hidden `_csrf` field added to all forms

---

## 📅 Week 6 – Advanced Security Audits & Final Deployment

**Goal:** Conduct advanced security audits, ensure compliance with OWASP Top 10, and prepare the application for secure deployment.

### Tasks Completed:

#### 1. Security Audits & Compliance
- **OWASP ZAP** – Performed automated security scan
- **Nikto** – Web server vulnerability scanner
- Checked compliance with **OWASP Top 10** best practices

#### 2. Secure Deployment Practices
- Enabled **automatic security updates** and dependency scanning
- Followed **Docker security best practices** (container scanning, avoid root user)

#### 3. Final Penetration Testing
- Used **Burp Suite** for deep penetration testing
- Documented all vulnerabilities and applied fixes


---

## 📊 Final Security Checklist

| Security Control | Week Implemented | Status |
|------------------|----------------|--------|
| Vulnerability Assessment | Week 1 | ✅ |
| Helmet.js & Secure Headers | Week 2 | ✅ |
| JWT & Bcrypt | Week 2 | ✅ |
| Winston Logging | Week 3 | ✅ |
| Rate Limiting | Week 4 | ✅ |
| CORS | Week 4 | ✅ |
| API Key Authentication | Week 4 | ✅ |
| CSP + HSTS | Week 4 | ✅ |
| SQL Injection Prevention | Week 5 | ✅ |
| CSRF Protection | Week 5 | ✅ |
| OWASP ZAP & Nikto Scan | Week 6 | ✅ |
| Penetration Testing | Week 6 | ✅ |
| Zero Trust & WAF (Bonus) | Week 6 | ✅ |

---

## 🚀 How to Run This Project Locally

```bash
# Clone the repository
git clone https://github.com/IfzaRizwan98/Secure-Node-App-Internship.git

# Go to project directory
cd Secure-Node-App-Internship

# Install dependencies
npm install

# Start the application
node app.js
