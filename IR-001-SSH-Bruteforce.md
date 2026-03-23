# IR-001 — SSH Brute-Force Activity

## Incident title
Repeated SSH brute-force and invalid user attempts against Ubuntu VPS

## Date
YYYY-MM-DD

## Analyst
Telli

## Severity
Low to Moderate

## Summary
This incident report documents repeated SSH-related hostile activity observed against a public-facing Ubuntu VPS. The activity included invalid user attempts and repeated authentication probing from external IP addresses. No successful password-based compromise was confirmed.

## Affected asset
- Ubuntu VPS
- SSH service

## Detection source
- SSH authentication logs
- Fail2ban status
- UFW review

## Indicators observed
- Invalid user attempts
- Repeated source IP activity
- Authentication probing behavior
- Brute-force style login attempts

## Key findings
- Accepted password events: 0
- Accepted publickey events: [fill]
- Failed password attempts: [fill]
- Invalid user attempts: [fill]
- Fail2ban active: Yes
- UFW active: Yes

## Impact assessment
At the time of review, no evidence confirmed a successful compromise. The observed activity indicates routine hostile internet scanning and brute-force attempts against SSH exposure.

## Actions taken
- Reviewed SSH logs
- Reviewed repeated source IPs
- Confirmed public key login usage
- Confirmed password-based successful authentication remained zero
- Verified Fail2ban jail status
- Verified UFW active rules

## Current status
Contained / Monitored

## Recommendations
- Continue daily SSH log review
- Keep public key authentication enforced
- Maintain Fail2ban protection
- Maintain UFW review and expected rule validation
- Document repeated high-volume source IP patterns

## Notes
This report is part of a practical Blue Team / SOC learning portfolio focused on VPS hardening, monitoring, and incident documentation.
