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

#### Summary

- Tables for tabular data, not layout
- Table grouping: `<thead>`, `<tfoot>`,`<tbody>`
- `<th>` vs `<td>`
- Associating headers and cells: scope vs headers
- Simple vs Complex Tables


## Credits

All credits goes for pluralsight course
Meeting Web Accessibility Guidelines (Section 508/ WCAG 2.1) by Gerard K. Cohen
