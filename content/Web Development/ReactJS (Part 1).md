React apps are made out of *components*. A component is a re-usable piece of UI (user interface) that has its own logic and appearance. They can be anything from a small button to the entire layout of the page.

A React component is a JavaScript function which returns HTML Markup:
```jsx
function MyButton() {
	return (
		<button>I'm a button</button>	
	)
}
```

This new button function called `MyButton` can now be use in any other component like this:
```jsx
// export default function means that MyApp is the default function to be exported from the file. If you file is App.js and you export default MyApp, you can import it in another file. We will go over such details later.
export default function MyApp() {
	return (
		<div>
			<h1>Welcome to My App</h1>
			<MyButton />
		</div>	
	)
}
```

We differentiate between a normal function and a React component function by capitalizing the first letter. If the function starts with a capital letter, such as in this case `<MyButton />`, than you know that it is a component. Otherwise, a normal function would look like this `myButton()`.

This is how the above code will look when you put it together in a file called `App.js`

```jsx
function MyButton() {
	return (
		<button>I'm a button</button>	
	)
}

export default function MyApp() {
	return (
		<div>
			<h1>Welcome to My App</h1>
			<MyButton />
		</div>	
	)
}
```

And this is what it will look like after you run the code:
![[React Example.png]]

The markup syntax which is returned by the react component functions is called JSX. It has a little more rules compared to normal HTML. For example, when you have a function such as `MyButton()`, you have to return a single JSX parent. Let's say you wanted to have a button with a label:

```jsx
function MyButton() {
	return (
		<label>My Button</label>
		<button>I'm a button</button>
	)
}
```

This will give you an error. Why? Because the function can only return a single HTML tag. In this case, to return both the label and the button at the same time, we just have to wrap the tags in a *Parent* tag, which can be anything, like `<div>` or we could use the special empty tag provided by JSX which is `<></>`:

```jsx
function MyButton() {
	return (
		<>
			<label>My Button</label>
			<button>I'm a button</button>
		</>
	)
}
```

Now it works! Remember this.

How can you add styles to the JSX tags? In normal HTML you could add a style like this:
```html
<button style="myStyle">I'm a button</button>
```

In JSX, you use a property called `className` instead. If you want to add a css class called `myStyle` to the button tag, in JSX you would do it like this:

```jsx
<button className="myStyle">I'm a button</button>
```

This seems arbitrary. Why do we need to use JSX? How does it make our life easier?

JSX becomes very powerful when you want to display some data in your HTML. This would be complicated in a normal HTML project, but in React with the help of JSX it is very simple. Let's say I receive data from the server which gives me information about the current user. The data might be an *Object* with the *Name* of `user` which contains *Key-Value*  pairs such as `name: 'Vasili'` or `email: 'test@email.com'`. I can display this data very easily using JSX:

```jsx
return (
	<h1>
		{user.name}
	</h1>
)
```

The `user` might have a profile picture uploaded to the server. You could access that profile picture from the appropriate key, e.g., `imageUrl`. Instead of manually assigning the path of the image to the `<img>` tag, you can do the following:

```jsx
return (
	<img
		className="profile"
		src={user.imageUrl}
	/>
)
```

Notice, that you assign the `src` property of an image using JavaScript. To do this, you have use brackets `{}` instead of quotes `''`. You can do so with any property. If your classes were assigned programmatically with some called `classes` you could also do the following:
```jsx
return (
	<img
		className={classes}
		src={user.imageUrl}
	/>
)
```

The properties you can assign in JSX can be complicated and very useful. You could manipulate the data, add strings to it, do mathematical operations on it, put it in functions, and output the result in HTML. For example:
```jsx
return (
	<>
		<h1>Hello {user.name} {user.lastname}</h1>
		<p>Your age is {user.age}</p>
		<p>I can do any operation on your age, for example divide it by 5</p>
		<p>{user.age / 5 * 12 - 7}</p>
		<p>I can also put it in a function which might check something</p>
		<p>{isLegallyAllowedToDrink(user.age)}</p>
	</>
)
```