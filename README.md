# Number Sorter

An interactive JavaScript application that allows users to select five numbers and sort them in ascending order.  
Built to practice array manipulation, numeric comparison logic, and classic sorting algorithm implementations.

## Live Demo
https://sharpsanders.github.io/number-sorter/

![Number Sorter Screenshot](./img/Screenshot-number-sorter.png)

---

## Overview

The application provides:

- Five dropdown inputs (values 0–9)
- A Sort button
- A dynamic output display showing the sorted array

Default input values: `[8, 2, 4, 1, 3]`  
Example output: `[ 1, 2, 3, 4, 8 ]`

---

## Features

- Five selectable numeric inputs (0–9)
- Converts form values from strings to numbers
- Sorts values in ascending order
- Updates the UI dynamically without page reload
- Responsive layout for desktop and mobile

### Sorting Logic

The UI currently uses JavaScript’s built-in `Array.sort()` with a numeric comparison function:

```js
const sortedValues = inputValues.sort((a, b) => a - b);
In addition, the project includes manual implementations of:

Bubble Sort

Selection Sort

Insertion Sort

These are included for algorithm practice and comparison purposes.

Technical Highlights
Uses spread syntax and Array.map() to collect dropdown values

Prevents default form submission behavior with event.preventDefault()

Implements a proper numeric compare function to avoid lexicographical sorting errors

Separates UI update logic into a dedicated updateUI() function

Includes standalone sorting algorithm implementations written from scratch

Tech Stack
HTML5

CSS3

JavaScript (ES6+)

No external libraries or frameworks.

Project Structure
number-sorter/
  index.html     # Markup and form structure
  styles.css     # Layout and UI styling
  script.js      # Sorting logic and DOM interaction
How to Run Locally
Clone the repository:

git clone https://github.com/SharpSanders/number-sorter.git
cd number-sorter
Open index.html in your browser.

Optional: Use VS Code Live Server during development.

What This Project Demonstrates
DOM selection and value extraction

Converting form input values into numbers safely

Implementing and comparing multiple sorting algorithms

Proper numeric sorting using a custom compare function

Updating UI elements dynamically based on user input

Future Improvements
Allow dynamic number of inputs

Add algorithm selection toggle (built-in vs custom)

Visualize sorting steps

Add automated tests for each sorting function

Author
Trevyn Sanders
Better Endeavors LLC