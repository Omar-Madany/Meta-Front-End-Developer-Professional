## `Headings`

allows you to display titles and subtitles in web pages

+ Syntax : 

        <body>
            <h1>Heading 1</h1>
            <h2>Heading 2</h2>
            <h3>Heading 3</h3>
            <h4>Heading 4</h4>
            <h5>Heading 5</h5>
            <h6>Heading 6</h6>
        </body>

+ visual repersentation : 

><body>
><h1>Heading 1</h1>
><h2>Heading 2</h2>
><h3>Heading 3</h3>
><h4>Heading 4</h4>
><h5>Heading 5</h5>
><h6>Heading 6</h6>
></body>
---
## `paragraphs`
are used for displaying text content on a webpage. It is defined by the `<p>`

+ Syntax :

        <p>
            This paragraph
            contains a lot of lines
            but they are ignored.
        </p>

+ visual repersentation : 
  <p>
            This paragraph
            contains a lot of lines
            but they are ignored and you can go an check the code 
        </p>

>**Note** : that putting content on a new line is ignored by the web browser.

---
## `Line Breaks`

`<br/>` tag allows us to add breaks between paragraphs or other elements

+ Syntax :

        <p>
            This paragraph<br>
            contains a lot of lines<br>
            and they are displayed.
        </p>

+ Ex:
<p>
            This paragraph<br>
            contains a lot of lines<br>
            and they are displayed.
</p>

---
## `Strong`

Strong tags can be used to indicate that a range of text has importance.
+ Syntax :

        <p>
        No matter how much the dog barks: <strong> don't feed him chocolate </strong>.
        </p>

+ visual repersentation :

<p>
   No matter how much the dog barks: <strong>don't feed him chocolate</strong>.
</p>

---
## `Bold`
Bold tags can be used to draw the reader's attention to a range of text.
+ Syntax :

        <p>
            The primary colors are <b>red</b>, <b>yellow</b> and <b>blue</b>.
        </p>

+ visual repersentation :

<p>
   The primary colors are <b>red</b>, <b>yellow</b> and <b>blue</b>.
</p>

---
## `emphasis`
Emphasis tags can be used to add emphasis to text.
+ Syntax :

        <p>
        Wake up <em>now</em>!
        </p>

+ visual repersentation :

<p>
   Wake up <em>now</em>!
</p>

---
## `italics`
Italics tags can be used to offset a range of text
+ Syntax :

        <p>
            The term <i>HTML</i> stands for HyperText Markup Language.
        </p>

---
## `list`
- lists used for formatting webpage
- lists specified using the *\<li>* as the body of the list


there are two types of lists:

### **1. Unordered Lists :**

+ Syntax :

        <ul>
                <li>Tea</li>
                <li>Sugar</li>
                <li>Milk</li>
        </ul>

+ visual repersentation :

<ul>
   <li>Tea</li>
   <li>Sugar</li>
   <li>Milk</li>
</ul>

----
### 2.**Ordered List :**

+ syntax :

        <ol>
                <li>Rocky</li>
                <li>Rocky II</li>
                <li>Rocky III</li>
        </ol>

+ visual repersentation :

<ol>
   <li>Rocky</li>
   <li>Rocky II</li>
   <li>Rocky III</li>
</ol>

---
## `Div tags`

A \<div> tag defines a content division in a HTML document. It acts as a generic container and has no effect on the content unless it is styled by CSS.

shows div has a pragraph inside
+ Syntax :

        <div>
           <p>This is a paragraph inside a div</p>
        </div>


+ visual repersentation :

<div>
   <p>This is a paragraph inside a div</p>
</div>

the div has not impact unless you add css code 

+ Syntax :

        <style>
           div {
              border: 1px solid black;
              padding: 2px;
           }
        </style>
        <div>
           <div>
              <p>This is a paragraph inside stylized divs</p>
           </div>
        </div>

+ visual repersentation :

<img align='center' src='https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bVdFeS21TUSXRXkttd1EVw_3cd3c9ca71214bafa65b0144efae3ee1_html_nested_div_with_style.png?expiry=1689724800000&hmac=Rzixwyu2fG01GlXNVCDA2-gHyLUbEWmyNq-VNj2HjgY' >

<br>

---
## `Comments`

If you want to leave a comment in the code for other developers, it can be added as:

        <!-- This is a comment --> 
---
## `Linking`

to make a website you have to link webpages together 
\<a> is the default link tag for HTML

+ Syntax :

        <a href="https://google.com">Google</a>

+ visual repersentation :

<a href="https://google.com">Google</a>

---
## `img` 
use \<img> so you can display photo in a website 
the tag has 2 main attributes :
1. `src` used to display the image
2. `alt` if the image can't be displayed it gives if you a text of the content

+ Syntax :

        <img src="https://i.pinimg.com/564x/7f/12/ec/7f12ec08e16b28c02cd185591be97355.jpg" alt="anime photo">

+ visual repersentation :

<img src="https://i.pinimg.com/564x/7f/12/ec/7f12ec08e16b28c02cd185591be97355.jpg" alt="anime photo" height='100px'>

---
## `Table`
To create tables use `<table>` and to create table content we use :

1. \<th> for the table header 
2. \<tr> for the table content
3. \<td> for the table cells

+ Syntax :

        <table>
            <tr>
                <th>Dish</th>
                <th>Price</th>
            </tr>
            <tr>
                <td>Burger</td>
                <td>$5.99</td>
            </tr>
        </table>

+ visual repersentation :

<table>
        <tr>
        <th>Dish</th>
        <th>Price</th>
        </tr>
        <tr>
        <td>Burger</td>
        <td>$5.99</td>
        </tr>
</table>

---
## `Forms` 
To create a form in HTML, you can use the <form> element along with various form-related input elements to collect user input.

1. \<form> Tag: Use this tag to define a form. It serves as a container for form elements and provides functionality for submitting user input to a server.

2. Form Elements: Within the \<form> tag, you can include different types of form elements, such as input fields, checkboxes, radio buttons, select dropdowns, and more. These elements allow users to enter or select data.

+ Syntax :

        <form action="/submit-form" method="POST">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" placeholder="Enter your name" required>

            <label for="email">Email:</label>
            <input type="email" id="email" name="email" placeholder="Enter your email"  required>

            <label for="message">Message:</label>
            <textarea id="message" name="message" placeholder="Enter your message" rows="4"     required></textarea>

            <input type="submit" value="Submit">
        </form>

+ visual repersentation :

<form action="/submit-form" method="POST">
<label for="name">Name:</label>
<input type="text" id="name" name="name" placeholder="Enter your name" required>

<label for="email">Email:</label>
<input type="email" id="email" name="email" placeholder="Enter your email" required>

<label for="message">Message:</label>
<textarea id="message" name="message" placeholder="Enter your message" rows="4" required></textarea>

<input type="submit" value="Submit">
</form>

---
