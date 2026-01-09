# Security Policy

## 📌 Supported Versions

The following versions of **Drops Crypto** are currently supported with security updates:

| Version | Supported |
|--------|-----------|
| main   | ✅ Yes    |
| dev    | ⚠️ Best effort |
| < 1.0  | ❌ No     |

---

## 🚨 Reporting a Vulnerability

If you discover a security vulnerability, **please do not open a public issue**.

Instead, report it responsibly using one of the following channels:

- 📧 **Email**: security@dropscrypto.app *(recommended)*
- 📬 **Private GitHub Security Advisory**
- 🔐 Encrypted report (PGP) — on request

Please include:
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Proof of concept (if available)

We aim to respond **within 48 hours**.

---

## 🔐 Security Scope

### In scope
- Twitch OAuth 2.0 flow
- JWT authentication & authorization
- API endpoints (`/auth`, `/me`, `/wallets`)
- Mobile ↔ API communication
- Wallet linking logic
- Environment variable handling

### Out of scope
- Denial of Service (DoS/DDoS)
- Social engineering attacks
- Third-party service vulnerabilities (Twitch, Expo, ngrok)
- Physical device compromise

---

## 🛡 Security Practices

### Backend
- OAuth tokens are never exposed to the client
- JWT tokens have limited lifetime
- Secrets stored only in `.env`
- Prisma ORM prevents SQL injection
- Rate limiting on auth endpoints

### Mobile App
- Secure token storage (SecureStore / Keychain)
- No secrets embedded in the client
- HTTPS enforced for all API requests

---

## 🔎 Vulnerability Disclosure Process

1. Report received
2. Triage & validation
3. Patch development
4. Coordinated disclosure
5. Public fix announcement (if applicable)

---

## 🧪 Security Testing

- Manual testing during development
- Dependency scanning via `npm audit`
- Planned integration of SAST / DAST tools

---

## ⚖️ Legal

By reporting a vulnerability, you agree to:
- Act in good faith
- Avoid data exfiltration
- Avoid service disruption
- Give us reasonable time to fix the issue

We will not take legal action against researchers who follow this policy.

---

## 📄 Acknowledgements

We appreciate the efforts of security researchers and responsible disclosure.

Thank you for helping keep **Drops Crypto** secure.
