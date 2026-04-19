# log-analysis-project-
# Brute Force Attack Detection Project

## Description
This project simulates a brute force attack against a system and analyzes authentication logs to detect malicious activity.

## Environment
- Attacker: Kali Linux
- Target: Ubuntu (SSH enabled)
- Attack Tool: Hydra

## Attack Scenario
- Multiple login attempts targeting the admin account
- Repeated failed login attempts
- Successful login after multiple failures

## Sample Log
"
Failed password for admin from 192.168.1.10 port 22 ssh2
Failed password for admin from 192.168.1.10 port 22 ssh2
Failed password for admin from 192.168.1.10 port 22 ssh2
Accepted password for admin from 192.168.1.10 port 22 ssh2
"
## Analysis
Multiple failed login attempts followed by a successful login indicate a brute force attack.  
This suggests that the attacker successfully guessed the correct password.

## Detection Logic
IF failed_login > 3 AND success_login  
THEN brute_force_attack

## Incident Report
- Incident Type: Brute Force Attack
- Target: SSH (admin account)
- Findings:
  - Repeated failed login attempts
  - Successful login after failures
- Risk Level: High

## Recommendations
- Enable account lockout policy
- Implement multi-factor authentication (MFA)
- Monitor login attempts and IP behavior

## Skills Gained
- Log Analysis
- Attack Detection
- Incident Response
- Cybersecurity Fundamentals
