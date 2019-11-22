---
description: Radio buttons allow users to select one item from a given list.
title: Radio Button
status: Draft
author: orinevares
---

![Status](https://img.shields.io/badge/Recommended-Draft-orange.svg)
> Last Updated: February 11, 2019

# Radio Button
Radio buttons are a type of input that allow users to select only one option from a list.

## Example

<component-preview path="components/radio/sample.html" height="150px" width="800px"> </component-preview>

## Use This For
* A user can only select one option from a list

## Don't Use This when
*	A user can select more than one option from a list. In this case, use a [checkbox](../checkbox.md)

## Design Guidance
* Once a user has selected an option, they cannot return to having no options selected. If applicable, include a "None of the above" or "I don't know" option.
*	Do not assume a user will know how many options they can select. If needed, include a hint like "Select one option." 
*	It can be helpful to order the options based on user needs. For example, place the most likely responses at the top
*	Options should be listed vertically. This results with the best readability, and helps users with the correct association between the radio button and it's label.

## Rationale
Our radio buttons are larger than most browser defaults to allow for greater visibility and larger target areas for touchscreen devices. Research has shown that users resort to only clicking the radio and not the associated text.
Based on research done by [Gov.UK](https://designnotes.blog.gov.uk/2016/11/30/weve-updated-the-radios-and-checkboxes-on-gov-uk/)

## Behaviour
1.	Users should be able to click or tap on either the radio button or text label to select the option
2.	Do not preselect options, this results in perceived bias

## Accessibility
This component has been built according to [WCAG 2.0 AA](https://www.w3.org/TR/WCAG20/) standards and all government services should strive to meet this level.  This component successfully includes the following accessibility features:

### Screenreaders
As read on ChromeVox

Note: To navigate through radio selections tab to the first list item and then use your arrow keys to move up and down the list.

> *"One. Radio button unselected."*

> *"Two. Radio button unselected."*

> *"Three. Radio button unselected."*

> *"Four. Radio button unselected."*

If a radio button was selected

> *"[Radio Label]. Radio button selected."*

### Target Areas
* Radio button size is larger than default settings to provide a larger target area

### Colour Contrast
* [Contrast ratio](https://webaim.org/articles/contrast/) exceeds 7:1 for radio button on white background

## Code
### HTML
```html
    <label class="radio" for="radio_1">One
      <input type="radio" name="foo" id="radio_1">
      <span class="dot"></span>
    </label>

    <label class="radio" for="radio_2">Two
      <input type="radio" name="foo" id="radio_2">
      <span class="dot"></span>
    </label>

    <label class="radio" for="radio_3">Three
      <input type="radio" name="foo" id="radio_3">
      <span class="dot"></span>
    </label>

    <label class="radio" for="radio_4">Four
      <input type="radio" name="foo" id="radio_4">
      <span class="dot"></span>
    </label>
```
 
### CSS
```css

/* Customize the label (the container) */
.radio {
  display: block;
  position: relative;
  padding-left: 30px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 18px;
  font-family: ‘BCSans’, ‘Noto Sans’, Verdana, Arial, sans-serif;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default radio button */
.radio input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

/* Create a custom radio button */
.dot {
  position: absolute;
  top: 1px;
  left: 0;
  height: 18px;
  width: 18px;
  border-radius: 50%;
  border: 2px solid #606060;
}

/* When the radio button is checked, add a blue background */
.radio input:checked ~ .dot {
  background-color: #ffffff;
}

/* Custom checkbox has blue outline when in focus */
.radio input:focus ~ .dot {
  outline: 4px solid #3B99FC;
  outline-offset: 1px;
}

/* Create the indicator (the dot/circle - hidden when not checked) */
.dot:after {
  content: "";
  position: absolute;
  display: none;
  top: 50%;
  left: 50%;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #606060;
  transform: translate(-50%, -50%);
}

/* Show the indicator (dot/circle) when checked */
.radio input:checked ~ .dot:after {
  display: block;
}
```
