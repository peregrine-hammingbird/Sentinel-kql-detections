## What it detects
- Single IP performs failed sign-ins against many user accounts in a short time window.

## MITRE
- TA0006 Credential Access
- T1110 Brute Force / password spraying

## False positives
- 社内プロキシ/NAT配下の誤検知（多数ユーザーが同一IPに見える）
- SSO障害で一斉失敗
- 監査ツール/正規スキャナ

## Tuning knobs
- minUsers を環境に合わせて上げる
- ClientAppUsed や AppDisplayName で対象を絞る
- 既知のプロキシIPを allowlist
