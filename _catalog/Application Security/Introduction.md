---
title: Introduction
permalink: /catalog/as/
variant: markdown
description: ""
third_nav_title: Application Security
---
# Application Security

Controls to prevent application vulnerabilities caused by insecure coding.


# AS-1: Input Validation <a name="as-1"></a>

## Control Statement

Validate all application inputs to ensure that they match the expected type, structure, or format.

## Control Recommendations

Strictly validating inputs against a comprehensive schema prevents injection attacks caused by inserting special characters or content that would cause the application to perform incorrect operations.

## Risk Statement

Without input validation, there's a heightened risk of injection attacks, data manipulation, or system crashes due to unexpected input, potentially leading to unauthorised access or disruption of services.

# AS-2: Parametrised Interfaces <a name="as-2"></a>

## Control Statement

Use parametrised interfaces for database queries or system commands.

## Control Recommendations

Parametrised interfaces such Object-Relational Mapping (ORM) libraries ensure that parameters used in database queries or system commands are properly sanitised and prevent injection attacks.

## Risk Statement

Failure to use parameterised interfaces increases the vulnerability to SQL injection or command injection attacks, posing a significant risk of unauthorised access, data manipulation, or even potential system compromise.

# AS-3: Output Sanitisation <a name="as-3"></a>

## Control Statement

Sanitise all application outputs that will be used to render a HTML document.

## Control Recommendations

Any application outputs that are returned to the requester and used to render a HTML document can lead to cross-site scripting (XSS) attacks if they contain special characters that change the rendering of the HTML document by the browser.

## Risk Statement

Lack of sanitisation for application outputs used in rendering HTML documents exposes the system to the risk of cross-site scripting (XSS) attacks, allowing malicious code execution in users' browsers.

# AS-4: Authentication Mechanism Rate-Limiting <a name="as-4"></a>

## Control Statement

Apply rate-limiting on all authentication mechanisms to deter brute-force attacks.

## Control Recommendations

Consider rate-limiting to a maximum of 3 consecutive failed authentication attempts within 15 minutes. Time delays between log-on attempts reduce the risk of successful brute-forcing attacks. Bot mitigation tools such as CAPTCHA can further reduce this risk.

## Risk Statement

Without rate-limiting, there's an increased risk of unauthorised access as attackers may exploit weak credentials through repeated login attempts.

# AS-5: Password Requirements <a name="as-5"></a>

## Control Statement

Where SSO or passwordless is not supported, verify that user-defined passwords are at least [as-5_prm_1] characters in length and [as-5_prm_2].

## Control Recommendations

Latest NIST [SP 800-63B](https://doi.org/10.6028/NIST.SP.800-63b) guidelines found that password length is a primary factor in determining the strength of a password while composition and complexity rules provide marginal security benefits.

## Risk Statement

Short or commonly used passwords increase the vulnerability to unauthorised access, potentially leading to compromised accounts and unauthorised activities on the system.



### Parameters

| ID | Type | Description |
| -- | ---- | ----------- |
| as-5_prm_1 | number of characters | The minimum length of a password. |
| as-5_prm_2 | policy | The password policy. |