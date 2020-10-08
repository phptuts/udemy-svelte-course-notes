
1) Open visual studio code to the project folder you are going to use for your tip calculator.

2) Open a terminal on visual studio code 


3) Type in npx degit command to clone the sveltes/template repo into your project folder 

```bash
npx degit sveltejs/template .
```

4) Type in npm install to install the dependencies
```bash
npm install 
```

5) Then type in npm run dev to start the website

```bash
npm run dev
```

6) Go to your local website, localhost:3000 and make sure that svelte is running.

## Svelte Overview

1. Open the package.json file.  

2. Notice that svelte is a dev dependency.  This means that the whole svelte library does not ship with your app.  Svelte will only include the parts of it's library you need when compiling your application.

3. Also note that the three commands in your package.json, dev, build, and start.

  - Start will serve the index.html file in the public folder
  - Dev will serve the index.html file in the public folder and will recompile your application when it changes.  This is because we are passing -w which means watch.
  - Build is for building your app for production.
 

```json
"scripts": {
    "build": "rollup -c",
    "dev": "rollup -c -w",
    "start": "sirv public"
  },
```

## Rollup

Open up the rollup.config.js file.  This is where svelte gets compiled. The starting point for your svelte app is src/main.js.  Your app javascript will be compile into a file called bundle.js and your css will be compiled into a file called bundle.css.

Open up source folder and you will see the main.js file.  This is the entry point in your application.  The App component is being passed a prop named "name".  Go ahead change the prop store your name as it's value.  This will changes page to Hello {YourName}.  Look at the target being passed into the App component.  In the App Component we are targeting the body element.  This means that the App.svelte component will control the body of the page.

Open the App.svelte file.  It's taking in prop name and showing that on the page.  This is why the page now says Hello {Yourname}.  Note all components will go into the src folder.

Open up the public folder.  Here you will find the index.html, global.css files and the build folder we talked about previously. The global.css is just a css file no magic there.  Same for our index.html.  These files already have link and script tags for the bundle.js and bundle.css files.
