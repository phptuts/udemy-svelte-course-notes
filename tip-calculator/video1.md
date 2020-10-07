#  Project Setup

Let's get started.  Links to the code and notes in the resources.  In this series I am going to be using visual studio code as my code editor.  You can download it at https://code.visualstudio.com.  

You will also need to download and install the svelte extension for visual studio code.  Click on the extension button and type in svelte.  It should be the first one that comes up.   

You will also need to install nodejs.  Go to nodejs.org and download & install the latest version.


Open visual studio code to the project folder you are going to use for your tip calculator.

Open a terminal on visual studio code and type in 

```bash
npx degit sveltejs/template .
```

This will clone the [sveltejs/template](https://github.com/sveltejs/template) repository to your project folder.

Type in npm install to install the dependencies
```bash
npm install 
```

Then type in npm run dev to start the website

```bash
npm run dev
```

Go to your local website, localhost:3000 and make sure that svelte is running.

## Svelte Overview

Open the package.json file.  Notice that svelte is a dev dependency.  This means that the whole svelte library does not ship with your app.  Only the parts of svelte library you need ship with your app.

Also note that the three commands in your package.json, dev, build, and start.

Start will serve the index.html file in the public folder

Dev will serve the index.html file in the public folder and will recompile your application when it changes

Build is for building your app for production.

```json
"scripts": {
    "build": "rollup -c",
    "dev": "rollup -c -w",
    "start": "sirv public"
  },
```

Open up the rollup.config.js file.  This is where svelte gets compiled.  The bundle.js and bundle.css files are being compiled to the public/build folder.  These files will contain all the javascript and css for your components.

Open up source folder and you will see the main.js file.  This is the entry point in your application.  The App component is being passed a prop named "name".  Go ahead change the prop store your name as it's value.  This will changes page to Hello {YourName}.  Look at the target being passed into the App component.  In the App Component we are targeting the body element.  This means that the App.svelte component will control the body of the page.

Open the App.svelte file.  It's taking in prop name and showing that on the page.  This is why the page now says Hello {Yourname}.  Note all components will go into the src folder.

Open up the public folder.  Here you will find the index.html, global.css files and the build folder we talked about previously. The global.css is just a css file no magic there.  Same for our index.html.  These files already have link and script tags for the bundle.js and bundle.css files.





