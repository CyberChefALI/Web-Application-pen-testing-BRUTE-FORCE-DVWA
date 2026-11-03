# Web-Application-pen-testing-BRUTE-FORCE-DVWA

## OVERVIEW

This lab is a practical exercise to show how poorly protected login screens let hackers use automated tools to endlessly guess passwords until they finally break into an account.

## Prerequisites

Ensure you have DVWA installed and running.
Familiarize yourself with BurpSuite and the FoxyProxy extension for effective testing.

## STEP - 1 Setup Metasploit , DVWA & BURPSUITE

It means downloading and preparing the three main tools you need for the lab: Metasploit (to run exploits), DVWA (your vulnerable practice website), and Burp Suite (to intercept and tamper with web traffic).
<img width="1920" height="991" alt="meta  Running  - Oracle VirtualBox 28_10_2026 14_39_22" src="https://github.com/user-attachments/assets/cf9989d0-b71f-43f9-87ef-fc2179233ea2" />
<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 03_11_2026 11_30_59" src="https://github.com/user-attachments/assets/436588f1-571b-4e30-b1f4-b9806b0c8b3f" />
<img width="1920" height="1020" alt="Damn Vulnerable Web App (DVWA) v1 0 7 __ Welcome and 1 more page - Personal - Microsoft​ Edge 28_10_2026 14_50_30" src="https://github.com/user-attachments/assets/eeff9363-7300-45bd-85d9-a2cb5544ceb7" />


## STEP - 2 Launch Burp Suite and navigate to the Proxy tab.

Open Burp Suite and click on the Proxy tab at the top of the window to access your web traffic controls.
<img width="1920" height="1020" alt="PortSwigger - Chromium 03_11_2026 13_42_34" src="https://github.com/user-attachments/assets/a8981e7d-a44b-4d12-8046-fda8dcf115dc" />
<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 29_10_2026 11_05_43" src="https://github.com/user-attachments/assets/a18a37c8-7f18-4eb8-a8a0-30f9fbc10721" />


## STEP - 3 Launch DVWA

A) Set the security level to medium
<img width="1920" height="1020" alt="Damn Vulnerable Web App (DVWA) v1 0 7 __ Welcome and 1 more page - Personal - Microsoft​ Edge 28_10_2026 14_50_53" src="https://github.com/user-attachments/assets/c31dcbd5-6fd9-483b-a9f5-b0a1c816fb1d" />

B) Brute Force section
Open DVWA, click on the Brute Force section, and try logging in using i<img width="1920" height="1020" alt="Burp Suite Community Edition v2026 9 3 - Temporary Project 29_10_2026 11_05_43" src="https://github.com/user-attachments/assets/a8d1a7a4-dfbb-465c-8174-c8f51d80a51e" />
ncorrect usernames and passwords
<img width="1920" height="1020" alt="Damn Vulnerable Web App (DVWA) v1 0 7 __ Vulnerability_ Brute Force - Personal - Microsoft​ Edge 03_11_2026 14_08_32" src="https://github.com/user-attachments/assets/50c445b9-9c1f-46d2-a0ea-dc901c601ed3" />

## STEP - 4 Launch Burp suite

Go to the Proxy tab in Burp Suite, click on the Intercept sub-tab, and make sure interception is turned on before you load your DVWA page so it can catch the web traffic.

