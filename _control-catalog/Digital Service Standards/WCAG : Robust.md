---
title: "WCAG : Robust"
permalink: /wcag-robust/
variant: markdown
description: ""
third_nav_title: Digital Service Standards
---
Controls to ensure content remains accessible across various technologies and assistive tools.

| Controls                                         |
| ------------------------------------------------ |
| [WR-1: Name, Role, Value](#wr-1-name-role-value) |
| [WR-2: Status Messages](#wr-2-status-messages)   |

## WR-1: Name, Role, Value

**Group:** WCAG - Robust

### Control Statement

Ensure that essential information of custom components and controls can be identified and read by assistive technologies.

### Control Recommendations

Essential information including name, roles, properties, values, states, and state changes are provided using techniques like ARIA labels.

Standard HTML controls should already meet this criterion when used according to specification. (example: text input field)

### Rationale

Enables end users of assistive technology to properly understand and interact with custom components.

## WR-2: Status Messages

**Group:** WCAG - Robust

### Control Statement

Ensure that assistive technology can identify and announce system status changes that don&#39;t receive focus.

### Control Recommendations

Use ARIA roles and properties to inform users of status changes, such as when an incorrect text in an input is entered and a status message appears above.

### Rationale

Allows screen readers to identify and announce changes to content that may otherwise be missed by users of assistive technologies. This benefits users with visual impairments who unlike sighted users may not notice changes outside of their area of focus.
