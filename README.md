# Endpoint Security at Scale

A technical architecture reference examining how large enterprises
secure tens of thousands of endpoints using the Microsoft security stack.

Live site: https://kenny-li-nyc.github.io/endpoint-security-at-scale

---

## What this is

This project maps the five-layer architecture that connects Windows
and Azure platform controls, telemetry collection, detection and
analytics, AI-assisted investigation, and automated response into a
coherent security pipeline.

It is written as a practitioner reference, not a product overview.
Each layer page covers the core technologies, the operational failure
modes at enterprise scale, and how that layer feeds the next one.

---

## The five layers

- **Layer 01: Windows & Azure Platform** — Identity and OS foundation.
  Active Directory, Entra ID, Group Policy, and privileged access controls.

- **Layer 02: Telemetry Collection** — Signal collection and routing.
  Windows Event Logs, Sysmon, Defender telemetry, PowerShell logging,
  and Microsoft Sentinel as the central aggregation platform.

- **Layer 03: Detection & Analytics** — KQL-based detection rules,
  MITRE ATT&CK mapping, Defender for Endpoint, Defender for Identity,
  and Defender XDR incident correlation.

- **Layer 04: Security Copilot** — AI-assisted investigation. Alert
  summarization, prompt-driven runbooks, multi-stage incident analysis,
  and the role of human judgment in the pipeline.

- **Layer 05: Automated Response** — Remediation execution via Sentinel
  Playbooks, Intune remediation scripts, Azure Automation, and
  ServiceNow integration.

The operations page ties all five layers together through an
end-to-end incident scenario and covers cascade failure modes,
continuous improvement practices, and operational metrics.

---

## How it was built

This project was researched, structured, and authored by Kenny Li.
It draws on enterprise Windows and Azure infrastructure experience
in financial services environments.

The site was built using Aider with Gemini Flash as the AI coding
assistant. Content research, architecture decisions, and writing were
AI-assisted throughout. The build process was an exercise in using
AI agents to accelerate learning and production in a complex domain.

---

## Technology

Plain HTML, CSS, and vanilla JavaScript. No frameworks. Hosted on
GitHub Pages.

---

Kenny Li · Senior Infrastructure Engineer · github.com/kenny-li-nyc
