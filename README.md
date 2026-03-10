# Recon Lab: Interactive Reconnaissance Terminal Simulator

An interactive browser-based terminal simulator that teaches the reconnaissance phase of the cyber kill chain through guided, hands-on practice.

Built as a companion lab for the **"Kill Chain Decoded: The Reconnaissance Phase"** webinar at [Exploit3rs Cyber Security Academy](https://exploit3rs.ae).

![Python](https://img.shields.io/badge/Python-Flask-blue)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED)
![License](https://img.shields.io/badge/License-Proprietary-red)
![Difficulty](https://img.shields.io/badge/Difficulty-Beginner-brightgreen)

**Live Demo:** [http://16.25.12.51](http://16.25.12.51)

---

## Overview

Participants complete a 5-step reconnaissance chain against a fictional target, **NexGen Solutions**, a cloud security firm in Dubai that rushed a deployment. The lab uses a split-panel interface with guided task descriptions and an interactive terminal, where each step must be completed before the next unlocks.

---

## The 5-Step Recon Chain

| Step | Tool | Objective |
|------|------|-----------|
| 1 | `whois` | Gather organizational intelligence |
| 2 | `subfinder` | Enumerate subdomains and map attack surface |
| 3 | `nslookup` | Resolve DNS and map infrastructure |
| 4 | `nmap` | Scan ports and identify running services |
| 5 | `nuclei` | Detect vulnerabilities and CVEs |

---

## Features

- **Split-panel UI** with task descriptions and interactive terminal
- **Sequential progression** where tabs lock until the previous step is solved
- **Realistic output** with simulated command responses mirroring actual tool behavior
- **Secure flag delivery** via backend API only, never exposed in page source
- **Progress tracking** with a visual progress bar (0/5 to 5/5) and solved badges
- **Built-in commands** including `help`, `hint`, `status`, and `clear`
- **Mobile responsive** design across devices

---

## Tech Stack

- **Backend:** Python (Flask)
- **Frontend:** HTML, CSS, JavaScript
- **Containerization:** Docker
- **Deployment:** AWS ECR (`recon_lab_v1`)

---

## Quick Start

### Docker (Recommended)
```bash
docker build -t recon-lab .
docker run -p 80:80 recon-lab
```

Then open `http://localhost` in your browser.

### Local Development
```bash
cd app
pip install -r requirements.txt
python app.py
```

---

## MITRE ATT&CK Mapping

| Technique ID | Name |
|--------------|------|
| T1592 | Gather Victim Host Information |
| T1590 | Gather Victim Network Information |
| T1595 | Active Scanning |

---

## Project Structure
recon-lab/
├── app/
│   ├── app.py              # Flask backend + flag verification API
│   ├── templates/
│   │   └── index.html       # Terminal simulator UI
│   └── requirements.txt
├── solution/
│   └── WRITEUP.md           # Full step-by-step solution
├── IDEA.md                  # Challenge design document
├── USERFLOW.md              # User experience flow
├── README.md
└── Dockerfile


---

## Challenge Details

| Field | Value |
|-------|-------|
| Difficulty | Beginner |
| Points | 100 |
| Estimated Solve Time | Under 5 minutes |
| Port | 80 |
| Categories | Web, OSINT |

---

## Context

Developed for **Exploit3rs Cyber Security Academy** (Dubai, UAE) as part of the **Kill Chain Decoded** webinar series. This lab serves as an interactive, hands-on complement to the reconnaissance theory covered in the presentation.

---

## License

Proprietary. Exploit3rs Cyber Security Academy. All rights reserved.
