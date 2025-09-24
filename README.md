# On-Premise SOC Deployment with Incident Detection and Response

## Objective
This project involved designing and implementing a complete Security Operations Center in a virtualized environment to simulate real-world cyber attacks and build defensive capabilities. The lab enabled end-to-end security monitoring, from initial attack simulation to detection, investigation, and containment.

### Skills Learned
- SIEM deployment and configuration with Elastic Stack
- Endpoint Detection and Response (EDR) implementation
- Custom detection rule creation and threat hunting
- Incident response procedures and containment strategies
- Network segmentation and security architecture design
- Cyber kill chain analysis and mitigation

### Tools Used
- **Virtualization**: VMware vSphere/Workstation
- **SIEM**: Elastic Stack (Elasticsearch, Kibana)
- **EDR**: Elastic Defend with Fleet Server
- **C2 Framework**: Mythic C2 with Apollo agent
- **Ticketing**: osTicket for incident management
- **Monitoring**: Sysmon for Windows endpoint visibility

## Project Implementation

### Phase 1: Lab Architecture Design
*Ref 1: Network Diagram*
![Network Architecture](https://github.com/hameza123/On-Premise-SOC/blob/main/diagram-final-5.png)
**Description**: Designed a segmented network architecture with separate zones for defensive tools, attacker infrastructure, and target assets. The diagram shows VLAN segmentation, security zones, and communication paths between SIEM components, endpoints, and management interfaces.

### Phase 2: SOC Stack Deployment
*Ref 2: Elastic Stack Deployment*
![Elastic Deployment]
**Description**: Configured Elastic Stack components including Elasticsearch for log storage and Kibana for visualization. Shows the integration of Elastic Agents for endpoint monitoring and Fleet Server for centralized management.

### Phase 3: Attack Simulation (Red Team)
*Ref 3: Brute Force Attack Simulation*
![Brute Force Simulation](https://github.com/hameza123/On-Premise-SOC/blob/main/assh-alerts.png)
**Description**: Executed SSH and RDP brute-force attacks to gain initial access. The screenshot shows attack patterns and successful credential compromises that triggered our detection rules.

### Phase 4: Detection Engineering (Blue Team)
*Ref 4: Custom Detection Rules*
![Kibana Detection Rules](https://github.com/hameza123/On-Premise-SOC/blob/main/Rules.png)
**Description**: Authored and implemented custom detection rules in Kibana including:
- "6+ Failed RDP Logins in 5 Minutes" 
- "Suspicious Process: apollo.exe"
- "Connection to Known Malicious C2 IP"
- "Multiple Failed SSH Logins"

### Phase 5: Threat Hunting & Visualization
*Ref 5: Security Dashboards*
![Kibana Dashboards](https://github.com/hameza123/On-Premise-SOC/blob/main/Dashboard.png)
**Description**: Built comprehensive Kibana dashboards for real-time monitoring including "Failed SSH/RDP Logins Over Time" and "Suspicious Windows Activity" that provided visual indicators of the ongoing attack.

### Phase 6: Incident Response
*Ref 6: Incident Ticketing*
![osTicket Integration](https://github.com/hameza123/On-Premise-SOC/blob/main/ticket.png)
**Description**: Automated incident creation in osTicket showing how SIEM alerts automatically generated tickets for security team response, including host isolation commands executed through Elastic Defend.

## Key Achievements
- **Successfully detected** 100% of simulated attack vectors
- **Reduced mean time to detection** (MTTD) to under 5 minutes for critical alerts
- **Automated incident response** through SIEM-ticketing system integration
- **Contained threats** within 15 minutes of initial detection using EDR capabilities

This project provided hands-on experience in building enterprise-grade security operations capabilities and demonstrated practical skills in modern SOC technologies and methodologies.
