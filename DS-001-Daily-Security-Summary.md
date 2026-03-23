# DS-001 — Daily Security Summary

## Date
2026-03-04

## Analyst
Telli

## Asset
Ubuntu VPS

## Scope
- SSH
- Fail2ban
- UFW
- WireGuard

## Summary
This daily security summary reviews the current security state of the VPS, with attention to SSH activity, brute-force behavior, firewall status, Fail2ban enforcement, and secure remote administration. No successful password-based compromise was observed.

## Key observations

### SSH activity
- Invalid user attempts: 140
- Failed password attempts: 0
- Accepted publickey events: 1
- Accepted password events: 0

### Source IP review
- Top repeated source IPs observed:
  - 2.57.x.x — 20
  - 2.57.x.x — 19
  - 80.94.x.x — 15
  - 80.94.x.x — 4
  - 193.32.x.x — 4
- Suspicious patterns noted: repeated invalid-user probing and brute-force style SSH scanning from external IPs

### Fail2ban
- Jail status: active
- Currently banned: [fill if you want later]
- Total banned: [fill if you want later]

### UFW firewall
- Status: active
- Expected rules present: Yes

### WireGuard
- Tunnel status: operational
- Last handshake review: normal / active

## Security assessment
- Current risk level: Low to Moderate
- Main concern today: repeated SSH brute-force and invalid-user attempts against a public-facing VPS
- Overall system state: stable, monitored, and protected by public-key authentication, Fail2ban, and UFW

## Actions taken
- Reviewed SSH authentication logs
- Reviewed top repeated source IP patterns
- Confirmed accepted password remained zero
- Verified UFW active status
- Verified Fail2ban protection remained enabled

## Recommended next steps
- Continue daily SSH log review
- Maintain public-key-only administration model
- Continue documenting repeated hostile source IP patterns

## Notes
This summary is intended to support daily monitoring, incident visibility, and portfolio documentation for Blue Team learning work.
