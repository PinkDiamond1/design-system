---
description: Footer help users understand what the content of the page is about and provides a quick, organized way to reach the main sections of a website.
title: Footer - Basic
status: Draft
author: orinevares
---

![Status](https://img.shields.io/badge/Recommended-Draft-orange.svg)
> Last Updated: February 11, 2019

# Footer - Basic
Footers help people find what they need after scrolling to the bottom of a web page. They provide supplementary information such as copyright, contact information, social media links, and links to other pages within a website.

## Example

<component-preview path="components/footer/sample.html" height="200px" width="800px"> </component-preview>

## Requirements:
* This footer must appear on all public-facing online B.C. Government content and services.

Footer Links:
* “Home” returns to home page of your service
* [Disclaimer](https://www2.gov.bc.ca/gov/content/home/disclaimer), [Privacy](https://www2.gov.bc.ca/gov/content/home/privacy), [Accessibility](https://www2.gov.bc.ca/gov/content/home/accessibility), and [Copyright](https://www2.gov.bc.ca/gov/content/home/copyright) links should all be to the core government statements with any addendums being vetted by ministry or central legal advisors before being released. 
* “Contact Us” provides contact details for service area or program.

## Mobile Design
* All footer links should stack on one another

## Accessibility
This component has been built according to [WCAG 2.0 AA](https://www.w3.org/TR/WCAG20/) standards and all government services should strive to meet this level.  This component successfully includes the following accessibility features:

### Screenreaders
As read using ChromeVox

> *"Footer List with six (6) items."*

> *"Home. Link list item."*

> *"Disclaimer. Link list item."*

> *"Privacy. Link list item."*

> *"Accessibility. Link list item."*

> *"Copyright. Link list item."*

> *"Contact Us. Link list item."*

### Conveying Information
* Links underlined on hover to indicate they are clickable

## Code

### HTML

```html
<body style="display: flex; flex-direction: column; height: 100vh;">
  <div style="flex: 1 0 auto; padding: 20px;">
    <h1>Sample Footer</h1>
  </div>
  <footer class="footer">
    <div class="container">
    <ul>
      <li><a href=".">Home</a></li>
      <li><a href=".">Disclaimer</a></li>
      <li><a href=".">Privacy</a></li>
      <li><a href=".">Accessibility</a></li>
      <li><a href=".">Copyright</a></li>
      <li><a href=".">Contact Us</a></li>
    </ul>
    </div>
  </footer>
```
    
### CSS

```css
footer {
  background-color: #036;
  border-top: 2px solid #fcba19;
  color: #fff;
  font-family: ‘BCSans’, ‘Noto Sans’, Verdana, Arial, sans-serif; 
}

footer .container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  height: 46px;
}

footer ul {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin: 0;
  color: #fff;
  list-style: none;
  align-items: center;
  height: 100%;
}

footer ul li a {
  font-size: 0.813em;
  font-weight: normal;  /* 400 */
  color: #fff;
  border-right: 1px solid #4b5e7e;
  padding-left: 5px;
  padding-right: 5px;
}

a:hover {
  color: #fff;
  text-decoration: underline;
}

:focus {
  outline: 4px solid #3B99FC;
  outline-offset: 1px;
}
```
