---
title: Application Security
permalink: /catalog/as/
variant: markdown
description: ""
---
# Application Security

Controls to prevent application vulnerabilities caused by insecure coding.

| Controls |
| ---- |
| [AS-1: Input Validation](/catalog/as#as-1) |
| [AS-2: Parametrised Interfaces](/catalog/as#as-2) |
| [AS-3: Output Sanitisation](/catalog/as#as-3) |
| [AS-4: Authentication Mechanism Rate-Limiting](/catalog/as#as-4) |
| [AS-5: Password Requirements](/catalog/as#as-5) |
| [AS-6: Password Salting and Hashing](/catalog/as#as-6) |
| [AS-7: Access Control Check Enforcement](/catalog/as#as-7) |
| [AS-8: Application Secrets Management](/catalog/as#as-8) |
| [AS-9: Content Security Policy (CSP)](/catalog/as#as-9) |
| [AS-10: HTTP Strict Transport Security (HSTS)](/catalog/as#as-10) |
| [AS-11: Session Management](/catalog/as#as-11) |


<a id="as-1"></a>
## AS-1: Input Validation 

### Control Statement

Validate all application inputs to ensure that they match the expected type, structure, or format.

### Control Recommendations

Strictly validating inputs against a comprehensive schema prevents injection attacks caused by inserting special characters or content that would cause the application to perform incorrect operations.

### Risk Statement

Without input validation, there's a heightened risk of injection attacks, data manipulation, or system crashes due to unexpected input, potentially leading to unauthorised access or disruption of services.

<a id="as-2"></a>
## AS-2: Parametrised Interfaces 

### Control Statement

Use parametrised interfaces for database queries or system commands.

### Control Recommendations

Parametrised interfaces such Object-Relational Mapping (ORM) libraries ensure that parameters used in database queries or system commands are properly sanitised and prevent injection attacks.

### Risk Statement

Failure to use parameterised interfaces increases the vulnerability to SQL injection or command injection attacks, posing a significant risk of unauthorised access, data manipulation, or even potential system compromise.

<a id="as-3"></a>
## AS-3: Output Sanitisation 

### Control Statement

Sanitise all application outputs that will be used to render a HTML document.

### Control Recommendations

Any application outputs that are returned to the requester and used to render a HTML document can lead to cross-site scripting (XSS) attacks if they contain special characters that change the rendering of the HTML document by the browser.

### Risk Statement

Lack of sanitisation for application outputs used in rendering HTML documents exposes the system to the risk of cross-site scripting (XSS) attacks, allowing malicious code execution in users' browsers.

<a id="as-4"></a>
## AS-4: Authentication Mechanism Rate-Limiting 

### Control Statement

Apply rate-limiting on all authentication mechanisms to deter brute-force attacks.

### Control Recommendations

Consider rate-limiting to a maximum of 3 consecutive failed authentication attempts within 15 minutes. Time delays between log-on attempts reduce the risk of successful brute-forcing attacks. Bot mitigation tools such as CAPTCHA can further reduce this risk.

### Risk Statement

Without rate-limiting, there's an increased risk of unauthorised access as attackers may exploit weak credentials through repeated login attempts.

<a id="as-5"></a>
## AS-5: Password Requirements 

### Control Statement

Where SSO or passwordless is not supported, verify that user-defined passwords are at least [as-5_prm_1] characters in length and [as-5_prm_2].

### Control Recommendations

Latest NIST [SP 800-63B](https://doi.org/10.6028/NIST.SP.800-63b) guidelines found that password length is a primary factor in determining the strength of a password while composition and complexity rules provide marginal security benefits.

### Risk Statement

Short or commonly used passwords increase the vulnerability to unauthorised access, potentially leading to compromised accounts and unauthorised activities on the system.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| as-5_prm_1 | number of characters | The minimum length of a password. |
| as-5_prm_2 | policy | The password policy. |

<a id="as-6"></a>
## AS-6: Password Salting and Hashing

### Control Statement

Store passwords as salted hashes using a password hashing scheme that is resistant to offline attacks such as those described in NIST [SP 800-63b](https://doi.org/10.6028/NIST.SP.800-63b). The salt should be:
 * Generated using a cryptographically secure pseudo-random number generator in accordance with industry standards;
 * At least 32 bits long; and
 * Randomly generated for each account.


### Control Recommendations

Refer to NIST [SP 800-90Ar1](https://doi.org/10.6028/NIST.SP.800-90Ar1) for suitable pseudo-random number generators. Refer to NIST [SP 800-63b](https://doi.org/10.6028/NIST.SP.800-63b) Memorized Secret Verifiers section for suitable hashing schemes, including Argon2, scrypt, and PBKDF2. For application source code, use a cryptographically secure pseudo-random number generator function instead of an insecure one, such as crypto.randomBytes instead of Math.random in Node.js and java.security.SecureRandom.nextBytes instead of java.util.Random in Java.

### Risk Statement

Without salting and hashing, in case of a data breach, exposed passwords can be easily extracted, leading to potential compromise of user accounts and sensitive information.

<a id="as-7"></a>
## AS-7: Access Control Check Enforcement

### Control Statement

Perform access control checks on all authenticated requests.

### Control Recommendations

Utilise authorisation filters or middleware to force all authenticated requests to undergo access control checks.

### Risk Statement

Failure to perform access control checks on authenticated requests increases the risk of unauthorised access to sensitive data or functionalities, potentially leading to data breaches and misuse of system resources.

<a id="as-8"></a>
## AS-8: Application Secrets Management

### Control Statement

Encrypt and store application secrets in a secret management solution with appropriate access controls and do not hard-code secrets in source code.

### Control Recommendations

Secret management solutions include cloud solutions like AWS Secrets Manager and Azure Key Vault as well as cloud-agnostic solutions like HashiCorp Vault and CyberArk Conjur.

### Risk Statement

Exposure of sensitive information and unauthorised access to system credentials may occur if application secrets are stored without encryption or if hard-coded in source code.

<a id="as-9"></a>
## AS-9: Content Security Policy (CSP)

### Control Statement

Set minimally permissive CSP response headers to mitigate cross-site scripting attacks.

### Control Recommendations

Utilise the relevant fetch directives such as `default-src`, `script-src`, `style-src`, `connect-src`, `img-src`, `media-src` and `object-src` to prevent loading of scripts from malicious sources. Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

### Risk Statement

Without minimally permissive Content Security Policy (CSP) headers, the risk of cross-site scripting attacks, leading to unauthorised script execution and potential data theft, is increased.

<a id="as-10"></a>
## AS-10: HTTP Strict Transport Security (HSTS)

### Control Statement

Set HTTP Strict Transport Security (HSTS) response headers with a maximum age value of at least 1 year (31536000 seconds) to mitigate protocol downgrade attacks.

### Control Recommendations

Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

### Risk Statement

Failure to implement HTTP Strict Transport Security (HSTS) with a sufficient maximum age may expose the system to protocol downgrade attacks, compromising the security of communication channels.

<a id="as-11"></a>
## AS-11: Session Management

### Control Statement

Require users to re-authenticate after their session exceeds [as-11_prm_1] hour(s) or terminate the session.

### Control Recommendations

NIST SP 800-63B recommends re-authentication once per 30 days for Authenticator Assurance Level 1, 12 hours or 30 minutes inactivity for Authenticator Assurance Level 2, and 12 hours or 15 minutes inactivity for Authenticator Assurance Level 3. In addition to time period, system can consider re-authentication when roles, authenticators or credentials change or when the execution of privileged functions occurs.

### Risk Statement

Not verifying a user regularly and at suitable checkpoints could allow someone who has access to the user's account to carry out unauthorised actions.



#### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| as-11_prm_1 | time period (hours) | The maximum time period in hours of a user's session. |