# CSS Styling Inconsistency with :not() and Dynamic Classes

This repository demonstrates a CSS bug related to using the `:not()` pseudo-class with dynamically added and removed classes.  Under certain conditions, particularly when the class is added and removed rapidly, the browser might not correctly update the styling, leading to flickering or inconsistent application of styles.

The `bug.css` file shows the problematic code, and the `bugSolution.css` file provides a potential solution using a different approach.

## Bug Description
The bug stems from a race condition where the browser's rendering engine may not keep up with rapid changes to class attributes. The `:not()` selector might not be immediately updated, resulting in momentary display issues.

## Solution
The solution uses a more straightforward approach, avoiding the `:not()` selector entirely.

## How to reproduce
1.  Open the `index.html` in a browser.
2.  Observe the behaviour, focusing on the moment the class is removed.