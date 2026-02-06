# Password Spray Detection (Microsoft Sentinel)

## What it detects
Detects potential password spraying activity where a single IP address attempts authentication against multiple user accounts within a short time window.

## MITRE ATT&CK Mapping
- TA0006 – Credential Access
- T1110.003 – Password Spraying

## Detection Logic
- Time window: 1 hour
- Aggregation bin: 5 minutes
- Minimum failed attempts: 20
- Minimum distinct users targeted: 8

## False Positives
- Corporate NAT or proxy environments
- Identity provider outages
- Internal security scanning tools

## Tuning Recommendations
- Increase `minUsers` for large environments
- Exclude trusted IP ranges
- Filter specific `AppDisplayName` if necessary

