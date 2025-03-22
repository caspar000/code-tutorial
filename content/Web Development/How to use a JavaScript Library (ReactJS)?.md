Most code you will encounter is no longer written in basic HTML, CSS and JavaScript. Websites have become quite complicated and require additional tools to make it easier to write certain types of code. For this purpose, some people have developed JavaScript "libraries" which build upon the basic JavaScript and add functionality which makes it easier to code certain parts of a website. 

There are many JavaScript libraries, but we will be using "ReactJS" which is currently the most popular one.

![[JavaScript Library Usage.png]]

To download ReactJS, you have to first install "Node" and "NPM" (Node Package Manager). You can download Node from [here](https://nodejs.org/en/download). You should download the latest LTS (Long Term Support) version. After you install Node, NPM will be automatically installed on your computer.

Instead of creating a folder and manually creating `index.html` and similar files, you will be using a "Bundler" which will automatically create an empty project for you, will all the configuration. We will be using "Vite", which you can learn more about in their documentation [here](https://vite.dev/). 

To create a basic react application run the following command in your terminal:
```bash
npm create vite@latest my-react-app -- --template react
```

Move to the newly created folder in the terminal with the following command:
```bash
cd ./my-react-app
```
And install all the packages that it requires using
```bash
npm install
```

You can now open the Folder in any code editor you like, for example VSCode. The structure will look something like this:
![[React Folder Structure.png]]
- The `node_modules` folder is where all the packages are saved. You don't need to worry about this folder at all. 
- The `public` folder is where all your static assets will be, such as Fonts, Favicon, some Images and so on.
- The `src` folder is where the actual code is located. This is where you will be adding pages, components, functions, styles, and so on. By default, it has an `App.jsx` which is filled with a template code which displays the Vite logo.
- `.gitignore` is a file which is used by the GIT version management system to determine which files should not be tracked for changes. We will go over git a little later.
- `eslin.config.js` contains rules which give you a warning in the editor if you break them. It is not that important for now.
- `index.html` is the Index file where the code from `main.jsx` is inserted into. This is essentially the same kind of `index.html` file that you would create on your own. You can change the title of the page and favicon in this `index` file, as well as add other `<head>` properties such as description and so on.
- `package-lock.json` and `package.json` keep track of what packages you have installed in this project. They will be automatically updated if you install a new package. 
- `README` is a simple readme which tells you how to run the project
- `vite.config.js` is a file which contains configuration for Vite. This is unimportant for now.

Basically, the only folder you are currently interested in is `src`. 

To run the ReactJS project, you can't use the VSCode "Go Live" button. It has it's own server built in which you run from the terminal with the following command:
```bash
npm run dev
```

After you run the command, the terminal will display something like this:
![[npm run dev.png]]

The server will automatically updates when you change the code, and you can visit it in your browser by going to `http://localhost:5173/`, or by CTRL + Clicking the URL in the Terminal.

If you did everything correctly, you should see the following in your browser after running the server:
![[Default Vite + React App.png]]