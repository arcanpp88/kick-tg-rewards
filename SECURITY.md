# Security Policy

## 📌 Supported Versions

The following branches of **Drops Crypto** are currently supported with security updates:

| Branch | Supported |
|------|-----------|
| main | ✅ Yes |
| dev  | ⚠️ Best effort |
| others | ❌ No |

---

## 🚨 Reporting a Vulnerability

If you discover a security vulnerability, **please do not open a public GitHub issue**.

Instead, report it privately using **GitHub Security Advisories**:

- Go to the repository
- Open the **Security** tab
- Click **Report a vulnerability**

If GitHub Advisories are not available, you may contact the maintainers directly via a private message on GitHub.

Please include:
- A clear description of the issue
- Steps to reproduce
- Potential impact
- Proof of concept (if available)

We aim to respond within **48 hours**.

---

## 🔐 Security Scope

### In scope
- Twitch OAuth 2.0 authentication flow
- JWT-based authorization
- API endpoints related to authentication and user data
- Wallet linking logic
- Mobile ↔ Backend communication
- Environment variable handling

### Out of scope
- Denial of Service (DoS / DDoS)
- Social engineering attacks
- Vulnerabilities in third-party services (Twitch, Expo, ngrok)
- Compromised user devices

---

## 🛡 Security Practices

### Backend
- OAuth tokens are never exposed to the client
- JWT tokens are short-lived
- Secrets are stored only in environment variables
- Prisma ORM is used to mitigate SQL injection
- Input validation on all public endpoints

### Mobile Application
- No secrets embedded in the client
- Secure storage used for authentication tokens
- HTTPS enforced for all API requests

---

## 🔎 Vulnerability Disclosure Process

1. Vulnerability reported privately
2. Issue triaged and validated
3. Fix developed and tested
4. Patch released
5. Public disclosure if appropriate

---

## ⚖️ Responsible Disclosure

By reporting a vulnerability, you agree to:
- Act in good faith
- Avoid accessing or modifying user data
- Avoid service disruption
- Allow reasonable time for remediation

We will not pursue legal action against researchers who follow this policy.

---

## 🙏 Acknowledgements

We thank security researchers and contributors for responsible disclosure
and for helping improve the security of **Drops Crypto**.
