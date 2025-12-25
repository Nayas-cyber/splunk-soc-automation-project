## Failed Login Detection Query

```spl
index="soc-project" EventCode=4625
| stats count by user, ComputerName, src_ip
| where count >= 5

Description:
This query detects multiple failed authentication attempts (Event ID 4625) which may indicate brute-force or unauthorized access attempts.
