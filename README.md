# Uncommon HTML Bug: Accessing Non-Existent Element

This repository demonstrates a subtle yet problematic bug in HTML/JavaScript code.  The bug arises from trying to manipulate the `innerHTML` property of an element that does not exist in the DOM.

## Bug Description

The `bug.html` file contains JavaScript code that attempts to access an element with the ID "nonExistentElement."  Because this element is not defined in the HTML, the `getElementById` method returns `null`, and attempting to access `innerHTML` of a null object throws an error in the browser's console.

## Solution

The `solution.html` file demonstrates the corrected code.  Before manipulating the element's `innerHTML`, it checks if the element actually exists using a conditional statement.  If the element doesn't exist, an appropriate action (such as logging a warning or gracefully handling the error) is taken instead of throwing an exception.

This simple yet important check helps prevent runtime errors and makes the code more robust.