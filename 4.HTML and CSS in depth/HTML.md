# Sectioning tags 

## `Header`

Syntax: 
``````html 
<header>...</header>
``````
Usage: The \<header> element typically contains introductory content, such as a logo, website title, and main navigation links.
Example:
``````html
<header>
  <h1>My Website</h1>
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/contact">Contact</a></li>
    </ul>
  </nav>
</header>
``````
## `Navigation`

Syntax: 
``````html
<nav>...</nav>
``````
Usage: The \<nav> element is used to define the main navigation of a website. It often appears within the \<header> element.
Example:
``````html
<nav>
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/about">About</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>
</nav>
``````
## `Main Content` 

Syntax: 
``````html
<main>...</main>
``````
Usage: The \<main> element represents the primary content of a web page. It should be unique to each page and exclude repetitive content like headers and footers.
Example:
``````html
<main>
  <h1>Welcome to My Website</h1>
  <p>This is the main content of the page.</p>
  <!-- Other content goes here -->
</main>
``````
## `Footer`

Syntax: 
``````html
<footer>...</footer>
``````
Usage: The \<footer> element typically contains information like copyright notices, contact details, or additional navigation links.
Example:
``````html
<footer>
  <p>&copy; 2023 My Website</p>
  <p>Contact: <a href="mailto:contact@example.com">contact@example.com</a></p>
</footer>
``````
## `Article `

Syntax: 
``````html
<article>...</article>
``````
Usage: The \<article> element represents a self-contained composition, such as a blog post, news article, or comment. It can be used within the <main> element.
Example:
``````html
<article>
  <h2>Blog Post Title</h2>
  <p>By John Doe | Published on July 15, 2023</p>
  <p>This is the content of the blog post.</p>
</article>
``````
## `Section`

Syntax: 
``````html
<section>...</section>
``````
Usage: The \<section> element defines distinct sections within an article or a web page. It helps organize content into meaningful blocks.
Example:
``````html
<section>
  <h3>Section Heading</h3>
  <p>This is the content of the section.</p>
</section>
``````
## `Aside`
Syntax:
``````html
<aside>...</aside>
``````
Usage : \<aside> A secondary set of content that is not required to understand the main content.

Example:
``````html
<aside>
    <h3>side contents</h3>
    <img src="/images/sidebar-image.jpg" alt="">
    <a href="/images/sidebar-image">click me</a>
</aside>
``````
## `details`
Syntax:
``````html
<details></details>
``````
Usage : The details element creates a disclosure widget in which information can be hidden or shown (depending upon the user's interaction with the page).
Example:
``````html
    <details>
        <!-- The summary element provides a clickable label for the section -->
        <summary>Click to Expand</summary>
        <!-- Content inside the details element -->
        <p>This is some hidden content that can be expanded or collapsed by clicking the label above.</p>
    </details>
``````
>**Note** : any other missed elements have been defined in HTML tags.md file in introduction to Front-end development folder
---
# containing elements
## `blockquote`
\<blockquote>: Used to describe a quotation.

``````html
<blockquote>
    This is a quoted text that may span multiple lines and is usually indented for readability.
</blockquote>
``````
## `description details`
\<dd>: Used to define a description for the preceding \<dt> element.

``````html
<dl>
    <dt>Term</dt>
    <dd>Description of the term.</dd>
</dl>

``````
##  `Description list`
\<dl>: Used to define a description list.
``````html
<dl>
    <dt>Term 1</dt>
    <dd>Description of Term 1</dd>
    <dt>Term 2</dt>
    <dd>Description of Term 2</dd>
</dl>
``````
## `Description term`
\<dt>: Used to describe terms inside \<dl> elements (used in conjunction with \<dd>).

``````html
<dl>
    <dt>Term 1</dt>
    <dd>Description of Term 1</dd>
    <dt>Term 2</dt>
    <dd>Description of Term 2</dd>
</dl>
``````
## `figcaption`

\<figcaption>: Defines a caption for a photo image.

``````html
<figure>
    <img src="image.jpg" alt="An example image">
    <figcaption>Caption for the image.</figcaption>
</figure>
``````
## `Figure`

\<figure>: Applies markup to a photo image.

``````html
<figure>
    <img src="image.jpg" alt="An example image">
    <figcaption>Caption for the image.</figcaption>
</figure>
``````
## `hr`

\<hr>: Adds a horizontal line to the parent element.

``````html
<p>This is some text above the horizontal line.</p>
<hr>
<p>This is some text below the horizontal line.</p> 
``````

## `menu`
\<menu> :A semantic alternative to \<ul> tag.
``````html
<menu>
    <li><a href="#">Home</a></li>
    <li><a href="#">About Us</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Portfolio</a></li>
    <li><a href="#">Contact</a></li>
</menu>
``````

## `pre`
\<pre>Used to represent preformatted text. Typically rendered in the web browser using a monospace font

``````html
    <pre>
        This is an example of preformatted text.
        It retains both spaces and line breaks exactly as you type them.
        
        It's often used for code examples, ASCII art, or any text that needs to maintain its formatting.
        
        You can use tabs or spaces for indentation, and they will be preserved.
        
        <a href="#">This is a link</a>
        <strong>This is bold text</strong>
    </pre>
``````
## `abbreviation`
\<abbr> Specifies that the containing text is an abbreviation or acronym.
``````html
The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.
``````
## `cite`
Defines the title of creative work (for example a book, poem, song, movie, painting or sculpture). The text in the \<cite> element is usually rendered in italics.

``````html
<p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
``````
## `code`
\<code>:Indicates that the containing text is a block of computer code.
``````html
<p>You may want to take a look at this function: <code>myFunction()</code>.</p>
``````
## `data`
\<data>:Specifies additional data associated with the content of its parent element.
``````html
<ul>
  <li><data value="21053">Cherry Tomato</data></li>
  <li><data value="21054">Beef Tomato</data></li>
  <li><data value="21055">Snack Tomato</data></li>
</ul>
``````
## `emphasize`
\<em> Emphasizes the containing text.
``````html
<p>This is <em>emphasized text</em> within a paragraph.</p>
``````
## `italics`
\<i> The containing text is displayed in italics. Used to indicate idiomatic text or technical terms.
``````html
<p>My mother has always told me that I'm very smart<i >I never thought</i> she'd say things like that!</p>
``````
## `marker`
\<mark> The containing text should be marked or highlighted.
``````html
<p>This is <mark>highlighted text</mark> within a paragraph.</p>
``````
## `quotation`
\<q> The containing text is a short quotation.
``````html
<p>He said, <q>This is a short quotation</q>.</p>
``````
## `strike`
\<s> Displays the containing text with a strikethrough or line through it.
``````html
<p>This is <s>strikethrough text</s> within a paragraph.</p>
``````
## `sample`
\<samp> The containing text represents a sample.
``````html
<p>The output of the command is <samp>sample text</samp>.</p>
``````
## `small`
\<small> Used to represent small text, such as copyright and legal text.
``````html
<p><small>This is small text.</small></p>
``````
## `time`
\<time> - Displaying Dates and Times:

``````html
<p>The event starts at <time datetime="2023-09-15T14:30:00Z">2:30 PM on September 15, 2023</time>.</p>
``````
## `underline`
\<u> - Underlined Text:

``````html
<p>This is <u>underlined text</u> within a paragraph.</p>
``````
## `variable`
\<var> - Variables in Mathematical Expressions:

``````html
<p>The formula for calculating area is <var>A = πr²</var>.</p>
``````
----------------------------------------------------------------
# Media tags
## `audio`
\<audio> - Embedding Audio:

``````html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
``````
## `canvas`
\<canvas> - Rendering Graphics:

``````html
<canvas id="myCanvas" width="200" height="100"></canvas>
``````
## `iframe`
\<iframe> - Embedding a Nested Web Page:

``````html
<iframe src="https://www.example.com"></iframe>
``````
## `img`
\<img> - Embedding an Image:

``````html
<img src="image.jpg" alt="Description of the image">
``````
## `video`
\<video> - Embedding a Video:

``````html
<video controls>
  <source src="video.mp4" type="video/mp4">
  Your browser does not support the video element.
</video>
``````
## `svg`
\<svg> - Scalable Vector Graphics:

``````html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="black" stroke-width="2" fill="red" />
</svg>
``````
----------------------------------------------------------------
# Meta
## `Basic Meta Tags (For SEO)`

\<meta name="description" content="Your brief page description"/>

Attribute: name, content
Explanation: Describes the content of the webpage in a brief manner.
Example:
``````html
<meta name="description" content="A comprehensive guide to meta tags in HTML."/>
``````
\<meta name="title" content="Your Page Title"/>

Attribute: name, content
Explanation: Specifies the title of the webpage.
Example:
``````html
<meta name="title" content="HTML Meta Tags Cheat Sheet"/>
``````
\<meta name="author" content="Author's Name"/>

Attribute: name, content
Explanation: Indicates the author of the webpage.
Example:
``````html
<meta name="author" content="John Doe"/>
``````
\<meta name="language" content="english"/>

Attribute: name, content
Explanation: Specifies the language of the webpage.
Example:
``````html
<meta name="language" content="english"/>
``````
## `Additional SEO Meta Tags`

\<meta name="robots" content="index,follow"/>

Attribute: name, content
Explanation: Informs search engines on how to crawl or index a certain page.
Example:
``````html
<meta name="robots" content="index,follow"/>
``````
\<meta name="google"/>

Attribute: name
Explanation: Indicates to Google not to show the sitelinks search box for your page.
Example:
``````html
<meta name="google"/>
``````
\<meta name="googlebot" content="notranslate"/>

Attribute: name, content
Explanation: Informs Google not to provide an automatic translation for your page.
Example:
``````html
<meta name="googlebot" content="notranslate"/>
``````
\<meta name="revised" content="Sunday, July 18th, 2022, 5:15 pm"/>

Attribute: name, content
Explanation: Specifies the last modified date and time of the page.
Example:
``````html
<meta name="revised" content="Sunday, July 18th, 2022, 5:15 pm"/>
``````
<meta name="rating" content="safe for all"/>

Attribute: name, content
Explanation: Specifies the expected audience for your page.
Example:
``````html
<meta name="rating" content="safe for all"/>
``````
\<meta name="copyright" content="Copyright 2022"/>

Attribute: name, content
Explanation: Specifies copyright information.
Example:
``````html
<meta name="copyright" content="Copyright 2022"/>
``````
## `HTTP-Equiv Meta Tags`

\<meta http-equiv="content-type" content="text/html"/>

Attribute: http-equiv, content
Explanation: Specifies the format of the document returned by the server.
Example:
``````html
<meta http-equiv="content-type" content="text/html"/>
``````
\<meta http-equiv="refresh" content="30"/>

Attribute: http-equiv, content
Explanation: Specifies the duration of the page before it's considered stale.
Example:
``````html
<meta http-equiv="refresh" content="30"/>
``````
\<meta http-equiv="Cache-Control" content="no-cache"/>

Attribute: http-equiv, content
Explanation: Instructs the browser how to cache your page.
Example:
``````html
<meta http-equiv="Cache-Control" content="no-cache"/>
``````
## `Responsive Design/Mobile Meta Tags`
``````html
<meta name="format-detection" content="telephone=yes"/>
``````
Attribute: name, content
Explanation: Indicates that telephone numbers should appear as hypertext links.
Example:
``````html
<meta name="format-detection" content="telephone=yes"/>
``````
\<meta name="HandheldFriendly" content="true"/>

Attribute: name, content
Explanation: Specifies that the page can be properly visualized on mobile devices.
Example:
``````html
<meta name="HandheldFriendly" content="true"/>
``````
\<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

Attribute: name, content
Explanation: Specifies the area of the window in which web content can be seen.
Example:
``````html
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
``````
