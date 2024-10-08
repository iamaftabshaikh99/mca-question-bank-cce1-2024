
# HTML and CSS Answer Bank

## Q1. Explain HTML Page Structure with an Example

### Short Answer:
HTML is a markup language used to structure web pages.

### Detailed Answer:
1. **`<!DOCTYPE html>`**: This element defines the document type and version of HTML (HTML5). It ensures the browser renders the page correctly.
2. **`<html>`**: This is the root element of an HTML document. It encapsulates all other HTML elements.
3. **`<head>`**: The head section contains meta-information about the document, such as the page title and links to stylesheets or scripts.
   - **Common tags in `<head>`**:
     - `<title>`: Specifies the title of the webpage, which appears in the browser's title bar or tab.
     - `<meta charset="UTF-8">`: Defines the character encoding for the webpage to ensure the proper display of content.
4. **`<body>`**: The body contains the visible content of the webpage, such as text, images, and links.
   - **Example elements**:
     - `<h1>`: Represents a heading.
     - `<p>`: Represents a paragraph.

### Example from Professor:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Webpage's Heading</h1>
    <p>Content</p>
  </body>
</html>
```

---

## Q2. Explain formatting tags in HTML with an example

### Short Answer:
Formatting tags in HTML modify the appearance of text.

### Detailed Answer:
1. **`<b>`**: Renders text in bold without implying extra importance. This is used purely for visual styling.
2. **`<i>`**: Italicizes the text. Often used for emphasizing words or for citations of work.
3. **`<u>`**: Underlines the text, useful for indicating hyperlinks or emphasis.
4. **`<strong>`**: Similar to `<b>`, but semantically implies strong importance or urgency to the text.
5. **`<em>`**: Adds emphasis to the text, often displayed in italics, but carries a semantic meaning of importance.

### Example:
```html
<p>This is <b>bold</b> text and this is <i>italic</i> text.</p>
<p>This word is <u>underlined</u> and <strong>important</strong> text.</p>
<p>Using <em>emphasized text</em> helps convey emotion or context.</p>
```

---

## Q3. Explain the different types of lists in HTML with examples

### Short Answer:
HTML provides ordered lists, unordered lists, and definition lists for displaying items in a structured format.

### Detailed Answer:
1. **Ordered List (`<ol>`)**: Displays items in a specific order, typically with numbers or letters. The sequence matters in this case.
   - **Attributes**:
     - `type`: Specifies the numbering format (e.g., `1`, `A`, `a`, `I`, `i`).
     - `start`: Specifies the starting number for the list.
2. **Unordered List (`<ul>`)**: Displays items as bullet points. The order of items doesn't matter here.
3. **Definition List (`<dl>`)**: Displays a list of terms with corresponding descriptions.

### Example:
```html
<h2>Ordered List Example</h2>
<ol type="A">
  <li>First step</li>
  <li>Second step</li>
  <li>Third step</li>
</ol>

<h2>Unordered List Example</h2>
<ul>
  <li>Item one</li>
  <li>Item two</li>
</ul>

<h2>Definition List Example</h2>
<dl>
  <dt>HTML</dt>
  <dd>A markup language for structuring web pages.</dd>
  <dt>CSS</dt>
  <dd>A stylesheet language used to design the appearance of a document.</dd>
</dl>
```

---

## Q4. Explain table structure in HTML with an example

### Short Answer:
Tables in HTML organize data into rows and columns using the `<table>`, `<tr>`, `<th>`, and `<td>` tags.

### Detailed Answer:
1. **`<table>`**: Defines the table and contains all the rows and columns.
2. **`<tr>`**: Each row is represented with a `<tr>` tag.
3. **`<th>`**: Table headers are defined using the `<th>` tag. These are bold and centered by default.
4. **`<td>`**: Table data cells are defined with the `<td>` tag.

### Example:
```html
<table border="1">
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>City</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>30</td>
    <td>New York</td>
  </tr>
  <tr>
    <td>Bob</td>
    <td>25</td>
    <td>Los Angeles</td>
  </tr>
  <tr>
    <td>Charlie</td>
    <td>35</td>
    <td>Chicago</td>
  </tr>
</table>
```

---

## Q5. Explain hyperlinks in HTML with an example

### Short Answer:
Hyperlinks are created using the `<a>` tag and the `href` attribute, linking to external or internal resources.

### Detailed Answer:
1. **`<a>`**: The anchor tag is used to create a hyperlink.
2. **`href`**: Specifies the URL that the hyperlink points to.
3. **`target="_blank"`**: Opens the link in a new tab.
4. **`title`**: Provides a tooltip when hovering over the link.

### Example:
```html
<a href="https://www.example.com" target="_blank" title="Go to Example">Visit Example</a>
```

---

## Q6. Explain images in HTML with an example

### Short Answer:
Images in HTML are embedded using the `<img>` tag with attributes like `src` and `alt`.

### Detailed Answer:
1. **`<img>`**: The tag used to embed an image in a webpage.
2. **`src`**: Specifies the URL or path of the image.
3. **`alt`**: Provides alternative text for the image if it cannot be displayed.
4. **`width` and `height`**: Define the size of the image.

### Example:
```html
<img src="image.jpg" alt="A beautiful scenery" width="600" height="400">
<p>The image demonstrates embedding media using HTML.</p>
```