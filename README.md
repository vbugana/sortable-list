# Sortable List

Display a scrambled list that can be sorted with drag and drop

## Project Specifications

- Create an ordered list (Top 10 richest people)
- Scramble list items randomly
- Allow user to drag and drop an item to a different position
- Button to check if items are in correct order
- Show green for correct order and red for wrong order

## Description

This is App creates a draggable list of the world's richest people and allows the user to reorder the list by dragging and dropping the items. The code randomly sorts the initial order of the list on page load using the Fisher-Yates shuffle algorithm.

It also includes a `check` button that allows the user to check whether the items are correctly ordered.

The code creates a `ul` element with the `id` `draggable-list` and a button element with the `id` `check`.

It then defines an array called `richestPeople` that contains the names of the world's richest people. The code initializes an empty array called `listItems` to store the list items.

The function `createList` generates the list items and adds them to the `draggable-list` `ul` element. It does this by first mapping over the `richestPeople` array and adding a `sort` property to each element with a random value. It then sorts the array based on the `sort` property using the `Array.sort()` method. It then maps over the sorted array and creates an li element for each person, setting the `data-index` attribute to the index of the item in the array. It also sets the innerHTML of the li element to include a span with the item's index, a div with the class `draggable`, and the person's name and an icon for dragging. The function then pushes each li element to the `listItems` array and appends it to the `draggable-list` ul element. Finally, it calls the `addEventListeners` function.

The `addEventListeners` function adds event listeners to the draggable items and the list items. It selects all the elements with the class `draggable` and adds a `dragstart` event listener to each one. It also selects all the list items and adds `dragover`, `drop`, `dragenter`, and `dragleave` event listeners to each one.

The drag and drop functionality is handled by the following functions:

`dragstart`: This function sets the `dragStartIndex` variable to the index of the item being dragged.
`dragenter`: This function adds the `over` class to the item being dragged over.
`dragleave`: This function removes the `over` class from the item being dragged over.
`dragover`: This function prevents the default dragover behavior.
"dragDrop": This function swaps the positions of the dragged item and the item it is dropped onto by calling the `swapItems` function. It also removes the `over` class from the item being dropped onto.
`swapItems`: This function swaps the positions of two list items by first selecting the `draggable` element of each item using the "querySelector" method. It then appends the `draggable` element of the item being dragged to the `draggable` element of the item it is dropped onto, and vice versa.
The `checkOrder` function checks whether the items are correctly ordered by iterating over the `listItems` array and comparing the text content of the `draggable` element in each item to the corresponding element in the `richestPeople` array. If the two values match, it adds the "right" class to the item. If they do not match, it adds the "wrong" class to the item.

Finally, the code adds a `click` event listener to the `check` button that calls the `checkOrder` function when clicked.

## License

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Technologies Used

![HTML 5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

![CSS 3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

![Javascript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 😂 Here is a random joke that'll make you laugh!

![Jokes Card](https://readme-jokes.vercel.app/api)

https://mdb.pushkaryadav.in/generate
