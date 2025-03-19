You can view all the properties on the following link:
https://www.w3schools.com/cssref/index.php

You will need to know more properties compared to HTML as they are more frequently used. 

## CSS Structure
In CSS, each code block has a start and an end which are differentiated with *brackets* `{}` and lines are differentiated with *semicolons* `;`. You assign properties with key-value pairs as such `key: value;` So the structure of a document might look like this:
```css
h1 {
	background: #e5e5e5;
}

p {
	color: pink;
}

.class-name {
	padding: 20px;
}
```
If you forget to add `{}`, `:`, or `;` you will get an error.

## Common CSS Properties

`background` - you can set the background color using a *color name*, *rgba*, or *hexadecimal notation*
```css
background: pink;
background: rgba(200, 200, 200, 1);
background: #e5e5e5;
```

<p style="background: pink; color: black;">Example Text</p>

---

`color` - you can set the color of elements using *name, rgba* or *hexadecimal* notation
```css
color: pink;
color: rgba(200, 200, 200, 1);
background: #e5e5e5;
```

<p style="color: pink;">Example Text</p>

---

`font-family` - you can change the font of the text by specifying the name of the font. Some fonts are pre-installed on all computers, such as `Times New Roman`, others have to be included in the CSS file by linking them, or by downloading them from the internet. One of the most common places from where you can link fonts is from [Google Fonts](https://fonts.google.com/)
```css
font-family: 'Times New Roman';
font-family: Monospace;
```

<p>Default Font</p>
<p style="font-family: Courier, 'Times New Roman';">Font in Times New Roman</p>
<p style="font-family: monospace">Monospace font, often used in Programming</p>

---
`height` - you can set the height of the element
`width` - you can set the width of the element
the height can be set with pixels `px`, percents `%`, viewport percents `vh` or `vw`, percentage compared to the root element `rem`

```css
height: 200px; /* Height will be 200 pixels */
height: 80%;   /* Height will be 80% of available space */
height: 50vh;  /* Height will be 50% of the available screen space */
height: 2rem;  /* Height will be base size times 2 */

width: 20px;
width: 80%;
width: 50vw;
width: 2rem;
```

`<div style="background: pink; height:20px; color: black;">Box with 20px Height</div>`
<div style="background: pink; height:20px; color: black;">Box with 20px Height</div>

`<div style="background: pink; height:150px; color: black;">Box with 150px Height</div>`
<div style="background: pink; height:150px; color: black;">Box with 150px Height</div>

`<div style="background: pink; height:150px; width: 200px; color: black;">Box with 150px Height and 200px Width</div>`
<div style="background: pink; height:150px; width: 200px; color: black;">Box with 150px Height and 200px Width</div>

---
`padding` - amount of space between the edge of an element and the content inside it.
```css
padding: 0px; /* There is no padding around the element */
padding: 20px /* There is 20 pixel padding around the element */
```

`<div style="background: pink; color: black; padding: 0px;">Element with 0 Padding</div>`
<div style="background: pink; color: black; padding: 0px;">Element with 0 Padding</div>

`<div style="background: pink; color: black; padding: 20px;">Element with 0 Padding</div>`
<div style="background: pink; color: black; padding: 20px;">Element with 20 Padding</div>

If you only write `padding: number`, the padding will be applied equally on all sides. You can apply different padding amounts to different sides:
```css
padding-left: 20px;
padding-right: 10px;
padding-top: 0px;
padding-bottom: 40px;
```

---

`margin` - amount of space between the edge of an element and the next element which is outside of it. Rules work the same way as padding:
```css
/* Apply margin equaly */
margin: 20px;  
/* Or apply differently */
margin-top: 10px;
margin-bottom: 5px;
margin-left: 15px;
margin-right: 20px;
```

In the case below, we have two elements which are touching each other:
<div style="background: pink; padding: 20px; display: flex;">
<div style="background: red; width: 200px; height:200px; color: black">Red Box with 0 Margin on the Right</div>
<div style="background: blue; width: 200px; height:200px; color: white">Blue Box</div>
</div>

If we want to have the blue box separate from the red box by 20 pixels we will add `margin-right: 20px;` to the red box:
<div style="background: pink; padding: 20px; display: flex;">
<div style="background: red; width: 200px; height:200px; color: black; margin-right: 20px;">Red Box with 20 Margin on the Right</div>
<div style="background: blue; width: 200px; height:200px; color: white">Blue Box</div>
</div>

---
`text-align`: sometimes you want to change the text alignment:
```css
text-align: left;
text-align: center;
text-align: right;
```

By default text is aligned to the left
<div style="background: pink; color: black; padding: 50px;">
align left
</div>

but you can of course change it
<div style="background: pink; color: black; padding: 50px; text-align: center">
align center
</div>

---

`border` - a lot of buttons and elements have a border around them. The border can be full or partial and has many different styles. It is written together with the following syntax:
```css
/* A border with the size of 1px, color of black, and fully solid */
border: 1px black solid; /* size of border, color of border, style of border */
/* A border with the size of 5px, color of pink, and dashed */
border: 5px pink dashed;
```

`<div style="border: 1px black solid;">Example text.</div>`
<div style="border: 1px black solid;">Example text.</div>

`<div style="border: 5px pink dashed;">Example text.</div>`
<div style="border: 5px pink dashed;">Example text.</div>

Borders are very commonly done on buttons to give them visual flare:
<button style="padding: 4px 8px; border-radius: 16px; border: 2px #00838F solid; background: #26C6DA; color: black;">Subscribe</button>

---

`border-radius` - you can change the radius of the border to make them look more rounded. In the same way you can create circles
```css
border-radius: 16px; /* will make all the corners have a 16px radius */
border-radius: 100%; /* will make borders fully rounded */
/* top-left | top-right | bottom-right | bottom-left */
border-radius: 10px 20px 30px 0;
```

<div style="background: pink; height: 150px; width: 150px; color: black; display: flex; align-items: center; justify-content: center;">no radius</div>

`border-radius: 16px`
<div style="background: pink; height: 150px; width: 150px; color: black; display: flex; align-items: center; justify-content: center; border-radius: 16px">16px radius</div>

`border-radius: 100%`
<div style="background: pink; height: 150px; width: 150px; color: black; display: flex; align-items: center; justify-content: center; border-radius: 100%;">100% radius</div>

`border-radius: 10px 20px 70% 0`
<div style="background: pink; height: 150px; width: 150px; color: black; display: flex; align-items: center; justify-content: center; border-radius: 10px 20px 70% 0;">100% radius</div>

---

One of the most useful properties in CSS is `flex`. With `flex`, you can create grid like design, align content to center, create even padding between elements, and so on. You can view detailed examples on how to use flex [here](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

We will go over some of the basic flex properties to get you started:

`flex` - by default, every element is styled in a row. You can change the elements to be styled in a column instead by adding `display: flex`

no flex
<div style="background: pink; padding: 10px;">
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

with `display: flex`
<div style="background: pink; display: flex; padding: 10px">
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

you can control spacing between each element with `gap: number`;

for example, if you want each element to have a gap of 20 pixels between them, you would add `gap: 20px` to the flex element
```css
display: flex;
gap: 20px;
```
<div style="background: pink; display: flex; gap: 20px; padding: 10px">
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

you can change if the boxes are aligned at the start, center, or end by adding `justify-content: flex-start | center | flex-end`

```css
display: flex;
gap: 20px;
justify-content: center
```
<div style="background: pink; display: flex; justify-content: center; gap: 20px; padding: 10px">
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

if you want for the boxes to take up the entire pink area and be evenly spaced between each other, you would do: `justify-content: space-between`
<div style="background: pink; display: flex; justify-content: space-between; padding: 10px">
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
<div style="background: blue; width: 40px; height: 40px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

There are sometimes cases when we have different sizes of components inside a `flex`. For example, like this:
<div style="background: pink; display: flex; gap:20px; padding: 10px;">
<div style="background: blue; width: 80px; height: 80px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

In some cases, we would like those different sized elements to be centered on the same horizontal line. We can do so by adding `align-items: center`
<div style="background: pink; display: flex; gap:20px; padding: 10px; align-items: center">
<div style="background: blue; width: 80px; height: 80px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

If we want the content to be centered on a vertical line we can add `justify-content: center`
<div style="background: pink; display: flex; gap:20px; padding: 10px; justify-content: center">
<div style="background: blue; width: 80px; height: 80px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

you can of course do both at the same time:
<div style="background: pink; display: flex; gap:20px; padding: 10px; justify-content: center; align-items: center">
<div style="background: blue; width: 80px; height: 80px;"></div>
<div style="background: red; width: 40px; height: 40px;"></div>
</div>

This comes very useful when dealing with icons and images. There are a lot of cases where you would have an element like the following, with an icon and a text:
<div style="background:pink; padding: 10px; display:flex; justify-content: center;">
<div style="padding: 2px 6px; display: flex; gap: 8px; border: 2px black solid; border-radius: 16px; width: 160px;">
<div style="background: blue; width: 20px; height: 20px; border-radius: 100%"></div>
<div style="color: black"> Subscribe</div>
</div>
</div>

As you can see the blue "icon" and text is not fully centered unless we do `align-items: center` and `justify-content: center` at the same time
<div style="background:pink; padding: 10px; display:flex; justify-content: center">
<div style="padding: 2px 6px; display: flex; gap: 8px; border: 2px black solid; border-radius: 16px; width: 160px; align-items: center; justify-content: center">
<div style="background: blue; width: 20px; height: 20px; border-radius: 100%"></div>
<div style="color: black"> Subscribe</div>
</div>
</div>

You can use `flex` elements inside of other `flex` elements. This becomes useful when designing Headers, Footers, and other similar components. For example a common Header element might look like this:

<div style="background:pink; display:flex; justify-content: space-between">
<div style="background: red; height: 80px; padding: 0 10px; display: flex; align-items: center; justify-content: center; color: white;">HomePage Link</div>
<div style="background: blue; height: 60px; padding: 10px; display: flex; gap: 16px;">
  <div style="background: lightblue; color: black; display: flex; align-items:center; justify-content: center; padding: 0 10px;"> Button 1</div>
  <div style="background: lightblue; color: black; display: flex; align-items:center; justify-content: center; padding: 0 10px;"> Button 2</div>
</div>
</div>

It has one `flex` element for the header group itself, which spaces between two groups. The red group contains a link or an image, while the other group contains buttons, usually "Sign In" and "Register". The Blue group is also `flex` and has a gap of 16 pixels. The code for the above example can be seen below:

```html
<!-- This is the Header element which has flex and space-between -->
<header
  style="
    background:pink; 
    display:flex; 
    justify-content: space-between;
  "
>
  <!-- This is the "RED" group, which only contains text -->
  <div 
    style="
      background: red; 
      height: 60px; 
      padding: 0 10px; 
      display: flex; 
      align-items: center; 
      justify-content: center;
    "
  >
    HomePage Link
  </div>
  <!-- This is the "BLUE" group, which is also a flex and contains two buttons -->
  <div 
    style="
      background: blue; 
      height: 60px; 
      padding: 10px; 
      display: flex; 
      gap: 16px;
    "
   >
     <div 
       style="
         background: lightblue; 
         color: black; 
         display: flex; 
         align-items:center; 
         justify-content: center; 
         padding: 0 10px;
        "
      >
      Button 1
      </div>
     <div 
       style="
         background: lightblue; 
         color: black; 
         display: flex; 
         align-items:center; 
         justify-content: center; 
         padding: 0 10px;
        "
      >
      Button 2
      </div>
  </div>
</header>
```

Another common pattern, is when you have a "grid" of elements like the example below:
<div style="background: pink; padding: 10px;">
<div style="display:flex; gap:20px;">
<div style="background: blue; width: 100%; height: 200px;"></div>
<div style="background: blue; width: 100%; height: 200px;"></div>
</div>
</div>

```html
<div style="background: pink; padding: 10px;">
  <div style="display:flex; gap:20px;">
    <div style="background: blue; width: 100%; height: 200px;"></div>
    <div style="background: blue; width: 100%; height: 200px;"></div>
  </div>
</div>
```
All you need to do is set the width of the element to be 100% and have a gap property. You can do this for as many elements as you like, for example 5:
<div style="background: pink; padding: 10px;">
<div style="display:flex; gap:20px;">
<div style="background: blue; width: 100%; height: 200px;"></div>
<div style="background: blue; width: 100%; height: 200px;"></div>
<div style="background: blue; width: 100%; height: 200px;"></div>
<div style="background: blue; width: 100%; height: 200px;"></div>
<div style="background: blue; width: 100%; height: 200px;"></div>
</div>
</div>