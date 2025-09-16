---
title: "WCAG : Understandable"
permalink: /control-catalog/wu/
variant: markdown
description: ""
third_nav_title: Digital Service Standards
---
Controls to ensure content and user interfaces are clear and comprehensible.

| Controls                                                                               |
| -------------------------------------------------------------------------------------- |
| [WU-1: Language of Page](#wu-1-language-of-page)                                       |
| [WU-2: Language of Parts](#wu-2-language-of-parts)                                     |
| [WU-3: Unusual Words](#wu-3-unusual-words)                                             |
| [WU-4: Abbreviations](#wu-4-abbreviations)                                             |
| [WU-5: Changes On Focus](#wu-5-changes-on-focus)                                       |
| [WU-6: Changes On Input](#wu-6-changes-on-input)                                       |
| [WU-7: Consistent Navigation](#wu-7-consistent-navigation)                             |
| [WU-8: Consistent Identification](#wu-8-consistent-identification)                     |
| [WU-9: Consistent Help](#wu-9-consistent-help)                                         |
| [WU-10: Error Identification](#wu-10-error-identification)                             |
| [WU-11: Error Suggestion](#wu-11-error-suggestion)                                     |
| [WU-12: Error Prevention](#wu-12-error-prevention)                                     |
| [WU-13: Redundant Entry](#wu-13-redundant-entry)                                       |
| [WU-14: Accessible Authentication (Minimum)](#wu-14-accessible-authentication-minimum) |

## WU-1: Language of Page

**Group:** WCAG - Understandable

### Control Statement

Ensure that the primary language on a page is programmatically determined.

### Control Recommendations

For websites, specify the primary language of each webpage using the lang attribute in the HTML tag.

For mobile apps, set the language of the app content using the platform&#39;s appropriate language or accessibility attribute such the accessibilityLanguage attribute for iOS.

For PDFs, use the /Lang entry to specify the language of the document or section.

### Rationale

Specifying the language ensures that assistive technology can present content to end users using the correct language settings. This includes pronunciation rules and rendering of display characters and scripts.

## WU-2: Language of Parts

**Group:** WCAG - Understandable

### Control Statement

Ensure the language of words or sections that differ from the page&#39;s primary language is programmatically determined.

### Control Recommendations

Specify the language of text that differs from the primary language of the page using the lang attribute in HTML elements or the platform’s equivalent language tagging feature.

### Rationale

Allows assistive technology to identify language changes and properly present content in the correct intonation and proper pronunciation to end users.

## WU-3: Unusual Words

**Group:** WCAG - Understandable

### Control Statement

Provide definitions for technical jargon and unusual terms.

### Control Recommendations

Avoid jargon and unusual terms where possible. If absolutely necessary, provide contextual help such as inline explanations, tooltips, or glossaries.

### Rationale

Slang, jargon, metaphors, and figures of speech may not be understood by some groups of end users. Identifying and providing relevance guidance make such content more accessible to everyone.

## WU-4: Abbreviations

**Group:** WCAG - Understandable

### Control Statement

Provide the expanded form of abbreviations.

### Control Recommendations

Provide expanded forms of abbreviations the first time they appear on a page or flow, or provide contextual help such as inline explanations, tooltips, or glossaries.

Not required for common abbreviations such as PDF and SMS where presenting the expanded form is unnecessary for understanding of meaning, and may negatively affect the reading experience.

### Rationale

Abbreviations or acronyms may not be understood by some end users, especially when used for the first time in a page or section.

## WU-5: Changes On Focus

**Group:** WCAG - Understandable

### Control Statement

Avoid changing the context when a user interface component receives focus

### Control Recommendations

If a component triggers an event when it receives focus, the context should not be changed.

Avoid actions such as form submissions, opening a new window and changing focus to another component when a component receives focus.

### Rationale

Unexpected changes of context triggered by focus change can be disorienting to users of assistive technology. Ensuring that context changes are predictable helps end users feel secure and in control while navigating a site.

## WU-6: Changes On Input

**Group:** WCAG - Understandable

### Control Statement

Provide advance warning when input causes a change of context.

### Control Recommendations

Clicking on links or buttons are not considered inputs or changing the setting of that control in the context of this control.

Explicitly inform end users if provision of input like checking a checkbox or entering text into a text field results in a change in context. Changes in context include responses like navigation to a new page or section, submission, or opening a new window.

Alternatively, provide controls such as buttons that allow end users to intentionally trigger actions like confirming a selection or submission.

### Rationale

Unexpected changes of context triggered by input can be disorienting to users of assistive technology. Ensuring that context changes are predictable helps users feel secure and in control while navigating a site.

## WU-7: Consistent Navigation

**Group:** WCAG - Understandable

### Control Statement

Implement a primary or main navigation panel that

- 1. Is placed at or near the top of the website
- 2. Is not hidden or collapsed within an icon on desktop for websites
- 3. Presents navigation links in the same relative order on each page

### Control Recommendations

Test the top navigation component with users to ensure it is usable and accessible.

### Rationale

Unexpected changes of context triggered by focus change can be disorienting to end users with sensory or cognitive impairment, or users of assistive technology.

## WU-8: Consistent Identification

**Group:** WCAG - Understandable

### Control Statement

Identify and label repeated or related components consistently within the digital service.

### Control Recommendations

Ensure that text used to identify a component such as label, name, or text alternatives are identical for each user interface component with the same function within the digital service.

### Rationale

Allows end users to quickly learn and understand navigation, design and interaction patterns within the digital service. This reduces cognitive load and increase efficiency of task completion.

## WU-9: Consistent Help

**Group:** WCAG - Understandable

### Control Statement

Place help and support mechanisms consistently across multiple pages.

### Control Recommendations

Implementing the tl-4: Official Government Footer ensures consistent placement of contact and FAQ across multiple pages.

Ensure that other help and support mechanisms such as messaging systems or chatbots are also consistently placed across multiple pages.

### Rationale

Help and assistance are key aspects of a digital service. Consistent placement makes it easy for end users, especially those who may struggle with complex or unfamiliar interfaces to find help and support mechanisms.

## WU-10: Error Identification

**Group:** WCAG - Understandable

### Control Statement

Indicate input errors by:

- a) Visually and audibly identifying the component or section that generated the error
- b) Providing a text description of the error

### Control Recommendations

Clearly associate error messages with the source component or section. Ensure the error is easily identifiable and noticeable visually and for users of screen readers by using techniques such as ARIA attributes and requirements in wp-11.

### Rationale

Helping end users easily and quickly identify, locate and understand errors minimises the frustration of encountering and resolving errors.

## WU-11: Error Suggestion

**Group:** WCAG - Understandable

### Control Statement

Ensure that error messages:

- a) Explain what went wrong in non-technical language.
- b) Explain how to correct the issue or provide alternative actions (If suggestions for correction are known)

### Control Recommendations

Write error messages in plain language that is understood by end users of different backgrounds, and helps the user understand or resolve the issue. This applies to all error messages including inline form errors and system error pages such as 404, 500 errors.

### Rationale

Error messages that are not clear or do not provide useful and actionable information prevent end users from completing their tasks and lead to frustration.

## WU-12: Error Prevention

**Group:** WCAG - Understandable

### Control Statement

Prevent errors by:

- a) Checking user-entered data for errors and/or providing a mechanism to review, confirm, and correct information before final submission
- b) Allow submissions to be reversed (if feasible)

### Control Recommendations

Implement proper error validation.

Provide a summary page or section for users to review and correct their inputs/information before submission. This is essential for multi-page forms which are difficult to review, and transactions with significant consequences such as those involving payments or having legal implications.

### Rationale

Providing ways for end users to confirm, correct, or reverse important submissions reduces the chance of errors.

## WU-13: Redundant Entry

**Group:** WCAG - Understandable

### Control Statement

Avoid requiring re-entry of information already provided within the same process.

### Control Recommendations

Either auto-populate or allow the end user to select information that was already provided.

This is not required if the information is required to ensure the security of the content (E.g. Confirm password) or if the previously entered information is no longer valid.

### Rationale

Repetitive data entry requires unnecessary effort especially for end users with cognitive or motor impairments who may struggle with entering information.

## WU-14: Accessible Authentication (Minimum)

**Group:** WCAG - Understandable

### Control Statement

Provide accessible authentication alternatives that do not require recalling, solving, or transcribing information.

### Control Recommendations

Provide at least 1 non-password authentication such as Singpass QR login or text/email based one-time codes.

### Rationale

End users with cognitive impairments have difficulties recalling or performing cognitively demanding actions.