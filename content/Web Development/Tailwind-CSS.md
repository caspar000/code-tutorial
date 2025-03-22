Tailwind CSS is a library which makes styling a website really fast. Let's say that I want to make a header component, which will have 3 navigation links, and 2 action buttons, like so:
<div style="background: pink; display: flex; justify-content: space-between">
<div style="display: flex; gap: 16px;">
<div style="background: red; padding: 0 10px;">Home</div>
<div style="background: red; padding: 0 10px;">About</div>
</div>
<div style="display: flex; gap: 16px;">
<div style="background: blue; padding: 0 10px;">Sign In</div>
<div style="background: blue; padding: 0 10px;">Register</div>
</div>
</div>

I would have to have a separate style sheet with *at least* the following classes:
```css
header {
  background: pink;
  display: flex;
  justify-content: space-between;
}

.navigation-links {
  display: flex;
  gap: 16px;
}

.navigation-links a {
  background: red;
  padding: 0 10px;
}

.action-buttons {
  display: flex;
  gap: 16px;
}

.action-buttons button {
  background: blue;
  padding: 0 10px;
}
```

Instead, I could have modular classes which help me in certain situations. Instead of repeating `background: blue` in every class that requires it, what if I had a class called `bg-blue` which I would apply to any element that required it? Following the same logic you could rewrite all the css classes like so:
```css
header {
  background: pink;
  display: flex;
  justify-content: space-between;
}

.display-flex {
	display: flex;
}

.gap-16 {
	gap: 16px;
}

.bg-red {
    background: red;
}

.bg-blue {
    background: blue;
}

.padding-0-10 {
  padding: 0 10px;
}
```

Then I would use these classes in the HTML document itself, writing styles that require similar or same properties faster:
```html
<header>
  <div style="display-flex gap-16">
    <div style="bg-red padding-0-10">Home</div>
    <div style="bg-red padding-0-10">About</div>
  </div>
  <div style="display-flex gap-16">
    <div style="bg-blue padding-0-10">Sign In</div>
    <div style="bg-blue padding-0-10">Register</div>
  </div>
</header>
```

This gives me the added benefit of seeing what styles are applied to the tags without looking separately into the css file. It is more readable compared to css file and makes it faster to develop certain applications. 

---

TailwindCSS is a pre-defined library of such CSS classes. It looks something like this:
```html
<div class="flex flex-col items-center gap-6 p-7 md:flex-row md:gap-8 rounded-2xl">
  <div>
    <img class="size-48 shadow-xl rounded-md" alt="" src="/img/cover.png" />
  </div>
  <div class="flex items-center md:items-start">
    <span class="text-2xl font-medium">Class Warfare</span>
    <span class="font-medium text-sky-500">The Anti-Patterns</span>
    <span class="flex gap-2 font-medium text-gray-600 dark:text-gray-400">
      <span>No. 4</span>
      <span>·</span>
      <span>2025</span>
    </span>
  </div>
</div>
```

Which would give you the following result:
![[TailwindCSS Example.png]]

---

<div style="background: pink; display: flex; justify-content: space-between">
<div style="display: flex; gap: 16px;">
<div style="background: red; padding: 0 10px;">Home</div>
<div style="background: red; padding: 0 10px;">About</div>
</div>
<div style="display: flex; gap: 16px;">
<div style="background: blue; padding: 0 10px;">Sign In</div>
<div style="background: blue; padding: 0 10px;">Register</div>
</div>
</div>

To return to the example above, to write the following header with TailwindCSS, you would do it like this:
```html
<div style="bg-pink flex justify-between">
  <div style="flex gap-4">
    <div style="bg-red px-2.5">Home</div>
    <div style="bg-red px-2.5">About</div>
  </div>
  <div style="flex gap-4">
    <div style="bg-blue px-2.5">Sign In</div>
    <div style="bg-blue px-2.5">Register</div>
  </div>
</div>
```

# How to install TailwindCSS?
Make sure you have [Node](https://nodejs.org/en/download) installed on your computer. You can check if you have node installed by running the following command on your terminal:

```terminal
node -v
```

If it returns a value, like `v23.6.0`, then it is installed.

### Work in Progress...