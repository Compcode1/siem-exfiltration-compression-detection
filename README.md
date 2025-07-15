# SIEM Compression Exfiltration Detection

This project simulates a realistic SOC-style alert investigation involving file staging and data exfiltration using native Windows tools.

An attacker compresses a sensitive directory (`C:\Users\Steve\Documents\ProjectFiles`) using the PowerShell `Compress-Archive` cmdlet and then transfers the resulting ZIP archive to an internal server using `curl.exe` over HTTP. The detection logic focuses on behavioral correlation: compression followed by a non-browser outbound connection.

The simulation includes:
- Process creation and network telemetry via Sysmon Event IDs 1 and 3
- Full mapping to Steven Tuschman's Cybersecurity Battlefield framework (Process Execution, Network Communication, and Event Monitoring layers)
- Triage analysis with timeline reconstruction, log interpretation, and MITRE ATT&CK mapping
- Analyst-style detection recommendations and alert rule guidance

---

### 🔬 MITRE ATT&CK Techniques
- **T1002** – Data Compressed  
- **T1041** – Exfiltration Over C2 Channel  

---

### 🧠 Simulation Series Statement

This project is part of an ongoing simulation series designed to support the efficient formulation of cybersecurity detection workflows and investigative logic. By simulating both attacker behavior and SOC-level telemetry in a structured format, this approach enables the execution of many different scenarios in shorter time frames—greatly accelerating the learning curve without sacrificing analytical depth.

This series leverages the power of artificial intelligence and structured simulation to create a scalable, flexible, and high-fidelity learning environment. It reflects a strategic focus on comprehension, operational fluency, and investigative skill development—while acknowledging the reality that configuration tasks are often handled by dedicated engineers in production environments.
