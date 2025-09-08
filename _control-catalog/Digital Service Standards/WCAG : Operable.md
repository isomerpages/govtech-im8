---
title: "WCAG : Operable"
permalink: /wcag-operable/
variant: tiptap
description: ""
third_nav_title: Digital Service Standards
---
<p>Controls to make interface elements easy to operate for all users</p>
<p>| Controls |</p>
<p>| ------------------------------------------------------------------------------
|</p>
<p>| [WO-1: Keyboard equivalent](#wo-1-keyboard-equivalent) |</p>
<p>| [WO-2: No Keyboard Trap](#wo-2-no-keyboard-trap) |</p>
<p>| [WO-3: Character Key Shortcuts](#wo-3-character-key-shortcuts) |</p>
<p>| [WO-4: Adjustable Timings](#wo-4-adjustable-timings) |</p>
<p>| [WO-5: Pause, Stop, Hide](#wo-5-pause-stop-hide) |</p>
<p>| [WO-6: Reduce Flash Triggers](#wo-6-reduce-flash-triggers) |</p>
<p>| [WO-7: Bypass Repeating Content](#wo-7-bypass-repeating-content) |</p>
<p>| [WO-8: Page Title And Purpose](#wo-8-page-title-and-purpose) |</p>
<p>| [WO-9: Sequential Focus Order](#wo-9-sequential-focus-order) |</p>
<p>| [WO-10: Link Text And Purpose](#wo-10-link-text-and-purpose) |</p>
<p>| [WO-11: Multiple Ways](#wo-11-multiple-ways) |</p>
<p>| [WO-12: Headings and Labels](#wo-12-headings-and-labels) |</p>
<p>| [WO-13: Focus Visible and Not Obscured](#wo-13-focus-visible-and-not-obscured)
|</p>
<p>| [WO-14: Simple Pointer Alternatives](#wo-14-simple-pointer-alternatives)
|</p>
<p>| [WO-15: Pointer Cancellation](#wo-15-pointer-cancellation) |</p>
<p>| [WO-16: Label In Name](#wo-16-label-in-name) |</p>
<p>| [WO-17: Motion Actuation](#wo-17-motion-actuation) |</p>
<p>| [WO-18: Minimum Pointer Target Size](#wo-18-minimum-pointer-target-size)
|</p>
<p>## WO-1: Keyboard equivalent</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure any action done using a pointer device can also be done using a
keyboard.</p>
<p>### Control Recommendations</p>
<p>Provide keyboard operation for all the functionality of the page unless
the function requires path-dependent input such as handwriting.</p>
<p>Avoid requiring specific timings for individual keystrokes such as requirements
to repeat or execute multiple keystrokes within a short period of time.</p>
<p>### Rationale</p>
<p>Ensures that there is no loss of functionality for users who rely on keyboards
such as those with motor impairments.</p>
<p>## WO-2: No Keyboard Trap</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure that keyboard users can move keyboard focus away or out from a
component or section of the digital service.</p>
<p>### Control Recommendations</p>
<p>Test forms, widgets, and custom elements with keyboard-only navigation
to confirm end users can exit all components using standard keys (like
Tab and Shift+Tab).</p>
<p>If the key functionality of the component restricts the focus to a subsection
of the content, communicate clearly to users how to leave that state and
&amp;quot;untrap&amp;quot; the focus.</p>
<p>### Rationale</p>
<p>A keyboard trap happens when keyboard focus is moved to a component or
subsection of the digital service without a way of the end user navigating
back out using a keyboard interface. End users who who rely on exclusive
keyboard interface usage such as people with vision and physical disabilities
get stuck and are unable to proceed to other parts of the service or complete
a critical transaction.</p>
<p>## WO-3: Character Key Shortcuts</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide a mechanism to disable or remap shortcuts that are activated using
only one character key press.</p>
<p>### Control Recommendations</p>
<p>If character key shortcuts are used, provide end users with the ability
to disable or remap them. Implement keyboard settings within the interface
for customisation, ensuring shortcuts do not interfere with common keyboard
interactions.</p>
<p>### Rationale</p>
<p>Reduces the risk of accidental activation of keyboard shortcuts for keyboard
users and speech input users, whose dictation is interpreted as strings
of letters.</p>
<p>## WO-4: Adjustable Timings</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Allow time limits to be turned off, adjusted, or extended.</p>
<p>### Control Recommendations</p>
<p>Avoid time-dependent functions unless absolutely necessary. Ensure timers
are non-disruptive and adjustable or extendable.</p>
<p>Not required when the time limit is:</p>
<p>a) Mandatory from a legal point of view</p>
<p>b) Required as part of a real-time event where extensions would invalidate
the activity</p>
<p>c) Longer than 20 hours</p>
<p>### Rationale</p>
<p>Persons with disabilities may need more time to complete complex tasks
such as filling out lengthy grant forms. Designing functions that are not
time-dependent or allow for adjustable timings will help everyone, especially
people with disabilities, succeed at completing these tasks.</p>
<p>## WO-5: Pause, Stop, Hide</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide a function to pause, stop, hide or control the frequency of moving,
blinking, scrolling or auto-updating content that occur in parallel with
other content.</p>
<p>### Control Recommendations</p>
<p>Content changes refer to, but are not exclusive to, auto-updating information,
animations containing essential information or similar components.</p>
<p>Allow users to pause, stop, or hide content that automatically moves,
blinks, scrolls or auto-updates for more than 5 seconds.</p>
<p>### Rationale</p>
<p>Content that moves or auto-updates can be a barrier to anyone who has
trouble reading stationary text quickly, tracking moving objects or noticing
page changes easily. It can also cause problems for screen readers.</p>
<p>## WO-6: Reduce Flash Triggers</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Avoid content that flashes more than three times per second or provide
a warning and the option to skip such content.</p>
<p>### Control Recommendations</p>
<p>Provide a clearly displayed warning message such as &amp;quot;This video
may potentially trigger seizures for people with photosensitive epilepsy.
Viewer discretion is advised.&amp;quot;</p>
<p>Excludes flashes contained in a small area, are low contrast or include
a small amount of the colour red.</p>
<p>### Rationale</p>
<p>Flashing content can trigger seizures in end users with photosensitive
epilepsy leading to serious health risks for these users.</p>
<p>## WO-7: Bypass Repeating Content</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide a means of skipping repetitive blocks of content that appear across
multiple pages.</p>
<p>### Control Recommendations</p>
<p>Implement visible and keyboard accessible link(s) for end users to skip
repeated content blocks and/or group blocks of repeated material in a way
that can be skipped through the use of ARIA landmarks or heading markup.</p>
<p>### Rationale</p>
<p>End users who navigate sequentially with keyboards or screen readers often
encounter repeated content such as headers and navigation links across
multiple pages. Providing a mechanism to bypass these repetitive sections
enables users to access the main content more efficiently.</p>
<p>## WO-8: Page Title And Purpose</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide a page title describing the purpose of every web page or distinct
Single-Page Application view served from the same Uniform Resource Identifier
(URI).</p>
<p>### Control Recommendations</p>
<p>Provide a clear and succinct page title that describes the purpose of
the page. For example, &amp;quot;Budget 2024 Support Schemes Calculator&amp;quot;
is a clear title stating the page contains a calculator for Support Schemes
from Budget 2024.</p>
<p>### Rationale</p>
<p>Clear, descriptive titles provide quick context, enabling all end users
(including users of assistive technologies) to quickly understand where
they are without having to scan page content. They also facilitate efficient
navigation in site maps and search results, allowing rapid identification
of relevant information.</p>
<p>## WO-9: Sequential Focus Order</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure focusable components receive focus in an order that preserves meaning
and operability when the navigation sequences affect meaning or operation.</p>
<p>### Control Recommendations</p>
<p>When a user triggers a focusable element like a modal dialog via an element
(button or link), the keyboard focus should be set to within the modal
and limited to the elements of modal until dismissed.</p>
<p>When the modal is dismissed, the keyboard focus should logically return
to the original trigger element to minimise confusion for the user.</p>
<p>### Rationale</p>
<p>Allows keyboard users to navigate in a sequence that reflects the content&amp;#39;s
logical structure, preventing disorientation from unexpected tabbing focus.
This approach accommodates various valid navigation patterns while preserving
content coherence. Implementing this improves accessibility, often results
in cleaner markup, and can enhance SEO, benefiting all users.</p>
<p>## WO-10: Link Text And Purpose</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure that link text identifies the purpose of the link and can be interpreted
easily on its own.</p>
<p>### Control Recommendations</p>
<p>Avoid using vague link text such as &amp;quot;click here&amp;quot; or
&amp;quot;read more&amp;quot;.</p>
<p>### Rationale</p>
<p>Descriptive and meaningful link text helps users understand the content
and purpose of each link without needing to read the surrounding text.
This is especially important for screen reader users who often navigate
web pages by jumping from one link to another. It also improves the SEO
value of a page and helps all users find the information they need more
efficiently.</p>
<p>## WO-11: Multiple Ways</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide at least two ways to reach the same content.</p>
<p>### Control Recommendations</p>
<p>Focus on information architecture and implement multiple ways to reach
content such as clear and logical navigation structures, search function
and shortcuts.</p>
<p>### Rationale</p>
<p>Providing multiple ways to access content allows end users to locate content
in ways that best meet their needs. Users may find one navigation path
easier or more comprehensible than another, improving both the user experience
of the service and the discoverability of content.</p>
<p>## WO-12: Headings and Labels</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide descriptive headers and labels that identify the context of surrounding
text and the component&amp;#39;s purpose.</p>
<p>### Control Recommendations</p>
<p>Do not disable platform or user-agent default visual focus indicators.
If default focus indicators are not available or do not meet other accessible
guidelines like colour contrast, modify the background colour or border
of the element with focus.</p>
<p>Ensure that &amp;#39;floating&amp;#39; components like widgets and sticky
headers do not cover elements receiving focus.</p>
<p>### Rationale</p>
<p>Allows end users to quickly identify which element or control has keyboard
focus. This is especially important for users relying exclusively on keyboards
to navigate.</p>
<p>## WO-13: Focus Visible and Not Obscured</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure components receiving focus have distinguishable indicators and
are not obscured by other elements.</p>
<p>### Control Recommendations</p>
<p>Do not disable platform or user-agent default visual focus indicators.
If default focus indicators are not available or do not meet other accessible
guidelines like colour contrast, modify the background colour or border
of the element with focus.</p>
<p>Ensure that &amp;#39;floating&amp;#39; components like widgets and sticky
headers do not cover elements receiving focus.</p>
<p>### Rationale</p>
<p>Allows end users to quickly identify which element or control has keyboard
focus. This is especially important for users relying exclusively on keyboards
to navigate.</p>
<p>## WO-14: Simple Pointer Alternatives</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide single-point alternatives to multipoint or path-based interactions
or gestures.</p>
<p>### Control Recommendations</p>
<p>If multipoint or path-based gestures such as sliders and drag-and-drop
functions are used, provide alternative options to perform the same interaction
through simple single-point alternatives.</p>
<p>### Rationale</p>
<p>Interactions that involve complicated gestures or precise movements such
as dragging or pinching can be challenging or impossible for end users
with mobility disabilities, elderly users, or those using adaptive input
devices.</p>
<p>## WO-15: Pointer Cancellation</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide a predictable and consistent way to cancel or undo pointer interactions.</p>
<p>### Control Recommendations</p>
<p>Implement clear and accessible methods to cancel critical actions such
as an &amp;quot;undo&amp;quot; function. Confirmation dialogs can be used
as a secondary confirmation for critical actions.</p>
<p>Unless absolutely necessary, only execute a function when the click or
touch is released (up-event) instead of when the click or touch is made
(down-event). This gives end users the opportunity to cancel the activation
after by moving their pointer or finger away from the target before releasing.</p>
<p>### Rationale</p>
<p>People with various disabilities can accidentally initiate touch or mouse
events. Allowing such end users to easily recover from such unintended
pointer actions minimises unintended consequences such as accidental submissions.</p>
<p>## WO-16: Label In Name</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure that visible text labels of user interface components match or
are contained within their programmatic or accessible names.</p>
<p>### Control Recommendations</p>
<p>Ensure that accessibility labels meaningfully describe the equivalent
visual UI element by containing both the visible text label and other contextual
descriptors that help assistive technology users fully understand the purpose
and interaction.</p>
<p>### Rationale</p>
<p>Matching visible text labels with the programmatic component supports
the use of assistive technologies such as allowing speech-input users to
navigate by speaking the visible text labels of components.</p>
<p>## WO-17: Motion Actuation</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Provide an option to disable motion control for motion-operated features,
and provide alternative means to operate such features.</p>
<p>### Control Recommendations</p>
<p>When implementing motion-operated features, provide a way to disable motion
actuation and offer alternative means to operate these features through
user interface components.</p>
<p>Not required when motion is essential to the function, such as in pedometers
that require device motion to count steps.</p>
<p>### Rationale</p>
<p>End users with motor impairments may have difficulty holding or moving
a device steadily, which can prevent them from using motion-operated features
and may cause accidental triggering of functions.</p>
<p>## WO-18: Minimum Pointer Target Size</p>
<p><strong>Group:</strong> WCAG - Operable</p>
<p>### Control Statement</p>
<p>Ensure that interactive areas for pointer input are at least 24 by 24
CSS pixels.</p>
<p>### Control Recommendations</p>
<p>Use min-height and min-width to ensure sufficient target spacing.</p>
<p>If targets have to be smaller than 24-pixels, they must be spaced so that
a 24-pixel area around each target does not overlap adjacent targets.</p>
<p>Follow platform guidelines and consider larger target sizes for mobile
applications and mobile web browsing where touch is the input mechanism.</p>
<p>Not required if the size of the interactive area is constrained by the
line-height of non-interactive text such as text links within a body of
text.</p>
<p>### Rationale</p>
<p>End users with physical and fine motor disabilities require more effort
to accurately activate small targets or targets that are close to each
other. Ensuring pointer inputs are large enough with sufficient spacing
between targets reduces the likelihood of errors from accidentally activating
the wrong control.</p>
<p></p>