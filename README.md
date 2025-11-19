# Number Sorter

A small interactive tool that lets you choose five numbers from dropdowns and then sorts them in ascending order. Built to practice array methods, comparison functions, and classic sorting algorithms in JavaScript.

## Demo

The UI shows:

- A title: **Number Sorter**
- An **Input** section:
  - Five dropdowns, each with values from `0` to `9`
  - Default values: `[8, 2, 4, 1, 3]`
- A **Sort** button
- An **Output** section that displays the sorted array, like:

```text
[ 1, 2, 3, 4, 8 ]
Tech Stack
HTML – structure for the inputs, button, and output.

CSS – layout, spacing, and styling consistent with the freeCodeCamp theme.

JavaScript – reading form values, sorting, and updating the UI.

Features
Five dropdowns to select numbers between 0 and 9.

On Sort, the app:

Reads the selected values.

Converts them to numbers.

Sorts them in ascending order.

Updates the output display.

Responsive layout that stays centered and readable on small and large screens.

Includes implementations of three classic sorting algorithms:

Bubble sort

Selection sort

Insertion sort

(Only the built-in Array.sort is wired to the UI right now; the other algorithms are there as learning/reference code.)

How to Run the Project
Clone the repository:

bash
Copy code
git clone https://github.com/SharpSanders/number-sorter.git
cd number-sorter
Open the app:

Option A: Double-click index.html to open it in your browser.

Option B (recommended while developing): Use the Live Server extension in VS Code and open index.html via Live Server.

You should see the Number Sorter interface with five dropdowns and the Sort button.

How to Use
Use each dropdown under Input to pick the numbers you want.

Click the Sort button.

The Output section will update to show the numbers sorted in ascending order.

You can change the dropdown values and hit Sort again as many times as you want.

How It Works (JavaScript Overview)
All logic lives in script.js.

Main flow
sortButton references the Sort button.

sortInputArray(event):

Calls event.preventDefault() to stop the form submitting.

Collects the values of all elements with the class .values-dropdown:

js
Copy code
const inputValues = [
  ...document.getElementsByClassName("values-dropdown")
].map((dropdown) => Number(dropdown.value));
Sorts them using the built-in Array.sort with a numeric comparison:

js
Copy code
const sortedValues = inputValues.sort((a, b) => a - b);
Calls updateUI(sortedValues) to display the result.

updateUI(array):

Loops through the sorted array.

For each index i, sets the text of #output-value-i to the sorted number.

This updates the output [ 0, 0, 0, 0, 0 ] into the actual sorted list.

Classic Sorting Algorithms (for learning)
The file also contains three standalone sorting implementations:

bubbleSort(array)

selectionSort(array)

insertionSort(array)

Each function:

Takes an array of numbers.

Mutates it in place to sort it.

Returns the sorted array.

These functions aren’t wired to the UI, but they’re useful for practicing and comparing against the built-in sort method.

Project Structure
text
Copy code
number-sorter/
├── index.html   # Markup for the title, form, and output display
├── styles.css   # Styling and layout for the sorter UI
└── script.js    # Sorting logic, DOM interaction, and classic algorithms
What I Practiced
Selecting DOM elements and reading their values.

Converting string values from form controls into numbers.

Using spread syntax and Array.map.

Sorting numbers correctly with a custom compare function.

Implementing bubble sort, selection sort, and insertion sort by hand.

Updating the UI dynamically based on user interaction.

Future Improvements
Allow the user to:

Choose how many numbers to sort.

Pick which sorting algorithm to use (built-in vs bubble/selection/insertion).

Show a step-by-step visualization of each sorting algorithm.

Add error handling for invalid inputs or duplicated IDs.

Add tests for each sorting function.

Author
Created by Trevyn Sanders.