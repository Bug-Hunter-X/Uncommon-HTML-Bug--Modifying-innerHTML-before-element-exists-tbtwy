# Uncommon HTML Bug: Modifying innerHTML Before Element Exists

This repository demonstrates a subtle but important bug in HTML and JavaScript interaction. The bug arises when attempting to modify the `innerHTML` property of an element before the element is fully parsed and added to the Document Object Model (DOM).  This can lead to unexpected behavior or errors.

## Bug Description

The `bug.html` file contains a simple HTML structure with a `<div>` element and a JavaScript script. The script tries to change the `innerHTML` of the `div` before the browser has finished parsing and rendering it. This results in the modification failing to take effect.

## Solution

The `bugSolution.html` file provides a corrected version using the `DOMContentLoaded` event. This event ensures the script executes only after the HTML document is fully parsed and ready, guaranteeing the element exists and can be safely manipulated.

This demonstrates the importance of understanding the order of execution between HTML parsing and JavaScript execution, and using appropriate event listeners to ensure reliable DOM manipulation.