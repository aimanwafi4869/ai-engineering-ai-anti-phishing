# AI Anti-Phishing
> AI anti-phishing system real-time inspects network traffic and blocks dangerous web requests to safeguard users and organizations from malicious sites and credential theft.

## Problem Statement
Modern security teams and enterprise users face a rapidly escalating volume of sophisticated phishing attacks that easily bypass static blacklists and traditional domain filters. Existing rule-based solutions fail to adapt to zero-day malicious domains and dynamic URL obfuscation techniques created by automated cyber threats. AI engineering is the ideal solution because lightweight machine learning models can dynamically analyze context, payload structures, and linguistic cues in real time at the proxy layer to intercept novel threats before users expose sensitive credentials.

## Evidence of the Problem
- Phishing as the Primary Breach Vector: Phishing and social engineering account for 62% of corporate breaches involving the human element, with a single phishing-initiated data breach costing organizations an average of $4.8 million (Source: IBM Cost of a Data Breach Report / Verizon Data Breach Investigations Report). (SafeToOpen Research. (2026, July 5). Phishing statistics 2026: The key numbers, sourced. SafeToOpen. Safetoopen.Com. https://safetoopen.com/en/resources/phishing-statistics-2026/)

- Inefficacy of Static Blocklists Against Rapid Takedowns: Over 1.06 million new phishing attacks were recorded in Q2 2026 alone, with modern malicious lookalike domains staying live for an average of just 12 hours—a lifecycle window far too short for traditional database blocklists to index and update (Source: Anti-Phishing Working Group (APWG) / BlackBerry Global Threat Intelligence Report). (SecureSlate Team. (2026, October 5). Phishing statistics 2026: Sourced numbers and what they mean for your controls. SecureSlate. https://getsecureslate.com/blog/phishing-statistics)

## Initial Related Work / Existing Approaches
- Blacklist-Based Domain Filtering (e.g., Google Safe Browsing / PhishTank API): Relies on centralized databases of known malicious URLs to block traffic.
-- Key Limitation: High false-negative rate against zero-day phishing sites because newly generated malicious domains stay active for hours before being indexed and reported.
(Akshaya Arun. (2026). Next Generation of Phishing Attacks using AI powered Browsers. 2406.12547V1. Scribd. https://www.scribd.com/document/940515654/2406-12547v1)
- Client-Side Browser Extension Machine Learning Models: Runs lightweight classification models directly within the user's browser extension to evaluate page DOM elements and URLs.
Key Limitation: Highly vulnerable to client-side bypasses (e.g., attackers disabling scripts), introduces browser performance latency, and fails to inspect encrypted raw socket traffic prior to full page rendering.
(Wenhao Li. (December 2024). A State-of-the-art Review on Phishing Website Detection Techniques. ResearchGate. https://www.researchgate.net/publication/386849281_A_State-of-the-art_Review_on_Phishing_Website_Detection_Techniques)
- Email Security Gateway NLP Parsers (e.g., SpamAssassin / Mail Inspector Rules): Analyzes incoming email headers and body text for deceptive phrases and phishing markers before delivered to the inbox.
Key Limitation: Ineffective against non-email attack vectors such as direct link sharing, QR-code phishing (Quishing), and messaging app exploits that bypass email gateways entirely.
(CaptainDNS. (2026, February 16). CaptainDNS. CaptainDNS. https://www.captaindns.com/en/blog/phishing-trends-2025-2026-statistics)

## Project Objectives
- O1: To develop and implement a proxy server capable of real-time HTTP/HTTPS traffic interception and bi-directional payload inspection.
- O2: To integrate an AI models that can evaluates incoming requests against context-aware, and structural threat patterns to identify phishing sites.

## Target Users
- Enterprise Security Operations Center (SOC) Teams & Network Administrators
IT administrators who require centralized network-level inline interception to enforce phishing defenses without installing agent software across managed endpoints.

## Data Sources
- Web page Phishing Detection Dataset
https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset
## Weekly Progress
| Week | Focus | Deliverable | Status |
|------|-------|-------------|--------|
| W1 | System map + project scope | README + docs | ✅ |
