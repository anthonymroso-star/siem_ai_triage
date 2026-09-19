# Real-Time SIEM Data Engineering, Automated AI Triage & Analyst Update Console (PoC)
An automated security assistant built with **Python** and **Pandas** that monitors live server alerts, packages them, and uses a local AI model to instantly analyze threats so security teams can investigate and respond to attacks faster.

> **Compliance & Data Sanitization Note:** Where applicable, files, scripts, logs, IP addresses, hostnames, and architecture identities within this repository have been sanitized and anonymized in alignment with relevant security frameworks and responsible-disclosure guidelines.

## Lab Architecture Overview
* **Data Origin Environment:** Ubuntu Production Container Node (Simulating a live corporate server stack pushing logs via HTTP POST).
* **Data Ingress Gateway:** Windows Analyst Laptop listening locally on Port 8080.
* **Local AI Infrastructure:** Ollama Host Machine executing an optimized registry string of `llama3.2:3b` on Port 11434.
* **Persistent Archival Databases:** Self-contained line-delimited Python JSON log streams (`.jsonl`) and an appended Pandas-generated CSV Analyst Triage Ledger.

## Key Skills Demonstrated

| Core Capability | Technical Implementation & Approach |
| :--- | :--- |
| **Pipeline Engineering** | Programmed a HTTP listener on Port 8080, and enforcing a 2GB RAM cap and 50MB file block rotation rules. |
| **Pandas Data Structuring**  | Re-architected storage pools from a CSV table model to a, line-delimited JSON stream eliminating character-collision data truncation. |
| **OS Interoperability** | Implemented managed shared read operations using file stream handlers, bypassing Windows permission locks. |
| **Schema Normalization** | Developed an on-the-fly dictionary pre-processor to unzip JSON keys into flat vertical data lines. |
| **Token Optimization** | Configured API request parameters to enforce hard output token clipping constraints, preventing remote server generation bottlenecks. |
| **Interactive Braking** | Leveraged Pythyon foreground execution to gracefully freeze ingestion during analyst manual note entry cycles. |
| **Data Enrichment** | Engineered Python dictionary unpacking to bind human commentary to raw security logs. |
| **OPSEC Compliance** | Implemented zero-trace execution wiping parameters to keep corporate telemetry out of public source tracking. |

## 📁 Repository Contents
* `/notebooks`: Holds the core operational script files (`local_edr_dataengine.ipynb` and `local_edr_ai_analysis.ipynb`).
* `/samples`: Scrubbed, anonymized data log entries and triage ledger snapshots.
* `/images`: Holds high-contrast terminal console outputs and AI forensic execution visuals.


## Featured Project Walkthroughs
1. **[Data Ingestion: Live Streaming JSON Log Telemetry ](./notebooks/local_edr_dataengine.ipynb)**
2. **[AI Forensic Analysis: Automated Response Assistance](./notebooks/local_edr_ai_analysis.ipynb)**
3. **[Sample Data Ingestion Payload: Scrubbed Live JSON String Structure](./samples/wzuh_siem_logs_sample.json)**

## Active Milestones
* [Phase 2A Implementation: Integrating Automated Model Switching Matrix with gemma4]
* [Phase 2B Implementation: Deploying a Telemetry Severity Level Filter Threshold (Level 10+)]

