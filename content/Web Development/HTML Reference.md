## HTML Tags
You can see all the HTML Tags on the following link:
https://www.w3schools.com/tags/

You won't need all of the tags listed in the reference. There are the main tags that are used the most frequently:

Structural HTML Tags
- `<html>` - specify where HTML starts
- `<head>` - contains head elements such as title, style, and meta tags
- `<title>` - defines the title
- `<body>` - defines the body where images, tables, and so on exist

Semantic HTML Tags 
None of these tags have any special function except to make it easier to identify what part of the page you are working on. You can write every single one of these as a `<div>`. It's only here for semantic structure
- `<header>` 
- `<nav>`
- `<section>`
- `<article>`
- `<aside>`
- `<footer>`

Most Common HTML Tags
- `<div>` - defines a division in an HTML document (a group)
- `<p>` - paragraph
- `<a>` - hyperlink
- `<img>` - image
- `<ul>` - unordered list
- `<ol>` - ordered list
- `<li>` - list item
- `<table>` - table
- `<tr>` - table row
- `<th>` - table header
- `<td>` - table data
- `<form>` - HTML form for user input
- `<input>` - input control within a form
- `<button>` - clickable button
- `<h1>-<h6>` - headings of different levels
- `<span>` - generic inline container
- `<label>` - label for input element
- `<iframe>` - embedded frame for external content

This is how you usually start an HTML file
```html
<!DOCTYPE html>  
<html>  
<head>
  <!-- Your CSS file can be linked here -->
  <link rel="stylesheet" href="style.css">
</head>
<body>  
<!-- Your Web Application content Goes Here -->



</body>  
  <!-- Your JavaScript file can be linked here -->
  <script src="scripts.js"></script>
</html>
```

If your document has a header, main section, and footer, you would do it like this:
```html
<!DOCTYPE html>  
<html>  
<head>
  <link rel="stylesheet" href="style.css">
</head>
<body>  
  <header>Header</header>
  <section>Main Section</section>
  <footer>Footer</footer>
</body>  
  <!-- Your JavaScript file can be linked here -->
  <script src="scripts.js"></script>
</html>
```