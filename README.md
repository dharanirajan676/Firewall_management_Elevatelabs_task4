# Firewall_management_Elevatelabs_task4
🛡️ Cyber Security Internship - Task 1 ✅, Objective: To block insecure Telnet access and enable secure SSH access in Windows, ensuring remote administration is performed through encrypted communication.

Name: DHARANIRAJAN B
Internship: Elevate Lab – Cyber Security Section

Task 4 – Telnet Vulnerability Removal & SSH Configuration on Windows

Objective:
To block insecure Telnet access and enable secure SSH access in Windows, ensuring remote administration is performed through encrypted communication.

Procedure:

Step 1: Checking for Telnet Service Vulnerability
- Accessed Control Panel → Programs and Features → Turn Windows features on or off.
- Found Telnet Client enabled (used for testing).
- Verified open Telnet port by running in Command Prompt:
  telnet localhost 23
  Result: Connection was successful, confirming port 23 was accessible.

Step 2: Blocking Telnet Port in Firewall
- Opened Windows Defender Firewall with Advanced Security.
- Created an Inbound Rule to block TCP port 23.
- Applied the rule to Domain, Private, and Public profiles.

Step 3: Enabling SSH Access
- Installed OpenSSH Server feature in Windows (Settings → Optional Features → Add a Feature → OpenSSH Server).
- Started the SSH service via:
  net start sshd
- Created a Windows Firewall Inbound Rule to allow TCP port 22 (SSH).
- Applied the rule to all network profiles.

[port details were predefined and browsed on internet]

Step 4: Verification
- Tested Telnet access:
  telnet localhost 23
  Result: Connection failed — port 23 blocked successfully.

- Tested SSH access from another system:
  ssh username@<Windows_IP>
  Result: Connection successful with password prompt, confirming secure remote access.

Scan Summary:
| Risk Level     | Count |
|----------------|-------|
| Critical       | 0     |
| High           | 0     |
| Medium         | 0     |
| Low            | 1     |
| Total Findings | 1     |

Conclusion:
By blocking Telnet port 23 and enabling SSH on port 22, insecure remote access was replaced with an encrypted protocol. This strengthens system security while maintaining administrative accessibility.

