# FUTURE_CS_03 - API Security Risk Analysis

## Overview
This report analyzes the JSONPlaceholder public test API to 
identify common API security risks, following the OWASP API 
Security Top 10 framework. This is a read-only, ethical security 
assessment — no exploitation or destructive testing was performed.

## API Tested
JSONPlaceholder (https://jsonplaceholder.typicode.com) — a public 
test/demo API intended for learning and testing purposes.

## Scope
- Read-only requests only (GET)
- No exploitation, bypass attempts, or flooding/DoS testing
- Testing limited to public, demo-designated endpoints

## Findings Summary
- **Broken Authorization (High)** — Any user's data accessible by 
  changing the ID in the URL, with no ownership verification
- **Excessive Data Exposure (High)** — /users endpoint returns full 
  personal details, including GPS coordinates, without authentication
- **Missing Rate Limiting (Medium)** — Repeated rapid requests are 
  never throttled or blocked
- **Poor Input Validation (Low)** — Invalid IDs return empty 
  responses instead of clear error messages

Full details, business impact, and remediation steps are in the 
attached report.

## Tools Used
- Postman (API request testing and inspection)
- Browser (initial endpoint exploration)
- Canva (report design)

## Methodology
1. Reviewed API documentation to understand available endpoints
2. Tested endpoints using Postman, inspecting responses and headers
3. Tested authorization boundaries by varying resource IDs
4. Tested rate limiting by sending repeated rapid requests
5. Tested input validation with malformed/invalid input
6. Classified findings by risk severity and documented remediation

## Files
- [report.pdf](./report.pdf) — Full API Security Risk Analysis Report
- Screenshots — Postman request/response evidence for each finding
