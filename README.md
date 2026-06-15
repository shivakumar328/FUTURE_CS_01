# FUTURE_CS_01

## Vulnerability Assessment Report — AltoroMutual (demo.testfire.net)

**Internship:** Future Interns Cyber Security Internship 2026 — Task 1  
**Prepared by:** Shivakumar S   

---

## Website Tested

**Target:** [https://demo.testfire.net](https://demo.testfire.net) — AltoroMutual  
**Host / IP:** 65.61.137.117  
**Application:** AltoroJ — a deliberately vulnerable Java-based banking web application published by HCL Technologies Ltd. for security training and tool demonstration purposes.  
**Tech Stack:** Java JSP, Apache-Coyote/1.1 (Tomcat), ISO-8859-1

---

## Scope

### In-Scope — Passive / Read-Only Analysis Only
- Public-facing pages: Homepage, Login (`/login.jsp`), Feedback form (`/feedback.jsp`), Search (`/search.jsp`), Server Status (`/status_check.jsp`), Swagger UI (`/swagger/index.html`), CGI endpoint (`/cgi.exe`)
- Sensitive discovered resources: Admin file (`/admin/clients.xls`) discovered via passive ZAP spider crawl across 234 URLs

### Out-of-Scope
- Login bypass / credential attacks — not permitted
- Active SQL injection exploitation — read-only scope only
- Authenticated pages / dashboard — no login performed
- Denial-of-Service testing — prohibited
- Third-party services: petstore.swagger.io, online.swagger.io

> ⚠️ All testing was strictly passive and read-only. No active exploitation, authentication bypass, brute-force, or denial-of-service testing was performed at any point.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| OWASP ZAP 2.17.0 (Checkmarx) | Passive web scan — 11 passive alerts; spider crawled 234 URLs |
| PTK | Passive header and response analysis — 16 findings (10 unique) |
| Nmap 7.98 | Port & service enumeration |
| Browser DevTools (Chrome) | HTTP response header inspection, cookie flag analysis, page source review |
| Wappalyzer | Technology stack fingerprinting |
| Shodan | External host intelligence for 65.61.137.117 |
| Manual Source Code Review | Passive endpoint analysis, URL parameter inspection |

---

## Findings Summary

| Severity | Count |
|----------|-------|
| 🔴 High | 4 |
| 🟠 Medium | 4 |
| 🟡 Low | 4 |
| ℹ️ Informational | 3 |
| **Total** | **15** |



## Disclaimer

This assessment was conducted strictly in a passive, read-only capacity on demo.testfire.net — a publicly available, intentionally vulnerable demonstration application (AltoroJ) published by HCL Technologies Ltd. This report was produced as part of the **Future Interns Cyber Security Internship Task 1 (2026)** for educational and training purposes only. The analyst assumes no liability for actions taken or not taken based on the contents of this report.

---

## Task Reference

🔗 [Future Interns — Cyber Security Task 1 (2026)](https://futureinterns.com/cyber-security-task-1-2026/)  
🏢 [Future Interns LinkedIn](https://www.linkedin.com/company/future-interns)
