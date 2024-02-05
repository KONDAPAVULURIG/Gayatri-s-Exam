Title: NGINX Configuration for Location-Based 404 and Security Headers

Description:

This repository contains NGINX configuration snippets for:

Location-based 404: Returns a 404 status code for any content ending with specific extensions (css, jpg, jpeg, js, json, png, mp4, pdf).
HTTP Security Headers: Adds essential security headers to responses, but only if not already set by the upstream server. Defaults to no headers if none are present upstream.
Features:

Customizable extension list for 404 handling.
Enhanced access log format for detailed request tracking.
Secure headers:
Strict-Transport-Security (HSTS) with Subdomain inclusion.
X-Content-Type-Options: nosniff to prevent MIME sniffing vulnerabilities.
X-XSS-Protection: 1; mode=block to help mitigate XSS attacks.
X-Frame-Options: DENY to prevent clickjacking.
Content-Security-Policy: frame-ancestors 'none' to restrict framing.
Access-Control-Allow-Credentials: TRUE for cross-origin requests with credentials.
Installation:

Clone the repository: git clone https://github.com/your-username/nginx-config.git
Copy the configuration snippets to your NGINX configuration files.
Adjust paths and options as needed.
Restart NGINX.
