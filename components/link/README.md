---
description: Links lead users to a different page or further information.
title: Links
status: Draft
author: orinevares
---

![Status](https://img.shields.io/badge/Recommended-Draft-orange.svg)
> Last Updated: February 11, 2019

# Links

Links lead users to a different page.

## Example

<component-preview path="components/link/sample.html" height="150px" width="800px"> </component-preview>

## Don't Use This when:
* Users need to take an action on a page such as log-in or submit, use a [primary button](../primary_button/README.md) instead.

## Design Guidance
* If your link is at the end of a paragraph or sentence make sure the linked text does not include the full stop.
* Links should be describe where it leads to
* Do not put links in words such as "Link", "Here", or "Click Here". [Learn more about descriptive links](https://accessibility.oregonstate.edu/descriptivelinks)
* Links should not open a new tab or window. If so they need to have the relevant icon to give the user advanced warning. Example below: 

```html
<a href="knitting.html" target="_blank">Application Portal (opens in new window)</a>
```

## Behaviour

1. On hover link removes underline and turns to blue.

## Accessibility
This checkbox has been built according to [WCAG 2.0 AA](https://www.w3.org/TR/WCAG20/) standards and all government services should strive to meet this level.  This component successfully includes the following accessibility features:

### Screenreaders
* External link icon included if link opens a new window or tab
* Descriptive language for writing links. [Learn more about descriptive links](https://accessibility.oregonstate.edu/descriptivelinks)

As read using ChromeVox

> *"This is an example of a link to access your application, internal link."*

> *"Here is another example of a link to apply, internal link."*

> *"Link, internal link."*

### Colour Contrast
* [Contrast ratio](https://webaim.org/articles/contrast/) exceeds 7:1 for link text

### Conveying Information
* Underline allows users to identify the link without relying on colour alone
* Underline dissapears on hover indicating link is clickable

## Code

### HTML

```html
    <p>This is an internal example of a link to <a href="#">access your application</a>.</p>
    <p>Here is another example of an internal link to <a href="#">apply</a>.</p>
    <p>This is an example of an <a href="#">External Link</a> <i class="fas fa-external-link-alt"></i></p>
```
    
### CSS

```css
body {
  font-family: ‘BCSans’, ‘Noto Sans’, Verdana, Arial, sans-serif;
  font-size: 18px;
}

a {
  color: #1a5a96;
}

a:hover {
  text-decoration: none;
  color: blue;
}

i {
  color: #1a5a96;
}
```
