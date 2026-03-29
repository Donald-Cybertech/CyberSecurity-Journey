# Learning Log: HTTP/HTTPS Deep Dive (Fundamentals)
**Date:** March 27, 2026
**Platform:** TryHackMe
**Module:** HTTP in Detail

## 🎯 Objective
To understand the underlying protocols of the web, focusing on the request-response cycle, status codes, and the security implications of HTTP vs. HTTPS from a SOC Analyst perspective.

## 🛠️ Hands-on Tasks Completed
* **Request Manipulation:** Manually crafted `GET`, `POST`, `PUT`, and `DELETE` requests using a web emulator.
* **Header Analysis:** Inspected `User-Agent`, `Host`, and `Referer` headers to understand how clients identify themselves to servers.
* **Cookie Management:** Observed the `Set-Cookie` and `Cookie` workflow to understand session persistence in a stateless protocol.
* **Status Code Identification:** Analyzed server responses ($2xx$ Success, $3xx$ Redirection, $4xx$ Client Error, $5xx$ Server Error).

## 🔑 Key Concepts Learned

### 1. The Stateless Nature of HTTP
HTTP does not "remember" users. To provide a continuous experience (like staying logged in), servers use **Cookies**.
* **SOC Tip:** Monitoring for `Cookie` theft or session hijacking is a vital part of web security.

### 2. HTTP Methods (Verbs)
| Method | Purpose | Security Context |
| :--- | :--- | :--- |
| **GET** | Retrieve data | Often logged; sensitive info should never be in the URL (Query String). |
| **POST** | Submit data | Used for logins/forms; data is in the body, making it slightly more 'hidden' than GET. |
| **PUT/PATCH** | Update data | Unauthorized PUT requests can lead to web defacement. |
| **DELETE** | Remove data | High-risk; should be strictly restricted via permissions. |

### 3. HTTPS & TLS
HTTPS provides **Encryption, Integrity, and Authentication**. Without the "S", data is sent in plaintext, vulnerable to "Man-in-the-Middle" (MITM) attacks.

## 🏁 Results
* Successfully captured the flag: `THM{HTTP_REQUEST_MASTER}`
* Achieved 100% completion of the "HTTP in Detail" module.

📫 **Connect with me:** [(https://www.linkedin.com/in/terna-angwe/)]

