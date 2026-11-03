# Web-Application-pen-testing-BRUTE-FORCE-DVWA

## OVERVIEW

This lab is a practical exercise to show how poorly protected login screens let hackers use automated tools to endlessly guess passwords until they finally break into an account.

## Lab Environment & Toolset

Target Application: Damn Vulnerable Web Application (DVWA)

Interception Proxy: Burp Suite (Proxy / Intercept / Intruder)

Attack Method: Cluster Bomb attack leveraging custom username and password lists.

## STEP - 1 Setup Metasploit , DVWA & BURPSUITE

It means downloading and preparing the three main tools you need for the lab: Metasploit (to run exploits), DVWA (your vulnerable practice website), and Burp Suite (to intercept and tamper with web traffic).
<img width="1920" height="991" alt="meta  Running  - Oracle VirtualBox 28_10_2026 14_39_22" src="https://github.com/user-attachments/assets/cf9989d0-b71f-43f9-87ef-fc2179233ea2" />
<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 03_11_2026 11_30_59" src="https://github.com/user-attachments/assets/436588f1-571b-4e30-b1f4-b9806b0c8b3f" />
<img width="1920" height="1020" alt="Damn Vulnerable Web App (DVWA) v1 0 7 __ Welcome and 1 more page - Personal - Microsoft​ Edge 28_10_2026 14_50_30" src="https://github.com/user-attachments/assets/eeff9363-7300-45bd-85d9-a2cb5544ceb7" />



## STEP - 2 Launch DVWA

A) Set the security level to medium
<img width="1920" height="1020" alt="Damn Vulnerable Web App (DVWA) v1 0 7 __ Welcome and 1 more page - Personal - Microsoft​ Edge 28_10_2026 14_50_53" src="https://github.com/user-attachments/assets/c31dcbd5-6fd9-483b-a9f5-b0a1c816fb1d" />

B) Brute Force section
Open DVWA, click on the Brute Force section, and try logging in using incorrect usernames and passwords


<img width="1920" height="1020" alt="Damn Vulnerable Web App (DVWA) v1 0 7 __ Vulnerability_ Brute Force - Personal - Microsoft​ Edge 03_11_2026 14_08_32" src="https://github.com/user-attachments/assets/50c445b9-9c1f-46d2-a0ea-dc901c601ed3" />

## STEP - 3 Launch Burp suite

Go to the Proxy tab in Burp Suite, click on the Intercept sub-tab, and make sure interception is turned on before you load your DVWA page so it can catch the web traffic.
<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 29_10_2026 11_05_43" src="https://github.com/user-attachments/assets/ec80e71b-95f8-4cfb-9f6e-ed8eab299844" />
<img width="1920" height="1020" alt="PortSwigger - Chromium 03_11_2026 13_42_34" src="https://github.com/user-attachments/assets/b536e4ac-0b4e-41ba-81b2-0aff3699351c" />

## STEP - 4 Capture Web Traffic

Go to the Proxy tab in Burp Suite, click on the Intercept sub-tab, and make sure interception is turned on before you load your DVWA page so it can catch the web traffic
<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 29_10_2026 11_09_03" src="https://github.com/user-attachments/assets/259d9963-ee01-486c-a2c3-5150f59e7c19" />

## STEP - 5 Analyse Intruder Tab

Mark where the username and password go, then choose the 'Cluster Bomb' attack type

<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 03_11_2026 14_40_14" src="https://github.com/user-attachments/assets/5a1e70e0-0f79-4107-8ad2-0217f6b18f96" />

## STEP - 6 Create Username & Password wordlist

Create sample lists of usernames and passwords with different variations so you can feed them into the Cluster Bomb attack & then start the attack.

<img width="1900" height="1008" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 03_11_2026 14_45_36" src="https://github.com/user-attachments/assets/37f06380-6b04-4635-961b-23590e2a9369" />
<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 03_11_2026 14_45_02" src="https://github.com/user-attachments/assets/06e13640-16a3-4a56-9f32-4a02fb1c689e" />

## STEP - 6 Gaining password access

<img width="1900" height="1008" alt="2  Intruder attack of http___192 168 1 104 03_11_2026 14_48_26" src="https://github.com/user-attachments/assets/db556c46-5f4e-42de-a034-7c86701ea363" />

<img width="1920" height="1020" alt="2  Intruder attack of http___192 168 1 104 03_11_2026 14_53_37" src="https://github.com/user-attachments/assets/66788392-402a-4e90-b09d-b4829dfe0ac0" />

## Conclusion & Remediation

The DVWA Brute Force lab demonstrates that web applications lacking robust authentication controls are highly susceptible to automated credential guessing. By intercepting traffic via Burp Suite and executing a Cluster Bomb attack, accounts can be successfully compromised across vulnerable difficulty levels.

Recommended Remediations
To protect authentication mechanisms against brute force and credential stuffing attacks, implement the following controls:

Rate Limiting & Account Lockout: Temporarily lock accounts or enforce exponential delays after a set number of consecutive failed login attempts (e.g., 5 failures).

Multi-Factor Authentication (MFA): Require a secondary verification method (such as an authenticator app or hardware token) beyond standard passwords.

CAPTCHA / Challenge-Response: Integrate automated challenge systems on login forms after failed attempts to disrupt automated script execution.

Robust Logging & Monitoring: Monitor authentication traffic for high-frequency request spikes or unusual patterns indicative of automated tooling.
