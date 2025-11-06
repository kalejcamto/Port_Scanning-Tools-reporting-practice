# Port_Scanning-Tools-reporting-practice

Objective: Write a one-page report to your manager describing some port-scanning tools that might be useful to your company.

Description: Alexander Rocco Corporation, which has hired you as a security tester, asked you to research any new tools that might help you perform your duties. It has been noted that some open-source tools your company is using lack simplicity and clarity or don't meet the company's expectations. Your manager, Gloria Petrelli, has asked you to research new or improved products on the market.

Based on this information, write a one-page report for Ms. Petrelli describing some port-scanning tools that might be useful to your company. The report should include available commercial tools and their costs.

# Automated External Attack Surface Validation & Control Gap Analysis

**Repository Status:** Complete (Scanning, Data Wrangling, Risk Reporting, Remediation Planning)

---

## 💡 Executive Summary

This project demonstrates a programmatic approach to **Continuous Control Monitoring (CCM)** by validating an organization's external security posture. It addresses the critical operational risk of **asset drift** and unauthorized service exposure by automating the discovery of internet-facing vulnerabilities.

The solution uses **Nmap** integrated with custom **Python scripting** to transform raw scan data into structured, actionable **Risk Reports**, enabling immediate detection of security control failures and ensuring audit readiness for network boundaries.

**Key Governance/Risk Skills Demonstrated:**
* **Continuous Control Monitoring (CCM)**
* **Risk Reporting** and **Prioritization**
* **Data Wrangling** for security telemetry
* **Asset Visibility** and **Attack Surface Management**

---

## Project Scenario & Goal

**Scenario:** Conduct a simulated external audit to verify a critical **Preventative Control** (PC-05: Deny all public access to high-risk ports across the internet-facing IP inventory.

**Goal:** Provide automated, repeatable proof that the external network security controls (e.g., firewall, AWS Security Groups) are effectively enforced, and reduce time-to-discovery of unauthorized open ports from weeks to minutes.

---

## 📂 Project Phases & Navigation

The project follows a structured process to convert raw technical data into meaningful risk insights:

| Folder | Phase | Goal/Focus |
| :--- | :--- | :--- |
| **1 Automation_Engine** | **Scanning & Collection** | Contains the core `nmap` configuration and **Python/Bash scripts** used to execute timed scans against target IP ranges (Input). |
| **2 Data_Wrangling** | **Data Structuring** | Scripts dedicated to parsing the Nmap XML output, cleaning the data, and transforming it into structured CSV/JSON, ready for analysis. |
| **3_Risk_Analysis_and_Reporting** | **Insight Generation** | Contains the final **Risk Report Template** and scoring logic. Categorizes findings into Risk Levels (Critical, High, Medium) based on port, service, and protocol discovered. |
| **4_Remediation_Plan_Example** | **Mitigation & Closure** | Simple documentation detailing suggested mitigation steps (immediate removal of public Security Group rules) and the process for validating remediation closure. |

---

## Key Technical Details

* **Primary Tool:** Nmap (for port and service discovery)
* **Language:** Python 3 (for automation and data wrangling)
* **Key Output:** Structured CSV/JSON file with identified open ports mapped to a calculated **Risk Score**.
## **Internal Research Report: Recommended Port Scanning Tools**

----

**To:** Gloria Petrelli, Manager, IT Department
**From:** Security Tester
**Date:** November 3, 2025
**Subject:** Analysis of Port Scanning Tools for Enhanced Network Visibility and Simplicity

***

### **Executive Summary**

This report addresses the need for updated port scanning tools that offer improved clarity, simplicity, and efficiency compared to our current open-source solutions. After reviewing the market, I recommend a combination of highly respected **Open-Source** (for foundational auditing) and **Commercial** (for advanced reporting and simplicity) tools. These tools will significantly enhance our ability to map the Alexander Rocco Corporation network topology and quickly identify open service ports and potential vulnerabilities, streamlining our pentesting workflow.

---

### **Recommended Tool Analysis**

#### **1. Foundational Standard (Open Source): Nmap (Network Mapper)**

While we currently use open-source tools, **Nmap** remains the industry standard and must be utilized as the baseline for all internal testing.

* **Primary Benefit:** Unmatched flexibility, raw power, and an extensive library of scripts (**Nmap Scripting Engine - NSE**) capable of service version detection, vulnerability checks, and advanced scanning techniques.
* **Recommendation:** Use the graphical frontend **Zenmap** to improve simplicity and clarity for new users, addressing the current complexity concerns.
* **Cost:** **Free** (Open-Source).

#### **2. Commercial Recommendation for Simplicity & Reporting: Tenable Nessus Professional**

For a significant upgrade in reporting, ease of use, and comprehensive vulnerability detection, **Nessus** is the leading commercial solution.

* **Primary Benefit:** Nessus moves beyond simple port scanning to full, authenticated vulnerability assessment. It automatically identifies active services, checks them against a massive database of known vulnerabilities (CVEs), and provides **clear, prioritized remediation steps**. This drastically reduces manual analysis time.
* **Simplicity & Clarity:** Offers a clean GUI and generates highly professional, actionable reports suitable for management and technical teams alike.
* **Estimated Cost (Nessus Professional):** Approximately **$2,990 to $5,990 USD annually**, depending on the number of scanners/assets.

#### **3. Commercial Recommendation for Enterprise Asset Management: Qualys Cloud Platform**

For large-scale, continuous asset discovery and management across the entire corporation, the **Qualys** platform provides a robust, integrated solution.

* **Primary Benefit:** Qualys offers **continuous monitoring** and asset inventory, integrating port scanning and vulnerability data into a centralized, cloud-based dashboard. It's designed for **large enterprises** like Alexander Rocco Corporation.
* **Simplicity & Clarity:** Excellent reporting, risk prioritization, and compliance mapping (useful for PCI DSS checks on our hotel/restaurant systems).
* **Estimated Cost (Vulnerability Management Module):** Pricing is typically **subscription-based and varies widely by the number of IPs/assets**, but often starts in the range of **$15,000 USD+ annually** for an enterprise environment.

---

### **Conclusion and Next Steps**

| Tool | Type | Key Advantage | Recommended Use | Estimated Cost |
| :--- | :--- | :--- | :--- | :--- |
| **Nmap/Zenmap** | Open Source | Foundational data, raw flexibility, and zero cost. | Baseline network discovery and specialized checks. | **Free** |
| **Nessus Professional** | Commercial | High simplicity, prioritized vulnerability reporting, and ease of use. | Detailed, authenticated vulnerability assessments. | **~$3,000 - $6,000 USD/yr** |
| **Qualys** | Commercial | Enterprise-scale, continuous asset inventory, and compliance. | Ongoing, large-scale vulnerability and asset management. | **$15,000+ USD/yr (Enterprise)** |

I recommend we initially allocate budget for a **Nessus Professional** license. This investment will provide an immediate and significant improvement in the clarity and quality of our pentest reporting, directly addressing the concerns noted by the company. I await your approval to move forward with procurement.
