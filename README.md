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

## Credits

All credits goes for pluralsight course
Meeting Web Accessibility Guidelines (Section 508/ WCAG 2.1) by Gerard K. Cohen
