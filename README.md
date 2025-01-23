# Uncommon HTML Error: Incorrect Text Content Access

This repository demonstrates a subtle error in accessing and manipulating the text content of an HTML element.  The issue arises from a misunderstanding of how the `textContent` property works when assigning a new value.

The `bug.html` file contains the erroneous code, and `bugSolution.html` provides the correct implementation.  The core problem involves using `textContent` in a way that might overwrite existing content without proper retrieval of the original value.

## Problem

The primary error lies in the JavaScript code.  The intent is to access the existing text content of an element and possibly log it or perform other manipulations. However, the assignment of the new text directly in the `textContent` property replaces the previous content, and the variable assigned to the `textContent` property will return the *new* value rather than the *old* value.

## Solution

The solution involves storing the original value before modifying the `textContent` property.