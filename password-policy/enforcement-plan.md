# Password Policy Enforcement Plan

**Author:** Freddy Morgan-Smith
**Date:** 07/10/2025
**For:** Password Security Fundamentals Project

---

## Purpose
This document outlines how the password policy would actually be implemented in a real organization. It covers the technical setup, rollout plan, and how to handle problems.

---

## Implementation Timeline

### Week 1-2: Setup
- Install and configure Bitwarden for the organization
- Set up Active Directory password complexity requirements
- Test everything with IT team first

### Week 3-4: Training
- Run training sessions for all staff (groups of 10-15)
- Show people how to use Bitwarden and set up MFA
- Create quick reference guide (1 page)

### Week 5-6: Deployment
- Roll out to departments one at a time
- Sales → Operations → Admin → Remote workers
- Help desk on standby for issues

### Week 7+: Monitoring
- Check compliance monthly
- Run password audits quarterly
- Update policy based on what's working/not working

---

## Technical Setup

### Active Directory Settings
Need to configure:
- Minimum password length: 12 characters
- Complexity enabled (uppercase, lowercase, numbers, symbols)
- Account lockout after 5 failed attempts
- 30 minute lockout duration
- Password history: remember last 5 passwords

### Bitwarden Configuration
- Create organization account
- Set up user groups by department
- Require MFA for all users
- Configure master password requirements (12+ chars, complex)

### MFA Enforcement
Enable MFA on these systems first:
- Email (Microsoft 365 or Google Workspace)
- VPN access
- Any admin/privileged accounts
- Cloud services (AWS, Azure, etc.)

Use Microsoft Authenticator or Google Authenticator (free and most people already have them).

---

## Password Breach Checking

Use Have I Been Pwned API to check if passwords have been leaked.

Basic process:
1. Hash the password with SHA-1
2. Send first 5 characters of hash to HIBP API (k-Anonymity model - keeps full password private)
3. Check if rest of hash appears in results
4. If found → force password reset

Run this check:
- When users create new passwords
- Monthly scan of all accounts
- Immediately when new major breach announced

---

## Training Materials Needed

**30-Minute Training Session:**
1. Why this matters - show breach statistics, real examples
2. New policy requirements - what's changing
3. Bitwarden demo - hands-on setup
4. MFA setup - scan QR code with phone

**Follow-up Resources:**
- 1-page quick reference card
- Video tutorial (5 min screencast)
- FAQ document
- Help desk contact info

---

## Handling Common Issues

**"I forgot my master password!"**
- Can't recover it (that's how encryption works!)
- User has to create new account
- Lesson learned: write it down somewhere safe at home

**"MFA is annoying!"**
- Explain why it's necessary (show breach stats)
- Most people get used to it in a week
- It's required - no exceptions for critical systems

**"Bitwarden won't work on my phone!"**
- Check app is updated
- Try browser extension instead
- Worst case: use desktop app only

**"My account keeps locking out!"**
- Check for malware/keylogger
- Verify no one else using account
- Check for automated scripts using old password
- Reset password and re-enable MFA

---

## Compliance Monitoring

**Monthly Checks:**
- How many users have enabled MFA? 
- How many using Bitwarden? 
- Any accounts with weak passwords found?
- Any breached credentials detected?

**Quarterly Audit:**
- Run password cracking test on domain hashes (with permission!)
- Check for password reuse across accounts
- Review account lockout logs for patterns
- Update training based on common issues

**Tools to Use:**
- Hashcat for password strength testing
- HIBP API for breach monitoring
- Active Directory reports for lockouts
- Google Forms for user feedback

---

## When Things Go Wrong

**Password Compromised:**
1. Lock the account immediately
2. Call the user (don't email - their email might be hacked)
3. Check logs for what they accessed
4. Reset password in person with ID verification
5. Re-enable MFA
6. Monitor account for next 30 days

**Mass Breach (Multiple Accounts):**
1. Emergency meeting with IT team
2. Force password reset for all affected accounts
3. Email all staff about the incident
4. Review security controls - how did this happen?
5. Update policy to prevent it happening again

---

## Budget Estimate

Rough costs for 100-person company:

- Bitwarden Teams: ~$3,000/year
- Hardware security keys (for admins): ~$500 one-time
- Training time: ~40 hours of staff time
- Password auditing tools: ~$1,000/year

**Total: ~$4,500/year**

Compare this to average cost of a data breach: $4.45 million (IBM 2023 study)

Worth it.

---

## Notes & Lessons Learned

*This section would be filled in during actual implementation*

Things that worked well:
- 

Things that didn't work:
- 

Would do differently next time:
- 

---

## References

- NIST SP 800-63B: Digital Identity Guidelines
- Have I Been Pwned API: https://haveibeenpwned.com/API/v3
- Bitwarden Documentation: https://bitwarden.com/help/
- Microsoft Password Guidance: https://aka.ms/passwordguidance

---

**End of Document**