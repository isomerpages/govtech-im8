---
title: Performance and Reliability
permalink: /control-catalog/dss/pr/
variant: markdown
description: ""
third_nav_title: Digital Service Standards
---
Controls to ensure consistent system performance and dependability.

| Controls                                                                 |
| ------------------------------------------------------------------------ |
| [PR-1: Digital Service Review](#pr-1-digital-service-review)             |
| [PR-2: Digital Service Registration](#pr-2-digital-service-registration) |
| [PR-3: Digital Service Availability](#pr-3-digital-service-availability) |
| [PR-4: Notify of Scheduled Downtime](#pr-4-notify-of-scheduled-downtime) |
| [PR-5: Manage Broken Links](#pr-5-manage-broken-links)                   |
| [PR-6: Browser Compatibility](#pr-6-browser-compatibility)               |
| [PR-7: Optimise Load Times](#pr-7-optimise-load-times)                   |

## PR-1: Digital Service Review

**Group:** Performance and Reliability

### Control Statement

Review digital services every [ insert: param, pr-1_prm_1 ] day(s). Shut down services that are no longer needed or fail to meet their intended objectives.

### Control Recommendations

Review factors such as relevance, importance and usage rates of the service.Ensure that there is a process to review each digital service such as websites and mobile apps periodically.

Review factors such as relevance, importance and usage rates of the service.

### Rationale

Services that are not effective incur unnecessary costs for the organisation.

### Parameters

| ID         | Type                     | Description                                                                      |
| ---------- | ------------------------ | -------------------------------------------------------------------------------- |
| pr-1_prm_1 | time period (days) (int) | The time period in days within which a digital service review must be conducted. |

## PR-2: Digital Service Registration

**Group:** Performance and Reliability

### Control Statement

Register and implement WOGAA on all public facing digital services.

### Control Recommendations

Registration and implementation includes:

1. Registration of all public facing digital services

2. Implementation of WOGAA tracking code

3. Enabling Sentiments

Refer to Setup Guide for details.

Only registration is required for SaaS and COTS products that do not allow customisation and the implementation of the tracking code and sentiments.

### Rationale

A centralised registry and tracking of digital services across Whole-of-Government facilitates central oversight and benchmarking of digital services. WOGAA implementation enables analytics data and feedback collection that is essential to identifying issues and opportunities for continuous improvement of the digital service.

## PR-3: Digital Service Availability

**Group:** Performance and Reliability

### Control Statement

Make digital services available to users 24/7.

Clearly communicate the operational hours if a service cannot be available 24/7.

### Control Recommendations

Do not limit the availability of services to specific hours unless justified by operational or business requirements.

### Rationale

End users expect to have access to digital channels anytime excluding planned and unplanned downtime.

## PR-4: Notify of Scheduled Downtime

**Group:** Performance and Reliability

### Control Statement

Provide notice of scheduled downtime at least [ insert: param, pr-4_prm_1 ] day(s) in advance.

### Control Recommendations

Clearly communicate scheduled downtime using methods like maintenance banners and in-app notifications. Useful information include date, time, duration, and reason for the downtime (if applicable), feature(s) or section(s) of the digital service that will be unavailable (if applicable).

Balance between providing enough lead time, and ensuring that end users can remember when the maintenance will happen.

### Rationale

Awareness of scheduled downtime minimises disruption to users by allowing them to plan around it.

### Parameters

| ID         | Type                     | Description                                                     |
| ---------- | ------------------------ | --------------------------------------------------------------- |
| pr-4_prm_1 | time period (days) (int) | The time period in days to provide notice of schedule downtime. |

## PR-5: Manage Broken Links

**Group:** Performance and Reliability

### Control Statement

Establish processes to detect broken links, and address them within [ insert: param, pr-5_prm_1 ] day(s) from detection.

### Control Recommendations

Use automated tools like WOGAA&#39;s broken link scanner to regularly scan for broken links. This applies to both internal and external links.

### Rationale

Broken links affect content delivery and prevent end users from completing tasks. Digital services with many broken links are perceived as untrustworthy and unreliable.

### Parameters

| ID         | Type                     | Description                                      |
| ---------- | ------------------------ | ------------------------------------------------ |
| pr-5_prm_1 | time period (days) (int) | The time period in days to address broken links. |

## PR-6: Browser Compatibility

**Group:** Performance and Reliability

### Control Statement

Ensure web-based services are compatible with the latest major versions of at least [ insert: param, pr-6_prm_1 ] widely used web browsers, based on usage statistics.

### Control Recommendations

Regularly test your service on the latest two major versions of popular browsers such as Chrome, Firefox, Safari, and Edge. Get browser usage data from analytics tools.

Consider using browser compatibility tools like BrowserStack or LambdaTest to automate and expand testing across multiple environments.

### Rationale

Browser incompatibility can cause layout bugs and other functional issues.

### Parameters

| ID         | Type                     | Description                 |
| ---------- | ------------------------ | --------------------------- |
| pr-6_prm_1 | number of browsers (int) | The number of web browsers. |

## PR-7: Optimise Load Times

**Group:** Performance and Reliability

### Control Statement

Ensure that page load time of web-based services is [ insert: param, pr-7_prm_1 ] second(s) or less.

### Control Recommendations

Track or regularly test and optimise performance using tools like WOGAA and Google PageSpeed Insights.

### Rationale

Long page load times frustrate end users and lead to longer transaction times and increased abandonment rate.

### Parameters

| ID         | Type                        | Description                                     |
| ---------- | --------------------------- | ----------------------------------------------- |
| pr-7_prm_1 | time period (seconds) (int) | The time period in seconds for page load times. |