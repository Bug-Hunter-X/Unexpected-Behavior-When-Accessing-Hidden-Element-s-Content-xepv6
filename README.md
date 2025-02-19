# Uncommon HTML Bug: Accessing Hidden Element's Content

This repository demonstrates an uncommon bug related to accessing the content of an HTML element after it has been hidden using JavaScript.  The bug arises from attempting to access the `innerHTML` (or other properties) of a DOM element after setting its `display` style to `none`. While seemingly straightforward, it can lead to unexpected behavior, ranging from silent failures to explicit error messages, depending on the browser and subsequent operations.

## Bug Description

The bug occurs when an HTML element is hidden using `element.style.display = "none";`, but code later attempts to access the content of that hidden element. This scenario can result in unexpected errors or inconsistent behavior across different browsers. This is not a standard error and could be easily overlooked.

## How to Reproduce

1. Open the `bug.html` file in your web browser.
2. Observe the console. You may get an error, or the console output might be unexpected.

## Solution

The solution involves checking if the element exists before accessing its content, even after it is hidden.  The `bugSolution.html` file demonstrates the corrected code.
