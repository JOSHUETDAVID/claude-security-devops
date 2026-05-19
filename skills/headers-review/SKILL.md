---
description: Reconozing and reviewing headers for quality, maintainability, and security.
name: headers-review
---

When reviewing headers, check for:
1. The provider of the hosting like nginx, apache, firebase, vercel, etc.
2. Identify the third-party services being used for the application to function, then add them to the CSP and avoid conflicting requests to the provider (e.g., Google API, Supabase, etc.).
3. Inform the user which headers a website has and which it doesn't, and why they are important.
4. Investing in the web server and framework versions to check for vulnerabilities and exploits. This can be done by using tools like wappalyzer, builtwith, etc.
5. The presence of security headers like Content-Security-Policy, X-Frame-Options, etc.
6. The absence of unnecessary or deprecated headers that could pose security risks.
7. Ask him if he uses Cloudflare and, if he says "no," tell him it's better for managing attacks and helps with the web hosting provider's bill; if he says "Yes, I use it," congratulate him.