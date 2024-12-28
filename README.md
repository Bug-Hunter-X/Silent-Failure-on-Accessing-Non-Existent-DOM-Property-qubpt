# Silent Failure on Accessing Non-Existent DOM Property

This repository demonstrates a subtle bug in JavaScript when interacting with the DOM. Accessing a non-existent property of a DOM element will not throw an error in most browsers. This can lead to unexpected behavior and hard-to-debug issues. 

The `bug.html` file shows the problematic code. The `solution.html` file offers a solution by first checking for the existence of the property before attempting to access it.

## Bug Explanation

The bug lies in directly accessing `myDiv.nonExistentProperty` without checking if the property exists.  Modern browsers usually return `undefined` without raising an error, making the problem difficult to spot during development. 

## Solution

The solution involves explicit checks using the `in` operator or optional chaining (`?.`) to ensure that the property exists before attempting to use it.