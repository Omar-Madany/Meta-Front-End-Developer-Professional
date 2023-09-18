## `JS DOM`
a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document

##### 1. Main DOM

1. Accessing DOM Elements:

You can access DOM elements using methods like getElementById, getElementsByClassName, getElementsByTagName, and querySelector.
Example:
``````js
const elementById = document.getElementById('myElement');
``````
2. Modifying Element Properties:

You can modify element properties like innerHTML, textContent, style, and className to change content and appearance.
Example:
``````js
const element = document.getElementById('myElement');
element.innerHTML = 'New Content';
element.style.color = 'red';
``````
3. Handling Events:

JavaScript allows you to attach event handlers to DOM elements to respond to user interactions (e.g., clicks, mouseovers).
Example:
``````js
const button = document.getElementById('myButton');
button.addEventListener('click', function() {
  alert('Button Clicked!');
});
``````
4. Creating and Appending Elements:

You can create new DOM elements using document.createElement and append them to the document using methods like appendChild or insertBefore.
Example:
``````js
const newDiv = document.createElement('div');
newDiv.textContent = 'New Div Element';
document.body.appendChild(newDiv);
``````
5. Modifying Element Attributes:

You can change element attributes like src, href, and class to modify their behavior and appearance.
Example:
``````js
const image = document.getElementById('myImage');
image.src = 'new-image.jpg';
``````
6. Traversing the DOM:

JavaScript allows you to navigate and manipulate the DOM tree by accessing parent, child, and sibling elements.
Example:
``````js
const parent = document.getElementById('parentElement');
const firstChild = parent.firstChild;
const nextSibling = firstChild.nextSibling;
``````
7. Removing Elements:

You can remove elements from the DOM using the remove() method.
Example:
``````js
const elementToRemove = document.getElementById('elementToRemove');
elementToRemove.remove();
``````
8. Manipulating CSS:

JavaScript can change CSS styles directly or by modifying element classes.
Example:
``````js
const element = document.getElementById('myElement');
element.style.backgroundColor = 'blue';
element.classList.add('active');
``````

##### 2. Query Selectors

It allows you to find and interact with specific elements on a web page using CSS-style selectors. Here are some key points about querySelector:

1. Selecting Elements:

querySelector allows you to select HTML elements based on CSS-style selectors, such as class names, IDs, element names, attributes, and more.
Example:
``````js
const element = document.querySelector('.myClass'); // Selects the first element with the class "myClass"
``````
2. Selecting by ID:

You can select elements by their id attribute using # followed by the ID.
Example:
``````js
const element = document.querySelector('#myId'); // Selects the element with the ID "myId"
``````
3. Selecting by Element Type:

You can select elements by their HTML tag name.
Example:
``````js
const heading = document.querySelector('h1'); // Selects the first <h1> element on the page
``````
4. Selecting Nested Elements:

querySelector can also be used to select elements within other elements, creating a nested selection.
Example:
``````js
const listItem = document.querySelector('ul li'); // Selects the first <li> element within a <ul>
``````
5. Selecting by Attribute:

You can select elements based on their attributes.
Example:
``````js
const link = document.querySelector('a[href="https://example.com"]'); // Selects <a> elements with a specific href attribute
``````
6. Selecting Multiple Elements:

If you want to select multiple elements that match a selector, you can use querySelectorAll instead.
Example:
``````js
const elements = document.querySelectorAll('.myClass'); // Selects all elements with the class "myClass"
``````
7. Handling Selected Elements:

Once you've selected an element, you can interact with it by changing its content, modifying attributes, adding event listeners, or applying CSS styles.
``````js
// Example: Changing the text content of a selected element
const element = document.querySelector('.myElement');
element.textContent = 'New Content';
``````
