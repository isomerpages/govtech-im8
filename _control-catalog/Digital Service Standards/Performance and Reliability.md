---
title: Performance and Reliability
permalink: /performance-and-reliability/
variant: markdown
description: ""
third_nav_title: Digital Service Standards
---
<p>Controls to ensure consistent system performance and dependability.</p>
<p>| Controls |</p>
<p>| ------------------------------------------------------------------------
|</p>
<p>| [PR-1: Digital Service Review](#pr-1-digital-service-review) |</p>
<p>| [PR-2: Digital Service Registration](#pr-2-digital-service-registration)
|</p>
<p>| [PR-3: Digital Service Availability](#pr-3-digital-service-availability)
|</p>
<p>| [PR-4: Notify of Scheduled Downtime](#pr-4-notify-of-scheduled-downtime)
|</p>
<p>| [PR-5: Manage Broken Links](#pr-5-manage-broken-links) |</p>
<p>| [PR-6: Browser Compatibility](#pr-6-browser-compatibility) |</p>
<p>| [PR-7: Optimise Load Times](#pr-7-optimise-load-times) |</p>
<p>## PR-1: Digital Service Review</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Review digital services every [ insert: param, pr-1_prm_1 ] day(s). Shut
down services that are no longer needed or fail to meet their intended
objectives.</p>
<p>### Control Recommendations</p>
<p>Review factors such as relevance, importance and usage rates of the service.Ensure
that there is a process to review each digital service such as websites
and mobile apps periodically.</p>
<p>Review factors such as relevance, importance and usage rates of the service.</p>
<p>### Rationale</p>
<p>Services that are not effective incur unnecessary costs for the organisation.</p>
<p>### Parameters</p>
<p>| ID | Type | Description |</p>
<p>| ---------- | ------------------------ | --------------------------------------------------------------------------------
|</p>
<p>| pr-1_prm_1 | time period (days) (int) | The time period in days within
which a digital service review must be conducted. |</p>
<p>## PR-2: Digital Service Registration</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Register and implement WOGAA on all public facing digital services.</p>
<p>### Control Recommendations</p>
<p>Registration and implementation includes:</p>
<p>1. Registration of all public facing digital services</p>
<p>2. Implementation of WOGAA tracking code</p>
<p>3. Enabling Sentiments</p>
<p>Refer to Setup Guide for details.</p>
<p>Only registration is required for SaaS and COTS products that do not allow
customisation and the implementation of the tracking code and sentiments.</p>
<p>### Rationale</p>
<p>A centralised registry and tracking of digital services across Whole-of-Government
facilitates central oversight and benchmarking of digital services. WOGAA
implementation enables analytics data and feedback collection that is essential
to identifying issues and opportunities for continuous improvement of the
digital service.</p>
<p>## PR-3: Digital Service Availability</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Make digital services available to users 24/7.</p>
<p>Clearly communicate the operational hours if a service cannot be available
24/7.</p>
<p>### Control Recommendations</p>
<p>Do not limit the availability of services to specific hours unless justified
by operational or business requirements.</p>
<p>### Rationale</p>
<p>End users expect to have access to digital channels anytime excluding
planned and unplanned downtime.</p>
<p>## PR-4: Notify of Scheduled Downtime</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Provide notice of scheduled downtime at least [ insert: param, pr-4_prm_1
] day(s) in advance.</p>
<p>### Control Recommendations</p>
<p>Clearly communicate scheduled downtime using methods like maintenance
banners and in-app notifications. Useful information include date, time,
duration, and reason for the downtime (if applicable), feature(s) or section(s)
of the digital service that will be unavailable (if applicable).</p>
<p>Balance between providing enough lead time, and ensuring that end users
can remember when the maintenance will happen.</p>
<p>### Rationale</p>
<p>Awareness of scheduled downtime minimises disruption to users by allowing
them to plan around it.</p>
<p>### Parameters</p>
<p>| ID | Type | Description |</p>
<p>| ---------- | ------------------------ | ---------------------------------------------------------------
|</p>
<p>| pr-4_prm_1 | time period (days) (int) | The time period in days to provide
notice of schedule downtime. |</p>
<p>## PR-5: Manage Broken Links</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Establish processes to detect broken links, and address them within [
insert: param, pr-5_prm_1 ] day(s) from detection.</p>
<p>### Control Recommendations</p>
<p>Use automated tools like WOGAA&amp;#39;s broken link scanner to regularly
scan for broken links. This applies to both internal and external links.</p>
<p>### Rationale</p>
<p>Broken links affect content delivery and prevent end users from completing
tasks. Digital services with many broken links are perceived as untrustworthy
and unreliable.</p>
<p>### Parameters</p>
<p>| ID | Type | Description |</p>
<p>| ---------- | ------------------------ | ------------------------------------------------
|</p>
<p>| pr-5_prm_1 | time period (days) (int) | The time period in days to address
broken links. |</p>
<p>## PR-6: Browser Compatibility</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Ensure web-based services are compatible with the latest major versions
of at least [ insert: param, pr-6_prm_1 ] widely used web browsers, based
on usage statistics.</p>
<p>### Control Recommendations</p>
<p>Regularly test your service on the latest two major versions of popular
browsers such as Chrome, Firefox, Safari, and Edge. Get browser usage data
from analytics tools.</p>
<p>Consider using browser compatibility tools like BrowserStack or LambdaTest
to automate and expand testing across multiple environments.</p>
<p>### Rationale</p>
<p>Browser incompatibility can cause layout bugs and other functional issues.</p>
<p>### Parameters</p>
<p>| ID | Type | Description |</p>
<p>| ---------- | ------------------------ | ---------------------------
|</p>
<p>| pr-6_prm_1 | number of browsers (int) | The number of web browsers.
|</p>
<p>## PR-7: Optimise Load Times</p>
<p><strong>Group:</strong> Performance and Reliability</p>
<p>### Control Statement</p>
<p>Ensure that page load time of web-based services is [ insert: param, pr-7_prm_1
] second(s) or less.</p>
<p>### Control Recommendations</p>
<p>Track or regularly test and optimise performance using tools like WOGAA
and Google PageSpeed Insights.</p>
<p>### Rationale</p>
<p>Long page load times frustrate end users and lead to longer transaction
times and increased abandonment rate.</p>
<p>### Parameters</p>
<p>| ID | Type | Description |</p>
<p>| ---------- | --------------------------- | -----------------------------------------------
|</p>
<p>| pr-7_prm_1 | time period (seconds) (int) | The time period in seconds
for page load times. |</p>
<p></p>