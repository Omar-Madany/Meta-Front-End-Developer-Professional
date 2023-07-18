# Selectors <a href="selector">
<div id="selector">
## `Element Selector`
The element selector allows developers to select HTML elements based on their element type.

+ Syntax :

*HTML*

    <p>Once upon a time...</p>
    <p>In a hidden land...</p>

*CSS*

    p { 
      color: blue; 
    }

---
## `ID Selector`
The ID selector uses the id attribute of an HTML element. Since the id is unique within a webpage, it allows the developer to select a specific element for styling. ID selectors are prefixed with a # character.

+ Syntax :

*HTML*

    <span id="latest">New!</span>

*CSS*

    #latest { 
      background-color: purple; 
    }

##  `Class selector`
The CSS rule has been applied to all elements with the specified class name. The class selector is prefixed with a . character.

+ Syntax :

*HTML*

    <a class="navigation">Go Back</a>
    <p class="navigation">Go Forward</p>

*CSS*

    .navigation { 
      margin: 2px;
    }

## `Element with class selector`
A more specific method for selecting HTML elements is by first selecting the HTML element, then selecting the CSS class or ID.

+ Syntax :

*HTML*

    <p class="introduction"></a>

*CSS*

    p.introduction { 
      margin: 2px;
    }
---
## `Descendant Selector`
Selects all elements that are descendants of a specified element, Class or ID

+ Syntax :

*HTML* 

    <div id="blog">
      <h1>Latest News</h1>
      <div>
        <h1>Today's Weather</h1>
        <p>The weather will be sunny</p>
      </div>
      <p>Subscribe for more news</p>
    </div>
    <div>
      <h1>Archives</h1>
    </div>

*CSS*

    #blog h1 {
      color: blue;
    }

The CSS rule will select all h1 elements that are contained within the element with the ID blog

---
## `Child Selector`
Selects only direct children of an HTML tag and ignores any nested child tags inside it.

+ Syntax :

*HTML*

    <div id="blog">
      <h1>Latest News</h1>
      <div>
        <h1>Today's Weather</h1>
        <p>The weather will be sunny</p>
      </div>
      <p>Subscribe for more news</p>
    </div>

*CSS*

    #blog > h1 {
      color: blue;
    }

>**NOTE**:that this will not go beyond a single depth level. Therefore, the CSS rule will not be applied to the h1 element containing the text Today's Weather

---
## `:hover Pseudo-class`
Changes styles when a user hovers over or clicks on certain parts of your webpage, such as links

+ Simple Syntax :

*CSS*

    a:hover {
      color: orange;
    }
---
</div>
---
