# Secure-Node-App-Internship
"Security hardening of a vulnerable Node.js application. Implemented JWT authentication, Bcrypt password hashing, Helmet.js for secure headers, and Winston for security audit logging. Part of my Cybersecurity Internship project."

🛡️ Secure Node.js Web Application - Cybersecurity Internship

📌 Project Overview

This project focused on identifying, exploiting, and remediating critical vulnerabilities in a Node.js web application. Over a 3-week intensive security assessment, the application was transformed from a highly vulnerable state to a hardened, production-ready environment.

🛠️ Phase 1: Vulnerability Assessment (Week 1)

Identified critical security flaws using both automated tools and manual penetration testing techniques:

Automated Scanning: Used OWASP ZAP to identify 13+ alerts including SQL Injection and Missing Security Headers.

Manual Exploitation: Successfully executed Stored XSS (Cross-Site Scripting) and SQL Injection Login Bypass payloads.

Information Leakage: Captured verbose error messages (Stack Traces) leaking server folder structures.

🔐 Phase 2: Security Implementation (Week 2)

Implemented industry-standard defense mechanisms to mitigate identified risks:

Secure HTTP Headers: Integrated Helmet.js to hide server signatures (X-Powered-By) and prevent Clickjacking/XSS.

Input Sanitization: Used Validator.js to escape user inputs, effectively neutralizing XSS attack vectors.

Password Hashing: Replaced plain-text storage with salted hashes using Bcryptjs (Salt factor: 10).

Enhanced Authentication: Implemented JWT (JSON Web Tokens) for stateless and secure session management.

Data Integrity: Enforced Email Validation to ensure only legitimate identity formats are accepted.

📊 Phase 3: Advanced Logging & Testing (Week 3)

Finalized the security posture with persistent auditing and reconnaissance:

Persistent Logging: Integrated Winston Logger to capture security events in a dedicated security.log file.

Penetration Testing: Conducted a service-level scan using Nmap to verify port security and header implementation.

Security Audit Trails: Created real-time console and file-based logs for every sensitive profile update and authentication event.

🚀 How to Run

Clone the repository: git clone [https://github.com/IfzaRizwan98/Secure-Node-App-Internship]

Install dependencies: npm install

Start the secure server: npm start

Check logs: View security.log for real-time audit trails.

📂 Project Structure

app.js: Main entry point with Helmet and Winston integration.

routes/users/user.js: Core controller with Bcrypt, JWT, and Validation logic.

security.log: Permanent record of all security-sensitive operations.

Final_Security_Report.pdf: Comprehensive documentation of the entire internship journey.
