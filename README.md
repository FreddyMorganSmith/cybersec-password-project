# Password Security Fundamentals

A cybersecurity project exploring password policies, password strength analysis, and breach detection tools.

**Author:** Freddy Morgan-Smith 
**Course:** Cybersecurity & Digital Forensics - Year 2  
**Started:** 07/10/2025

---

## Project Overview

This project demonstrates core password security concepts through three main components:

1. **Password Policy & Enforcement** - Creating organizational security policies
2. **Hashcat Demo** - Demonstrating password cracking and why strength matters
3. **Password Checker Tool** - Building a web app to analyze password strength and check for breaches

---

## Project Structure
password-security-fundamentals/
├── password-policy/              # Security policy documentation
│   ├── password-policy-draft.md
│   ├── enforcement-plan.md
│   └── images/bitwarden-demo/
├── hashcat-demo/                 # Password cracking demonstrations
│   └── (coming soon)
├── password-checker-tool/        # Full-stack web application
│   ├── backend/                  # Python/FastAPI
│   └── frontend/                 # React
└── documentation/                # Project tracking
├── PROGRESS.md
└── SCREENSHOTS.md

---

## Tech Stack

**Documentation:**
- Markdown
- Bitwarden (password manager demo)

**Hashcat Demo:**
- Hashcat
- Python (for result analysis)

**Password Checker Tool:**
- **Backend:** Python, FastAPI
- **Frontend:** React, Tailwind CSS
- **APIs:** Have I Been Pwned (HIBP)
- **Deployment:** Vercel (frontend) + Render (backend)

---

## Current Progress

### ✅ Completed
- [x] Project structure setup
- [x] Password policy document (based on NIST guidelines)
- [x] Enforcement plan with realistic implementation strategy
- [x] Bitwarden demonstration (password manager + MFA)

### 🔄 In Progress
- [ ] Hashcat demo setup
- [ ] Password strength analysis algorithm

### 📋 Upcoming
- [ ] HIBP API integration
- [ ] React frontend development
- [ ] Full deployment

See `documentation/PROGRESS.md` for detailed timeline.

---

## Learning Objectives

**Security Concepts:**
- Password complexity requirements and why they matter
- Multi-Factor Authentication (MFA) implementation
- Password breach detection using k-Anonymity
- Password hashing and cracking techniques
- Security policy development

**Technical Skills:**
- Python API development (FastAPI)
- React frontend development
- RESTful API integration
- Secure coding practices
- Git/GitHub workflow

---

## How to Use This Repository

Each section has its own README with specific setup instructions:

1. **Password Policy:** See `password-policy/README.md`
2. **Hashcat Demo:** See `hashcat-demo/README.md` (coming soon)
3. **Password Checker Tool:** See `password-checker-tool/README.md` (coming soon)

---

## Resources & References

- NIST SP 800-63B: Digital Identity Guidelines
- Have I Been Pwned API: https://haveibeenpwned.com/API/v3
- Bitwarden: https://bitwarden.com
- Hashcat: https://hashcat.net/hashcat/
- OWASP Password Storage Cheat Sheet

---

## License

MIT License - See LICENSE file for details

---

## Contact

Questions or feedback? Feel free to open an issue or reach out.

**Portfolio:** https://www.freddysmith.dev 
**GitHub:** FreddyMorganSmith
