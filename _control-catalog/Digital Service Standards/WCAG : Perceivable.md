---
title: "WCAG : Perceivable"
permalink: /wcag-perceivable/
variant: markdown
description: ""
third_nav_title: Digital Service Standards
---
Controls that ensure users can perceive the content in various forms

| Controls                                                                                                         |
| ---------------------------------------------------------------------------------------------------------------- |
| [WP-1: Text Alternatives for Non-Text content](#wp-1-text-alternatives-for-non-text-content)                     |
| [WP-2: Captions for Prerecorded Media](#wp-2-captions-for-prerecorded-media)                                     |
| [WP-3: Text or Audio Alternatives for Prerecorded Media](#wp-3-text-or-audio-alternatives-for-prerecorded-media) |
| [WP-4: Live Captions](#wp-4-live-captions)                                                                       |
| [WP-5: Audio Description for Prerecorded Video Content](#wp-5-audio-description-for-prerecorded-video-content)   |
| [WP-6: Presentation of Info and Relationships](#wp-6-presentation-of-info-and-relationships)                     |
| [WP-7: Meaningful Content Order](#wp-7-meaningful-content-order)                                                 |
| [WP-8: Describing Displayed Controls](#wp-8-describing-displayed-controls)                                       |
| [WP-9: Display Orientation](#wp-9-display-orientation)                                                           |
| [WP-10: Identify Input Purpose](#wp-10-identify-input-purpose)                                                   |
| [WP-11: Use of Color](#wp-11-use-of-color)                                                                       |
| [WP-12: Audio Control](#wp-12-audio-control)                                                                     |
| [WP-13: Minimum Contrast](#wp-13-minimum-contrast)                                                               |
| [WP-14: Text Scaling](#wp-14-text-scaling)                                                                       |
| [WP-15: Images of Text](#wp-15-images-of-text)                                                                   |
| [WP-16: Content Reflow](#wp-16-content-reflow)                                                                   |
| [WP-17: Non-text Contrast](#wp-17-non-text-contrast)                                                             |
| [WP-18: Text Spacing](#wp-18-text-spacing)                                                                       |
| [WP-19: Content on Hover or Focus](#wp-19-content-on-hover-or-focus)                                             |

## WP-1: Text Alternatives for Non-Text content

**Group:** WCAG - Perceivable

### Control Statement

Provide text alternatives for essential non-text content.

### Control Recommendations

Provide accurate, concise alt text or a relevant textual description for non-text content (images, charts, media).

Implement purely decorative non-text content in a way that can be ignored by assistive technology.

### Rationale

Ensures that equivalent information is conveyed to all end users by allowing assistive technologies to read and communicate essential non-text content.

## WP-2: Captions for Prerecorded Media

**Group:** WCAG - Perceivable

### Control Statement

Provide captions for prerecorded video or audio content.

### Control Recommendations

Use transcribing or captioning tools to generate captions. Ensure captions are aligned with audio and are readable.

Not required when the content is a media alternative for text and is clearly labeled as such.

### Rationale

Ensures that individuals with hearing impairments can access and understand the material. Captions also help people engage better with content and allow people to access the content without audio.

## WP-3: Text or Audio Alternatives for Prerecorded Media

**Group:** WCAG - Perceivable

### Control Statement

Provide alternatives for all prerecorded audio and video media.

### Control Recommendations

Provide text transcripts for audio-only content. Provide text alternatives or audio descriptions for video-only content and synchronised media (audio and video).

Not required when the content is a media alternative for text and is clearly labeled as such.

### Rationale

Ensures information conveyed by prerecorded audio and video content is available to all end users.

## WP-4: Live Captions

**Group:** WCAG - Perceivable

### Control Statement

Provide captions for live audio and video content.

### Control Recommendations

Use automated or live captioning services for content like livestream and webinars. Ensure that the service or tool is sufficiently accurate.

### Rationale

Live captions make live audio and video content accessible to end users who are deaf or hard of hearing.

## WP-5: Audio Description for Prerecorded Video Content

**Group:** WCAG - Perceivable

### Control Statement

Provided an audio description for all prerecorded video content.

### Control Recommendations

Provide user-selectable audio tracks focusing on critical visual elements necessary for understanding.

This is an extension of wp-3 which recommends but does not prescribe audio descriptions.

### Rationale

Ensures that individuals who have visual impairments can better experience video content. This involves both information conveyed through the audio track and also descriptions of visual information such as actions, signs and facial expressions.

## WP-6: Presentation of Info and Relationships

**Group:** WCAG - Perceivable

### Control Statement

Present the structure, order and relationships of information on a page in a way that can be programmatically determined by assistive technology.

### Control Recommendations

Apply techniques such as correct use of semantic HTML elements (e.g., headings, lists, tables), text descriptions and where necessary, ARIA markups. Do not overuse ARIA as it creates clutter and overwhelm end users.

### Rationale

Ensures that the structure and organisation of content are clear to all end users, including those who use assistive technologies.

## WP-7: Meaningful Content Order

**Group:** WCAG - Perceivable

### Control Statement

Ensure that the logical reading order of content can be programmatically determined by software.

### Control Recommendations

Ensure code is structured to preserve the logical reading order of content. Validate with screen reader testing to confirm that end users can navigate content in a logical sequence.

### Rationale

Allows assistive technology to present content in the intended reading order needed to understand the meaning.

## WP-8: Describing Displayed Controls

**Group:** WCAG - Perceivable

### Control Statement

Do not rely only on sensory characteristics such shape, colour, size, visual location, orientation, or sound when describing controls.

### Control Recommendations

Describe controls by name.

Avoid using expressions like &quot;click the blue button&quot; &quot;or&quot; &quot;Select an option after the beep&quot; when describing or referring to controls. Instead use clear, obvious and meaningful instructions like &quot;Click the &#39;next&#39; button to continue with the survey&quot;, &quot;When you have finished filling in your application form, click &#39;Submit&#39; to complete your submission&quot;

### Rationale

Reliance of specific sensory characteristics may make descriptions or instructions inaccessible to some users with specific disabilities. E.g. Colour and shape may not perceivable by blind users.

## WP-9: Display Orientation

**Group:** WCAG - Perceivable

### Control Statement

Do not restrict content to a single display orientation.

### Control Recommendations

Avoid locking orientation to a particular view. Ensure content can adapt to various orientations such as landscape and portrait without layout or functionality issues.

Not required if a specific display orientation is necessary to provide the content in an accurate and functional manner.

### Rationale

To ensure that content displays in the orientation (portrait or landscape) preferred by the end user. Users with dexterity impairments such as those in wheelchairs may have devices mounted in a particular orientation.

## WP-10: Identify Input Purpose

**Group:** WCAG - Perceivable

### Control Statement

Use labels and code to clearly specify the purpose and format of common inputs.

### Control Recommendations

Clearly distinguish similar fields such as billing address and shipping address. Specify the exact format of input fields that may have multiple valid interpretations such as dates.

### Rationale

Ensures that both regular end users and users of assistive technology can clearly discern the purpose of an input function.

## WP-11: Use of Color

**Group:** WCAG - Perceivable

### Control Statement

Avoid using colour as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element.

### Control Recommendations

Use a mix of shape (icons, symbols), colour and text for essential content such as error messages.

### Rationale

Using multiple modes in addition to colour, ensures that crucial information and state changes are well communicated to end users, especially those with colour vision deficiencies.

## WP-12: Audio Control

**Group:** WCAG - Perceivable

### Control Statement

Providing options to pause, stop or adjust the volume of audio that automatically plays for more than 3 seconds.

### Control Recommendations

Only play sounds on user request or provide the user with functions to pause, stop or adjust the volume near the beginning of the digital service so it is easily and quickly discovered.

### Rationale

To prevent unexpected or disruptive audio from affecting users&#39; experience, particularly those with cognitive or hearing impairments. Background audio also interferes with narration by screen reading software.

## WP-13: Minimum Contrast

**Group:** WCAG - Perceivable

### Control Statement

Ensure a minimum contrast ratio of 4.5:1 between text and its background.

Large text (at least 18 point or 14 point bold) can have a reduced contrast ratio of at least 3:1.

### Control Recommendations

Use tools like WebAIM&#39;s Contrast Checker or Oobee to verify that text and images of text meet the minimum contrast ratio.

Not required for

a) Text that is decorative, conveys no meaningful information

b) Part of a component in an inactive state

### Rationale

Adequate contrast between text and background is essential for good readability and usability, especially for end users with low vision or colour vision deficiencies.

## WP-14: Text Scaling

**Group:** WCAG - Perceivable

### Control Statement

Ensure text can be scaled up to 200% without loss of content or functionality.

### Control Recommendations

Use relative units like REM. Ensure at least one one browser or platform text scaling mechanism can be used. This includes zoom (of the entire page&#39;s content), magnification, and text-only resizing. Test to confirm that no content is clipped, truncated, or obscured after resizing.

This excludes captions and images of text.

### Rationale

Resizable text makes digital content accessible to a wide range of end users with different visual capabilities, particularly those without access to screen magnification tools.

## WP-15: Images of Text

**Group:** WCAG - Perceivable

### Control Statement

Use text instead of images of text.

### Control Recommendations

Avoid using images of text except when essential, such as for logos. Where text in images are necessary, ensure that alternative text or captions provide the same information.

### Rationale

Text in images are not accessible, especially for end users with visual impairments or reading disabilities. Users cannot adjust the size or font for better readability and the text is not readable by common screen reader technology.

## WP-16: Content Reflow

**Group:** WCAG - Perceivable

### Control Statement

Enable lines of text and content to reflow across different viewports.

### Control Recommendations

Use responsive design frameworks like CSS Flexbox or Grid and test on a variety of devices to confirm that content remains legible and usable without excessive scrolling even when text is resized.

Not required for content that requires two-dimensional layout for understanding or functionality, such as maps, complex data tables or data visualisations.

### Rationale

Enabling reflowing of content allows users who rely on large fonts, including those using devices with smaller screens to be able to view and navigate digital content without scrolling horizontally even when text size is increased.

## WP-17: Non-text Contrast

**Group:** WCAG - Perceivable

### Control Statement

Ensure a minimum contrast ratio of 3:1 between colours of user interface components and graphical objects that convey important information, and their respective backgrounds.

### Control Recommendations

Use tools like WebAIM&#39;s Contrast Checker to test contrast. Focus on elements critical for interaction, such as buttons and form inputs.

### Rationale

Sufficient contrast helps end users better perceive and identify non-text user interface components and key graphical objects, improving usability.

## WP-18: Text Spacing

**Group:** WCAG - Perceivable

### Control Statement

Ensure that text implemented using markup languages can be adjusted to the following text style properties with no loss of content or functionality:

- a) Line height to 1.5 times the font size
- b) Paragraph spacing to 2 times the font size
- c) Letter spacing to 0.12 times the font size
- d) Word spacing to 0.16 times the font size

### Control Recommendations

Allow for text spacing override by assistive technology and test with tools that simulate the spacing configurations specified.

Text content does not need to use these text spacing values as defaults, and there is no need to implement controls for users to adjust text properties within the digital service.

### Rationale

Ensures that end users, in particular those with low vision or dyslexia are: a) Not restricted from overriding default text spacing through the use of assistive technology, stylesheets or extensions. b) Content or functionality is not lost and the content remains legible and functional.

## WP-19: Content on Hover or Focus

**Group:** WCAG - Perceivable

### Control Statement

Ensure content appearing on hover or focus

- a) Appears long enough to be read and interacted with
- b) Does not disappear unexpectedly
- c) Can be easily dismissed using a pointer device or keyboard

### Control Recommendations

Design custom tooltips, sub-menus and other non-modal popups which display on hover and focus to be perceivable and dismissible without disrupting the overall user experience.

### Rationale

Elements that appear on hover or focus can be difficult to manage. End users with limited motor control may have trouble keeping their pointer steady, and keyboard-only users need a reliable way to dismiss such content.
