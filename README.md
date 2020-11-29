# Find the Bad: Knock Knock Audit
This lab contains malicious activity for you to identity that was captured in log files. It should only require the installation of Docker and Docker Compose. 

## Disclaimer
This lab is based on real data containing actual malicious indicators. If you attempt to do things such as find and run files, or visit network entities that occur in these logs, you do so at your own risk.

## Setup
1) Download and install [Docker](https://www.docker.com/get-started).
2) Download and install [Docker Compose](https://docs.docker.com/compose/install/) (On Windows Docker Compose should be bundled with the Docker installer, so this step shouldn't be required).
3) Download or clone this repository.
4) Open up a command prompt, make your way to this repository folder on your local machine and run `docker-compose up`.
5) When `docker-compose up` is finished bringing the containers up, open a browser and navigate to `http://localhost:5601` to access the Kibana instance.

## The Lab
This lab is built around using Kibana for identifying and investigating signs of a compromise. The `VT Hunting` Dashboard should provide you the information you need to get started.  It is considered intermediate, and so some assumptions are made about Kibana familiarity.  If you're looking for something more introductory, try these [labs instead](https://findthebad.com/tags/introductory/).

### Questions
1) What process caused the sigma rule hit?
2) What external file was attempted to be downloaded remotely and by what LOLBIN?
3) What process appears to have caused this activity and when was it run, by what user, on what computer?
4) Where did the script file come from?
5) How does it appear the attacker got access to this workstation?

### Useful Links
- [Sigma](https://github.com/Neo23x0/sigma)
- [Sysmon Event ID 3](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-3-network-connection)
- [Security Event ID 4625](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventID=4625)
- [LOLBAS](https://lolbas-project.github.io/#)
- [MITRE - ATT&CK - Masquerading: Rename System Utilities](https://attack.mitre.org/techniques/T1036/003/)
- [MITRE - ATT&CK - Brute Force: Password Guessing](https://attack.mitre.org/techniques/T1110/001/)

### Solution
Available [here](https://findthebad.com/knock-knock-audit//).
