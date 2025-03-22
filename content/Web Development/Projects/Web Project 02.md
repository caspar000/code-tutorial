This project will be a continuation of the previous project. I have added a new page to the [Figma](https://www.figma.com/design/344GbSxZ6hi1uFOF88IpUn/HTML-and-CSS-Study-Project?node-id=0-1&t=Mkc8QPlAjfbazIDp-1)document which you will have to develop. The new page looks like this:

![[Project Image 02.png]]

You have to add a new link to the header which will take you to the "About" page. On the "Home" page, the link with the name "Home" will have a border on the bottom and "About" will not. When going to "About" it will be the opposite.

This page has some components which are the same as in the "Home" page. This is a very common on large websites. In the future, you will write such code in "Components", but for now you can copy your existing code to the new page and change it as it is required.

You can create a new page in your folder by calling it something like `about.html`. The `about.html` will have mostly the same structure as `index.html`, but the section between the `<header>` and the `<footer>` will be different. 

You can link to the second page from `index.html` by inserting it in a `<a href="">About</a>` tag. For example:
```html
<a href="about.html">About</a>
```

This is a preparation for the next Project, which will be re-writing this application in ReactJS. In ReactJS, instead of copying code, you will write a component, which you can reuse on different parts of the website.