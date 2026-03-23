# RB-001 — SSH Triage Runbook

## Purpose
This runbook is used to review SSH-related activity on a Linux VPS and identify suspicious login attempts, brute-force behavior, and successful authentication events.

## Scope
- Ubuntu VPS
- SSH service
- Fail2ban
- UFW
- WireGuard-connected administration workflow

## Objectives
- Detect invalid user attempts
- Detect failed password attempts
- Confirm successful public key logins
- Review source IP patterns
- Support daily security summary documentation

## Key checks

### 1. Review SSH authentication logs
Check:
- invalid user attempts
- failed password attempts
- accepted publickey events
- accepted password events

### 2. Review top source IPs
Identify repeated IPs generating invalid access attempts.

### 3. Review Fail2ban status
Confirm:
- currently banned IPs
- total banned IPs
- jail status for SSH

### 4. Review firewall status
Confirm UFW is active and expected SSH/WireGuard rules are present.

## Expected secure state
- Accepted password = 0
- SSH access controlled
- Public key authentication in use
- Fail2ban active
- UFW active

## Output
Results from this runbook should be summarized in a daily security summary and used for incident review when needed.
