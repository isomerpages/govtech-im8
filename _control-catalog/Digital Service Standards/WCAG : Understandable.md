---
title: "WCAG : Understandable"
permalink: /wcag-understandable/
variant: tiptap
description: ""
third_nav_title: Digital Service Standards
---
<p>Controls to ensure content and user interfaces are clear and comprehensible.</p>
<p>| Controls |</p>
<p>| --------------------------------------------------------------------------------------
|</p>
<p>| [WU-1: Language of Page](#wu-1-language-of-page) |</p>
<p>| [WU-2: Language of Parts](#wu-2-language-of-parts) |</p>
<p>| [WU-3: Unusual Words](#wu-3-unusual-words) |</p>
<p>| [WU-4: Abbreviations](#wu-4-abbreviations) |</p>
<p>| [WU-5: Changes On Focus](#wu-5-changes-on-focus) |</p>
<p>| [WU-6: Changes On Input](#wu-6-changes-on-input) |</p>
<p>| [WU-7: Consistent Navigation](#wu-7-consistent-navigation) |</p>
<p>| [WU-8: Consistent Identification](#wu-8-consistent-identification) |</p>
<p>| [WU-9: Consistent Help](#wu-9-consistent-help) |</p>
<p>| [WU-10: Error Identification](#wu-10-error-identification) |</p>
<p>| [WU-11: Error Suggestion](#wu-11-error-suggestion) |</p>
<p>| [WU-12: Error Prevention](#wu-12-error-prevention) |</p>
<p>| [WU-13: Redundant Entry](#wu-13-redundant-entry) |</p>
<p>| [WU-14: Accessible Authentication (Minimum)](#wu-14-accessible-authentication-minimum)
|</p>
<p>## WU-1: Language of Page</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Ensure that the primary language on a page is programmatically determined.</p>
<p>### Control Recommendations</p>
<p>For websites, specify the primary language of each webpage using the lang
attribute in the HTML tag.</p>
<p>For mobile apps, set the language of the app content using the platform&amp;#39;s
appropriate language or accessibility attribute such the accessibilityLanguage
attribute for iOS.</p>
<p>For PDFs, use the /Lang entry to specify the language of the document
or section.</p>
<p>### Rationale</p>
<p>Specifying the language ensures that assistive technology can present
content to end users using the correct language settings. This includes
pronunciation rules and rendering of display characters and scripts.</p>
<p>## WU-2: Language of Parts</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Ensure the language of words or sections that differ from the page&amp;#39;s
primary language is programmatically determined.</p>
<p>### Control Recommendations</p>
<p>Specify the language of text that differs from the primary language of
the page using the lang attribute in HTML elements or the platform’s equivalent
language tagging feature.</p>
<p>### Rationale</p>
<p>Allows assistive technology to identify language changes and properly
present content in the correct intonation and proper pronunciation to end
users.</p>
<p>## WU-3: Unusual Words</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Provide definitions for technical jargon and unusual terms.</p>
<p>### Control Recommendations</p>
<p>Avoid jargon and unusual terms where possible. If absolutely necessary,
provide contextual help such as inline explanations, tooltips, or glossaries.</p>
<p>### Rationale</p>
<p>Slang, jargon, metaphors, and figures of speech may not be understood
by some groups of end users. Identifying and providing relevance guidance
make such content more accessible to everyone.</p>
<p>## WU-4: Abbreviations</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Provide the expanded form of abbreviations.</p>
<p>### Control Recommendations</p>
<p>Provide expanded forms of abbreviations the first time they appear on
a page or flow, or provide contextual help such as inline explanations,
tooltips, or glossaries.</p>
<p>Not required for common abbreviations such as PDF and SMS where presenting
the expanded form is unnecessary for understanding of meaning, and may
negatively affect the reading experience.</p>
<p>### Rationale</p>
<p>Abbreviations or acronyms may not be understood by some end users, especially
when used for the first time in a page or section.</p>
<p>## WU-5: Changes On Focus</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Avoid changing the context when a user interface component receives focus</p>
<p>### Control Recommendations</p>
<p>If a component triggers an event when it receives focus, the context should
not be changed.</p>
<p>Avoid actions such as form submissions, opening a new window and changing
focus to another component when a component receives focus.</p>
<p>### Rationale</p>
<p>Unexpected changes of context triggered by focus change can be disorienting
to users of assistive technology. Ensuring that context changes are predictable
helps end users feel secure and in control while navigating a site.</p>
<p>## WU-6: Changes On Input</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Provide advance warning when input causes a change of context.</p>
<p>### Control Recommendations</p>
<p>Clicking on links or buttons are not considered inputs or changing the
setting of that control in the context of this control.</p>
<p>Explicitly inform end users if provision of input like checking a checkbox
or entering text into a text field results in a change in context. Changes
in context include responses like navigation to a new page or section,
submission, or opening a new window.</p>
<p>Alternatively, provide controls such as buttons that allow end users to
intentionally trigger actions like confirming a selection or submission.</p>
<p>### Rationale</p>
<p>Unexpected changes of context triggered by input can be disorienting to
users of assistive technology. Ensuring that context changes are predictable
helps users feel secure and in control while navigating a site.</p>
<p>## WU-7: Consistent Navigation</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Implement a primary or main navigation panel that</p>
<p>- 1. Is placed at or near the top of the website</p>
<p>- 2. Is not hidden or collapsed within an icon on desktop for websites</p>
<p>- 3. Presents navigation links in the same relative order on each page</p>
<p>### Control Recommendations</p>
<p>Test the top navigation component with users to ensure it is usable and
accessible.</p>
<p>### Rationale</p>
<p>Unexpected changes of context triggered by focus change can be disorienting
to end users with sensory or cognitive impairment, or users of assistive
technology.</p>
<p>## WU-8: Consistent Identification</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Identify and label repeated or related components consistently within
the digital service.</p>
<p>### Control Recommendations</p>
<p>Ensure that text used to identify a component such as label, name, or
text alternatives are identical for each user interface component with
the same function within the digital service.</p>
<p>### Rationale</p>
<p>Allows end users to quickly learn and understand navigation, design and
interaction patterns within the digital service. This reduces cognitive
load and increase efficiency of task completion.</p>
<p>## WU-9: Consistent Help</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Place help and support mechanisms consistently across multiple pages.</p>
<p>### Control Recommendations</p>
<p>Implementing the tl-4: Official Government Footer ensures consistent placement
of contact and FAQ across multiple pages.</p>
<p>Ensure that other help and support mechanisms such as messaging systems
or chatbots are also consistently placed across multiple pages.</p>
<p>### Rationale</p>
<p>Help and assistance are key aspects of a digital service. Consistent placement
makes it easy for end users, especially those who may struggle with complex
or unfamiliar interfaces to find help and support mechanisms.</p>
<p>## WU-10: Error Identification</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Indicate input errors by:</p>
<p>- a) Visually and audibly identifying the component or section that generated
the error</p>
<p>- b) Providing a text description of the error</p>
<p>### Control Recommendations</p>
<p>Clearly associate error messages with the source component or section.
Ensure the error is easily identifiable and noticeable visually and for
users of screen readers by using techniques such as ARIA attributes and
requirements in wp-11.</p>
<p>### Rationale</p>
<p>Helping end users easily and quickly identify, locate and understand errors
minimises the frustration of encountering and resolving errors.</p>
<p>## WU-11: Error Suggestion</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Ensure that error messages:</p>
<p>- a) Explain what went wrong in non-technical language.</p>
<p>- b) Explain how to correct the issue or provide alternative actions (If
suggestions for correction are known)</p>
<p>### Control Recommendations</p>
<p>Write error messages in plain language that is understood by end users
of different backgrounds, and helps the user understand or resolve the
issue. This applies to all error messages including inline form errors
and system error pages such as 404, 500 errors.</p>
<p>### Rationale</p>
<p>Error messages that are not clear or do not provide useful and actionable
information prevent end users from completing their tasks and lead to frustration.</p>
<p>## WU-12: Error Prevention</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Prevent errors by:</p>
<p>- a) Checking user-entered data for errors and/or providing a mechanism
to review, confirm, and correct information before final submission</p>
<p>- b) Allow submissions to be reversed (if feasible)</p>
<p>### Control Recommendations</p>
<p>Implement proper error validation.</p>
<p>Provide a summary page or section for users to review and correct their
inputs/information before submission. This is essential for multi-page
forms which are difficult to review, and transactions with significant
consequences such as those involving payments or having legal implications.</p>
<p>### Rationale</p>
<p>Providing ways for end users to confirm, correct, or reverse important
submissions reduces the chance of errors.</p>
<p>## WU-13: Redundant Entry</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Avoid requiring re-entry of information already provided within the same
process.</p>
<p>### Control Recommendations</p>
<p>Either auto-populate or allow the end user to select information that
was already provided.</p>
<p>This is not required if the information is required to ensure the security
of the content (E.g. Confirm password) or if the previously entered information
is no longer valid.</p>
<p>### Rationale</p>
<p>Repetitive data entry requires unnecessary effort especially for end users
with cognitive or motor impairments who may struggle with entering information.</p>
<p>## WU-14: Accessible Authentication (Minimum)</p>
<p><strong>Group:</strong> WCAG - Understandable</p>
<p>### Control Statement</p>
<p>Provide accessible authentication alternatives that do not require recalling,
solving, or transcribing information.</p>
<p>### Control Recommendations</p>
<p>Provide at least 1 non-password authentication such as Singpass QR login
or text/email based one-time codes.</p>
<p>### Rationale</p>
<p>End users with cognitive impairments have difficulties recalling or performing
cognitively demanding actions.</p>
<p></p>