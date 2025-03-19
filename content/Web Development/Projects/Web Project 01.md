You will have to develop the following project in HTML and CSS.

![[Main.png]]

You can access the Figma file of the project [here](https://www.figma.com/design/344GbSxZ6hi1uFOF88IpUn/HTML-and-CSS-Study-Project?node-id=0-1&t=yhkCfacvfBCnJj3W-1)

Your project structure should look like this:
```
PROJECT (folder)
  ASSETS (folder)
    - icon.svg
  - index.html
  - style.css
```

You should link the HTML and CSS files with in the `<head>` tag.
`<link rel="stylesheet" href="style.css">`

You can download the icon as an SVG or PNG file from Figma. Use the `<img>` tag when adding the icon to the project.

You can add custom fonts to your CSS file from [Google Fonts](https://fonts.google.com/) by choosing a font, clicking "Get font > Get embed code > @import > copy code"

For example, the code for Roboto @import will look like this:
```
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');
</style>
```

You have to copy the `@import` part into you CSS file and add it as a Font Family:
```css
/* style.css */

@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');

.font-roboto { 
  font-family: "Roboto", sans-serif; 
  font-weight: auto; 
  font-style: normal; 
}
```

Then you can assign it to your whole document, or som other parts with a class
```css
/* style.css */

@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');

.font-roboto { 
  font-family: "Roboto", sans-serif; 
  font-weight: auto; 
  font-style: normal; 
}

body {
  font-family: "Roboto", sans-serif;
}

/* OR add style="font-roboto" to any element */
```
