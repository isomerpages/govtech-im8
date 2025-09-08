---
title: "WCAG : Robust"
permalink: /wcag-robust/
variant: markdown
description: ""
third_nav_title: Digital Service Standards
---
<p>Controls to ensure content remains accessible across various technologies
and assistive tools.</p>
<p>| Controls |</p>
<p>| ------------------------------------------------ |</p>
<p>| [WR-1: Name, Role, Value](#wr-1-name-role-value) |</p>
<p>| [WR-2: Status Messages](#wr-2-status-messages) |</p>
<p>## WR-1: Name, Role, Value</p>
<p><strong>Group:</strong> WCAG - Robust</p>
<p>### Control Statement</p>
<p>Ensure that essential information of custom components and controls can
be identified and read by assistive technologies.</p>
<p>### Control Recommendations</p>
<p>Essential information including name, roles, properties, values, states,
and state changes are provided using techniques like ARIA labels.</p>
<p>Standard HTML controls should already meet this criterion when used according
to specification. (example: text input field)</p>
<p>### Rationale</p>
<p>Enables end users of assistive technology to properly understand and interact
with custom components.</p>
<p>## WR-2: Status Messages</p>
<p><strong>Group:</strong> WCAG - Robust</p>
<p>### Control Statement</p>
<p>Ensure that assistive technology can identify and announce system status
changes that don&amp;#39;t receive focus.</p>
<p>### Control Recommendations</p>
<p>Use ARIA roles and properties to inform users of status changes, such
as when an incorrect text in an input is entered and a status message appears
above.</p>
<p>### Rationale</p>
<p>Allows screen readers to identify and announce changes to content that
may otherwise be missed by users of assistive technologies. This benefits
users with visual impairments who unlike sighted users may not notice changes
outside of their area of focus.</p>
<p></p>