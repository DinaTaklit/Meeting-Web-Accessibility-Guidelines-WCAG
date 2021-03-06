# Meeting Web Accessibility Guidelines (Section 508/ WCAG 2.1)

- If you are a web/front-end developer, the work you produce must be accessible to all users.
  
- Get hands-on, practical code examples that you can start using today towards your goal of meeting official accessibility guidelines.
  
- First, you will learn the differences between Section 508 and WCAG 2.1, helping you to decide which guideline to use.
  
- Dive into real-world, reusable code patterns/techniques and matching them to relevant guidelines.
  
- After finishing this course, not only will you be equipped to acquire government/education-related contracts, but you'll be able to make sites that meet established accessibility conformance guidelines and are more usable for everyone.

## 1. CHOOSING A WEB CONFORMANCE GUIDELINE

### Web Conformance Guidelines

- Accessible to people with disabilities
- Protection from discrimination lawsuits
- Better Search Engine Optimization
- Greater overall usability
- Future proof for yourself

### Official Conformance Guidelines

- Section 508 : United State
- WCAG 2.1(World Wide Web
Consortium)

### Section 508

- 1986 Amendment to Rehabilitation Act of 1973, updated in 2017
- Targeting websites developed or used by the federal government
- More information available at www.section508.gov

### WCAG 2.1

- Published in 2018 by the WCAG Working Group (WCAG WG), which is part of the World Wide Web Consortium (W3C) Web Accessibility Initiative (WAI)
- 78 total criteria organized as 13 guidelines under 4 principles – Perceivable, Operable, Understandable, Robust (POUR)
- Each guideline has 3 levels of conformance – **Level A**, **Level AA**, and **Level AAA**  
- More information available at
https://www.w3.org/WAI/standards-guidelines/wcag/

#### WCAG 2.1: POUR

##### WCAG 2.1: Perceivable

- Users must be able to perceive the information being presented

##### WCAG 2.1: Operable

- Users must be able to operate the interface

##### WCAG 2.1: Understandable

- Users must be able to understand the information as well as the operation of the user interface

##### WCAG 2.1: Robust

- Users must be able to access the content as
technologies advance

#### WCAG 2.1 Levels of Conformances

- **Level A**: Most basic of web
accessibility features
- **Level AA**: Biggest and most
common barriers
- **Level AAA**: Highest level of
accessibility

### Which to choose

:heavy_check_mark: WCAG 2.1 Level AA

### Section 508 vs. WCAG 2.1

- Section 508
  - Last updated in 2017
  - Limited to federal agencies, federally
  funded, or under contract by a federal
  agency

- WCAG 2.1
  - Last updated in 2018
  - Global acceptance
  
> Meeting WCAG 2.1 Level AA
covers all of Section 508
> Section 508 refresh is
expected to require
conformance to WCAG 2.1
Level AA

## 2. HTML

- HTML = SEMANTIC = ACCESSIBILITY
- **Web Stack**: HTML, CSS, JavaScript
- **Full Web Stack**: HTML, CSS, JavaScript, Area
- => SEMANTIC HTML IS ALREADY ACCESSIBLE!

### 2.1 Document Structure and Landmarks

#### Documnt Structure

- Page Structure => Content Structure
- Machine Readable Code => Human Readable Code
- Landmarks => Headings

#### Summary

- <!doctype>, language, and encoding
- Text resizing via viewport and relative
- units (em or rem)
- Unique Page `<title>`
- Landmarks
- Headings `<h1>` - `<h6>`

### 2.2 List

- Ordered List `<ol />`, Unordered List `<ul />`, Description List `<dl />`
- Why bother? => Improved Semantics
  > Screen readers
  >
  > - Same experience
  > - Discoverable Lists
  > - Type of List
  > - Total Items in List
  > - Item Number (ex, “Item 3 of 5”)

#### Info and Relationships

- Information, structure, and relationships conveyed
through presentation can be programmatically
determined or are available in text.
  - Logical structure
  - Visual cues, via CSS, must be conveyed non-visually via
  semantics

### 2.3 Navigation and skip links

- Consistent navigation
- Multiple ways to find pages/ content
- Meaningful link content
- Consistent overall interface
- Skip Links

#### Level AA 1.4.4 – Resize Text

Except for captions and images of text, text can be
resized without assistive technology up to 200 percent
without loss of content or functionality.

#### Level AA 1.4.5 – Images of Text

If the technologies being used can achieve the visual
presentation, text is used to convey information rather
than images of text.

#### Level AA 3.2.3 – Consistent Navigation

Navigational mechanisms that are repeated on multiple
Web pages within a set of Web pages occur in the same
relative order each time they are repeated, unless a
change is initiated by the user.

#### Level AA 2.4.5 – Multiple Ways

More than one way is available to locate a Web page
within a set of Web pages except where the Web Page is
the result of, or a step in, a process.

#### Level AA 3.2.4 – Consistent Identification

Components that have the same functionality within a
set of Web pages are identified consistently.

> Buttons/ Icons should be labelled the same for similar  functionality. Don’t switch things up!

#### Level A 2.4.4 – Link Purpose

The purpose of each link can be determined from the link
text alone or from the link text together with its
programmatically determined link context, except where the
purpose of the link would be ambiguous to users in general.

- Read More?
  - Visually Hidden Text - Frameworks => Bootstrap sr-only, Foundation show-for-sr
  - Visually Hidden CSS
  
   ```css
      .visuallyHidden {
      border: 0;
      clip: rect(0, 0, 0, 0);
      height: 1px;
      margin: -1px;
      overflow: hidden;
      padding: 0;
      position: absolute;
      white-space: nowrap;
      width: 1px;
      }
   ```  

#### Level A 2.4.1 – Bypass Blocks

A mechanism is available to bypass blocks of content
that are repeated on multiple Web pages.

- **Skip Link**: A shortcut link directly to the main content

### 2.4 Table

- Used to display data into rows and columns of cells
- Tables should not be used for layout!
- Parts of a Table
  - `<caption>`
  - `<thead>, <tfoot>, <tbody>`
  - `<th>`
  - scope and headers
- Complex tables should have a summary of how the table data is structured
- `<table summary="…">` is duprecated in HTML5
- An easy solution: add to the `<caption>`

#### Table Issues

- Complex tables are complex to navigate
- Personal user settings
- Screen Reader/ Browser Combinations

> It’s your job to add the proper content using the proper markup

- Avoid complex tables
- Avoid nesting and spanned columns/ rows
- Flatten data as much as possible

#### Table Summary

- Tables for tabular data, not layout
- Table grouping: `<thead>`, `<tfoot>`,`<tbody>`
- `<th>` vs `<td>`
- Associating headers and cells: scope vs headers
- Simple vs Complex Tables

### 2.5 Forms

#### Overview

- Accessible Forms
- Error Identification
- Color
- Keyboard Navigation/ Focus Indication

#### Level AA 1.4.3 – Contrast

The visual presentation of text and images of text has a
contrast ratio of at least 4.5:1

- Foreground stands out from background
- Does not apply to disabled elements or logos
- Applies to images and videos

#### Level AA 1.4.11 – Non-Text Contrast

User interface components and graphical objects have a
contrast ratio of at least 3:1

#### Level A 3.3.2 – Labels or Instructions

Labels or instructions are provided when content
requires user input

- Prefer visible labels

#### Level A 2.5.3 – Label in Name

Labels should match the text that is presented visually

#### Level A 4.1.2 – Name, Role, Value

For all user interface components (including but not limited to: form
elements, links and components generated by scripts), the name and
role can be programmatically determined; states, properties, and values
that can be set by the user can be programmatically set; and notification
of changes to these items is available to user agents, including assistive
technologies

#### Level A 1.3.3 – Sensory Characteristics

Instructions provided for understanding and operating
content do not rely solely on sensory characteristics of
components such as shape, size, visual location,
orientation, or sound

#### Level A 2.1.1 - Keyboard

All functionality of the content is operable through a
keyboard interface without requiring specific timings for
individual keystrokes

#### Level A 2.1.2 – No Keyboard Traps

If keyboard focus can be moved to a component of the
page using a keyboard interface, then focus can be
moved away from that component using only a
keyboard interface

- Hijacking keystrokes
- Preventing blur event
- Common responsive patterns

#### Level A 2.1.4 – Character Key Shortcuts

Users should have the ability to turn off, remap, or
activate only on focus.

#### Level AA 2.4.7 – Focus Visible

Any keyboard operable user interface has a mode of
operation where the keyboard focus indicator is visible.

#### Level A 1.4.1 – Use of Color

Color is not used as the only visual means of conveying
information, indicating an action, prompting a response,
or distinguishing a visual element

- 10% of men are color blind.
- 75% of those are red/ green deficient.
- Forms and Error Validation: red for errors green for success :!

#### Level A 3.3.1 – Error Identification

If an input error is automatically detected, the item that
is in error is identified and the error is described to the
user in text

#### Level AA 3.3.3 – Error Suggestion

If an input error is automatically detected and
suggestions for correction are known, then the
suggestions are provided to the user, unless it would
jeopardize the security or purpose of the content

- Never set a tabindex greater than 0!
- Acceptable values are -1 or 0
- Tab index follows visual order
- Visual order follows DOM order
- Acceptable tabindex Values
  - tabindex=“-1”
    - Removed from natural tab order
    - Focusable via JS, e.g. element.focus()
  - tabindex=“0”
    - Added to natural tab order
    - Focusable via JS, e.g. element.focus()

#### Forms Levels

- Level A 3.3.2 – Labels or Instructions
- Level A 4.1.2 – Name, Role, Value
- Level A 3.3.1 – Error Identification
- Level AA 3.3.3 – Error Suggestion
- Level A 1.3.1 – Info and Relationships
- Level AA 2.4.6 – Headings and Labels

#### Additional Guidelines

#### Level AA 3.3.4 – Error Prevention

Web pages that cause legal commitments or financial transactions for the user to occur, or that modify or delete
user-controllable data in data storage systems, must be reversible, checked, and confirmed

#### Level A 2.2.1 - Timing

Adjustable For each time limit that is set by the content, the user is
able to either turn off, adjust, or extend the time limit

#### Forms Summary

- Accessible Forms
- Error Identification
- Color
- Keyboard Navigation/ Focus Indication

## 3. Media

### Level A 1.1.1 – Non-text Content

All non-text content that is presented to the user has a
text alternative that serves the equivalent purpose.

### Media Overview

- Images
  - Background Images via CSS
  - SVG
- Audio
- Video
- Additional Media Guidelines

### 3.1 Images

- Assistive technologies cannot read text in images

#### => Level AA 1.4.5 – Images of Text

If the technologies being used can achieve the visual
presentation, text is used to convey information rather
than images of text

#### => Level A 1.1.1 – Non-text Content

All non-text content that is presented to the user has a
text alternative that serves the equivalent purpose.

- All `<img>`’s must use the **alt** attribute!

#### Alt Attribute Usage

- Error downloading
- Images turned off

> Images that are for decoration only should have an empty alt attribute, `alt=""`

- Screen readers ignore images with empty alt attributes

#### Tips for Writing ALT Text

- **Don’t describe the image literally**
  - Ex, "brown couch, with brown pillow on the left with alphabet imprint and pencil
  on top, with a laptop next to it"
- **Avoid words like "picture of" or "image of"**
  - Assistive technologies will note image**
- **Do describe the meaning or purpose of the image**
  - What was the point? What were you thinking?
- **Include any text in the image**

> Whatever is conveyed visually needs to be conveyed programatically (Perceivable)

### 3.2 Background Images via CSS

- Add hidden span to explain the contenet of the background image see portfolio browser support

### 3.3 Background Images via CSS

- **Add `role="img"` for semantics**
- **Use the `<title>`**
  - `<desc>` for expanded content, if necessary
- **Use aria-labelledby referencing the `<title>`**
  - aria-describedby to reference the `<desc>`

### 3.4 Audio

#### Examples of Audio-only

- Podcasts
- Radio newscast (recorded)
- TV/ Movie sound bites

#### Level A 1.2.1 - Audio-only and Videoonly (Prerecorded)

For prerecorded audio-only and prerecorded video-only
media, an alternative is provided that presents
equivalent information.

#### : Level A 1.1.1 – Non-text Content

All non-text content that is presented to the user has a
text alternative that serves the equivalent purpose.

#### Creating Transcripts

- Paid service
- Speech Recognition
  - Google Docs Voice Typing
  - Windows Speech Recognition
  - Apple Dictation
  - Dragon Naturally Speaking
- Manual

#### Tips for Creating Transcripts

- Include names of speakers
- Describe everything

#### Presenting Transcripts

- Inline
- Link

### 3.5 Video

#### Level A – 1.2.3 Audio Description or Media Alternative (Prerecorded)

An alternative for time-based media or audio description
of the prerecorded video content is provided for
synchronized media.

#### =>: Level A 1.1.1 – Non-text Content

All non-text content that is presented to the user has a
text alternative that serves the equivalent purpose.

#### Provide Captions

- **Level A 1.2.1 – Captions (Prerecorded)**
  - Captions are provided for all prerecorded audio content in synchronized media
- **Level AA 1.2.4 – Captions (Live)**
  - Captions are provided for all live audio content in synchronized media

#### Types of Captions

- **Open**: Always visible, embedded/ burned into videos
- **Closed**: Overlay, toggled on/ off by user

#### Captioning Prerecorded Video

- **YouTube**
  - Auto-subtitle
  - Upload a transcript and sync
  - Manual entry
- **Video Captioning Services**
- **Manual**

#### Captioning Live Video

- **Communication Access Realtime**
- **Communication (CART)**
  - Live, professional stenographers/subtitlers

#### Level AA – 1.2.5 Audio Description (Prerecorded)

Audio description is provided for all prerecorded video
content in synchronized media.

#### Creating Audio Description

- **Narrate non-visual cues**
  - "Door slams", "Thunder and lightning outside window", "Pam covers mouth while laughing as Dwight discovers his
  stapler is molded in jello"
- **Have subjects introduce themselves and describe surroundings**

### 3.6 Additional Media Guidelines

#### Level A 1.4.2 – Audio Control

If any audio on a Web page plays automatically for more
than 3 seconds, either a mechanism is available to pause or
stop the audio, or a mechanism is available to control audio
volume independently from the overall system volume level.

#### Level A 2.2.2 – Pause, Stop, Hide

For moving, blinking, scrolling, or auto-updating
information provide a mechanism to pause, stop, or hide

#### Level A 2.3.1 - Three Flashes or Below Threshold

Web pages do not contain anything that flashes more
than three times in any one second period

> Any embedded media using `<iframe>` should have a label, via the "`title`" attribute (Level A 2.4.1, Level A 4.1.2)

#### Media Summary

- **Non-text Content**
  - Alternate text for images, via “alt”
  attribute
  - Transcripts
  - Captions and audio description
- **Controls for Audio and auto-updating content**
- Flashing

## 4. Responsive Web Design and Accessibility

### Responsive Overview

- Switching context
- Order of content
- Focus order
- Mobile devices
- Additional responsive guidelines

### 4.1 Switching Context

#### Level A 3.2.2 – On Input

Changing the setting of any user interface component
does not automatically cause a change of context unless
the user has been advised of the behavior before using
the component.

### 4.2 Order of Content/ Focus

#### Level A 1.3.2 – Meaningful Sequence

When the sequence in which content is presented
affects its meaning, a correct reading sequence can be
programmatically determined.

- Visual order must match DOM order
- Assistive technologies access page content via markup/ DOM
- Combination of screen magnifiers and readers

#### Level A 2.4.3 – Focus Order

If a Web page can be navigated sequentially and the
navigation sequences affect meaning or operation,
focusable components receive focus in an order that
preserves meaning and operability.

- Focus order must be in a logical and expected manner

#### Level A 3.2.1 – On Focus

When any component receives focus, it does not initiate
a change of context.

- Don’t programmatically shift focus when not expected
- Notify users up front that the change will happen

### 4.3 Mobile Devices

#### Level AA 1.3.4 – Orientation

Content does not restrict its view and operation to a
single display orientation.

#### Level A 2.5.1 – Pointer Gestures

All functionality that uses gestures can be operated with
a single pointer.

#### Level A 2.5.2 – Pointer Cancellation

For functionality operated using a single point can be
cancelled or deferred.

#### Level A 2.5.4 – Motion Actuation

Functionality operated by device motion can also be
operated by UI components.

### 4.4 Additional Responsive Guidelines

- Be careful with off screen content
- Proper Ways to Accessibly Hide Content:
  - hidden attribute `[hidden]` `{ display: none; }`
  - `display: none;`
  - `visibility: hidden;`
  - `aria-hidden="true"`
- Use relative units, either em, rem, %

#### Level AA 1.4.12 – Text Spacing

No loss of content or functionality occurs by setting the following:
  • Line height is 1.5x font size
  • 2x font size spacing after paragraphs
  • Letter spacing at least .12x font size
  • Word space at least .16x font size

```css
html, body {
font-size: 1rem;
line-height: 1.5;
letter-spacing: .12rem;
word-spacing: .16rem;
}
p + p {
margin-top: 2rem;
}
```

- Avoid clipping content or introducing scrollbars

#### Level AA 1.4.10 – Reflow

Content can be presented without loss of information or
functionality, and without requiring scrolling in two dimensions
for:
  • Vertical scrolling content at a width equivalent to 320 CSS
  pixels
  • Horizontal scrolling content at a height equivalent to 256 CSS
  pixels

- Maintain color contrast with text over images

### Responsive Web Design and Accessibility Summury

- **Switching Context**
  - On focus/ input
- **Order of content**
  - Visual order must match DOM order
  - Floats, absolute positioning, flex order
- **Focus order**
  - Logical, Predictable
- **Mobile devices**
  - Orientation
  - Gestures and motion actuation
- **Additional Guidelines**
  - Off screen content
  - Relative units

## Credits

All credits goes for pluralsight course
Meeting Web Accessibility Guidelines (Section 508/ WCAG 2.1) by Gerard K. Cohen
