# Automation-Project
SOC AUTOMATION PROJECT
BY: NYAMBURA NJOROGE

 

Description:
This project is based on a simulation and part of an everyday work experience of a SOC analyst. The project is used to set up Wazuh, Shuffle and TheHive for detection and mitigation of threats and attacks within the workplace. 
As a cybersecurity analyst and professional, it is imperative to ensure the safety of an organizations systems and objects, and using the right applications can assist in this. Given the rise in advanced attack methods that malicious actors are using, using technology and automating the process of threat detection allows for these threats to be addressed a quickly as possible. The rationale behind this project is to implement automation into the system and use these applications to detect, alert and address possible attacks inflicted into a company’s system and network as a means for faster response time and continuous safety of systems.

![SOC AUTOMATION drawio](https://github.com/user-attachments/assets/86f8ba6e-0fa2-40d9-9f5e-aaf491f1dd5c)

The diagram above shows the roadmap of how this automation intends to be configured and the role of each application.
1.	Windows 10 Client= The windows10 client is a host machine within the company that has the Wazuh Agent installed on it. The windows10 client may be the device that holds data used by company personnel and would be the main source of attack from malicious actors. The Wazuh Agent collects data and logs that are occurring within the client. This includes attempted log ins, increased requests, applications and data being accessed, increased outflow of data from the client etc. All the logs are collected by the Wazuh Agent.
2.	The Wazuh Manager is an application accessed via the internet and is in charge of accumulating all the logs from the Wazuh agent into an application. This application is accessed to review the logs. In the Wazuh Manager, it includes all the logs, the action as well as the data and time. The Wazuh Manager is a SIEM in this case that collects the logs, analyses them and if an anomaly or IOC is detected, it generates an alert that is send to shuffle for further investigation.
3.	Shuffle is a Security Orchestration Automation and Response (SOAR). It receives the alerts from Wazuh and investigates the IOC by using OSINT for further research to understand the possibility of a false positive, correlates alerts with external data sources and triggers response actions. Shuffle will send an email to the SOC analyst on its findings.
4.	TheHive is a Security Incident Response Platform (SIRP). This is a platform that helps SOC analyst to investigate alerts and possible threats. While Shuffle sends an email to the soc analyst, an email is not an essential incident response platform. Emails can get lost in the inbox and it does not provide a structured response on who is working on the incident and how. TheHive assists the soc analysts on providing a platform that has a ticketing system that shows tickets of alerts received and who it was allocated to. It is a central dashboard that allows the soc analysts within the organization to keep track of existing alerts, collaborate with one another and also add comments on each case being investigated.

Applications used:
1.	1 Windows 10 with Sysmon installed on it.
2.	1 Wazuh Server
3.	1 TheHive Server
