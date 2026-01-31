# Sudo Privilege Escalation Detection (Linux SOC Project)

## 📌 Overview
This project simulates a **real-world SOC (Security Operations Center) investigation** focused on detecting **privilege escalation and misuse of sudo access** on a Linux system.

The analysis examines authentication logs to identify:
- Frequent sudo usage
- Time-based sudo anomalies
- High-risk administrative commands
- Script-based or non-interactive sudo execution
- Potential insider threat or compromised user behavior

---

## 🎯 Objectives
- Monitor and analyze sudo activity from Linux authentication logs
- Detect abnormal privilege escalation patterns
- Classify sudo commands based on risk severity
- Correlate user actions with executed commands
- Generate a SOC-style incident report with findings and recommendations

---

## 🛠 Tools & Technologies
- Ubuntu Linux (WSL)
- Bash / Shell utilities
- grep, awk, sed, sort, uniq
- Git & GitHub

---

## 📁 Project Structure
```text
sudo-privilege-analysis/
├── logs/
│   └── auth.log
├── analysis/
│   ├── sudo_commands.txt
│   ├── frequent_sudo_users.txt
│   ├── sudo_burst.txt
│   ├── sudo_time_only.txt
│   ├── sudo_time_analysis.txt
│   ├── sudo_executed_commands.txt
│   ├── high_risk_commands.txt
│   ├── high_severity.txt
│   ├── medium_risk_commands.txt
│   ├── low_risk_commands.txt
│   ├── sudo_no_tty.txt
│   ├── sudo_script_execution.txt
│   ├── user_command_map.txt
│   ├── sudo_alert_users.txt
│   └── timeline.txt
└── incident_report.md


----
🔍 Methodology

Collected authentication logs from /var/log/auth.log

Extracted all sudo-related events

Filtered PAM session noise to isolate real sudo command execution

Identified users with frequent sudo usage

Performed time-based anomaly and burst analysis

Extracted and classified executed commands by severity

Checked for non-interactive (no TTY) and script-based sudo usage

Built an event timeline for escalation analysis

Documented findings in a structured SOC incident report


------

📊 Key Findings

User uttej executed sudo commands multiple times (baseline exceeded)

No high-risk or destructive administrative commands were observed

No sudo usage without TTY detected

No script-based or automated sudo abuse identified

No persistence mechanisms (cron jobs) were found


-----

🧠 SOC Interpretation

The system shows frequent privileged access, which may require monitoring, but no direct malicious activity was detected.
Findings suggest legitimate administrative usage with no confirmed compromise.
-----

📄 Incident Report

Detailed analysis, risk assessment, and remediation steps are documented in:

incident_report.md

------

🧩 MITRE ATT&CK Mapping

TA0004 – Privilege Escalation

T1548 – Abuse Elevation Control Mechanism (sudo)



-----
🚀 Learning Outcomes

Hands-on experience with Linux privilege escalation detection

Practical SOC-style log analysis and correlation

Understanding of sudo abuse indicators

Exposure to detection engineering and SIEM-like alert logic

Improved incident reporting and security documentation skills


-----

⚠️ Note

This project uses local system activity for analysis.
No real-world attack was performed; the focus is on detection methodology, not exploitation.



👤 Author

Uttej Kumar Sadanala
Cybersecurity Enthusiast | SOC Analyst Aspirant
