# Phishing_detection
# SecURL 🔒  
**Real-Time Detection of Phishing Sites via Transparent Multi-Stage Analysis and OCR-Based Integrity Check**

A capstone project designed to tackle phishing threats through a secure, interpretable, and real-time web-based detection pipeline using hybrid structural + visual signals.

---

## 📌 Overview

**SecURL** is a real-time phishing detection system built to address limitations in traditional blacklists and opaque machine learning models. It implements a two-phase detection architecture:

- **Phase 1** — Structural and contextual checks using domain tokens, HTML title parsing, SSL certificate analysis, and favicon hashing.
- **Phase 2** — Visual verification using headless browser rendering, OCR via Google Vision API, and TF-IDF keyword validation.
---

## 🛠 Features

- Detects zero-day phishing websites
- Transparent decision-making with interpretable logic
- Visual-semantic branding verification (OCR + TF-IDF)
- Secure webpage rendering in isolated VM environment
- Defenses against shared infrastructure, cloaking, and SSL spoofing
- Lightweight web UI for real-time analysis

---

## 🔧 Technology Stack

| Component               | Technology / Tool                      |
|------------------------|----------------------------------------|
| Web Server             | `Flask` (Python)                       |
| Frontend               | `HTML`, `CSS`, `JavaScript`           |
| Headless Rendering     | `Playwright` (Chromium)                |
| OCR Engine             | `Google Cloud Vision API`              |
| HTML Parsing           | `BeautifulSoup`                        |
| SSL Cert Verification  | `ssl`, `socket` (Python stdlib)        |
| Domain Parsing         | `tldextract`                           |
| TF-IDF Analysis        | `Scikit-learn`                         |
| Search Verification    | `Google Custom Search API`             |
| Sandbox Environment    | `Linux Mint VM`                        |

---

## 🚀 Getting Started

> Ensure you're running on a system with Python 3.8+ and a virtualization environment (e.g., VirtualBox or VMware).

### 1. Clone the repository
```bash
git clone https://github.com/Natashajha1/Phishing_detection.git

python3 -m venv venv
source venv/bin/activate

# Google Custom Search
export GOOGLE_API_KEY='your_api_key_here'
export SEARCH_ENGINE_ID="your_search_engine_id"

# Google Vision API
export GOOGLE_APPLICATION_CREDENTIALS='path_to_your_gcp_credentials.json'

(Optional but recommended) Set up Linux Mint Virtual Machine
Use VirtualBox/VMware to isolate the browser rendering process. This increases security against drive-by-downloads and cloaked phishing pages.


