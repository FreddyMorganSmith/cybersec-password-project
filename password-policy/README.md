# Password Policy Documentation

This folder contains the password security policy and enforcement plan I created for this project.

## What's Here

- **password-policy-draft.md** - Full password security policy document
- **enforcement-plan.md** - Implementation and enforcement strategy
- **images/bitwarden-demo/** - Screenshots showing Bitwarden setup and MFA

## How I Created This

I started with a basic NIST password policy template and adapted it for a realistic company scenario. The policy covers:
- Password complexity requirements (12+ chars, complexity, no reuse)
- MFA requirements for critical systems
- Bitwarden as the organizational password manager
- Account lockout policies
- User responsibilities

The enforcement plan outlines how this would actually be rolled out in phases, including training, technical setup, and monitoring.

## Key Takeaways

**What I learned:**
- Why password managers are essential (humans are bad at remembering strong passwords)
- How MFA actually works (authenticator app + password = 2 factors)
- K-Anonymity model for checking breached passwords without exposing them
- Real-world implementation challenges (user resistance, legacy systems, budget)

**Bitwarden Features Demonstrated:**
- Secure password generation (16+ chars with complexity)
- MFA setup using authenticator app
- Encrypted vault storage
- Cross-platform sync

## Tools Used

- **Bitwarden** - Password manager (free tier)
- **Microsoft Authenticator** - MFA app
- **Markdown** - Documentation format

## Next Steps

Moving on to the Hashcat demo to show why weak passwords are dangerous and how quickly they can be cracked.

---

**Author:** Freddy Morgan-Smith 
**Date:** 07/10/2025
**Project:** Password Security Fundamentals