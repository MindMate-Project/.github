# Security Policy

## Supported Versions

The following versions of MindMate components currently receive security updates:

| Component | Version | Supported |
|---|---|---|
| Backend API | 1.0.x | ✅ |
| Web App | Latest main | ✅ |
| AI Service | Latest main | ✅ |

---

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

If you discover a security vulnerability in any MindMate repository, please report it responsibly by following these steps:

1. **Email the maintainers** at the contact address listed in the relevant repository's README, or open a [private security advisory](https://github.com/MindMate-Project/.github/security/advisories/new) in this repository.
2. Include as much detail as possible:
   - A description of the vulnerability and its potential impact
   - The repository and file(s) affected
   - Step-by-step instructions to reproduce the issue
   - Any proof-of-concept code (if applicable)
3. **Allow up to 72 hours** for an initial response. We will keep you informed of our progress.

---

## Disclosure Policy

- We follow a **coordinated disclosure** model.
- We ask that you give us a reasonable amount of time to address the issue before any public disclosure.
- We will credit you in the security advisory unless you prefer to remain anonymous.

---

## Security Best Practices for Contributors

When contributing to MindMate, please keep the following in mind:

- **Never commit secrets** — API keys, tokens, passwords, or credentials must not appear in source code. Use environment variables and the provided `.env.example` files.
- **Validate all inputs** — use existing middleware and validation utilities.
- **Keep dependencies updated** — open a PR if you notice a dependency with a known CVE.
- **Use HTTPS** — all external API calls must use encrypted connections.
- **Follow the principle of least privilege** — request only the permissions needed.

---

## Known Security Measures

MindMate Backend implements the following security controls:

- JWT authentication with expiry and signature verification
- bcryptjs password hashing
- Input validation on all routes
- CORS restrictions
- Role-based access control (user / patient / caregiver / admin)
- Cloudinary secure upload validation
