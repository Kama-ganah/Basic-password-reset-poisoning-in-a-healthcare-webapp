# Overview

As a penetration tester, I conducted a security assessment of a web application’s password reset functionality after identifying indicators of unsafe trust in client-controlled input. The engagement focused on evaluating how password reset links were generated and whether untrusted HTTP headers influenced sensitive workflows. By manipulating the Host header during the reset process, I was able to poison the reset link, capture another user’s reset token, and gain unauthorized access to the account.

# Steps Undertaken

Step 1: Assessed the password reset workflow to understand how reset links were generated and delivered to users.

Step 2: Intercepted and analyzed password reset requests to identify reliance on client-supplied headers.

Step 3: Manipulated the Host header to redirect the reset link to an attacker-controlled domain.

Step 4: Captured the leaked reset token and used it to reset the victim’s password and access the account.

# Conclusion

This assessment demonstrated how trusting unvalidated HTTP headers in sensitive authentication workflows can lead to full account compromise. The findings highlight the need for strict server-side URL generation and robust validation when handling password reset mechanisms.
