#  Project Setup

Let's get start.  Links to the code and notes in the resources.  In this series I am going to be usig visual studio code.  You can download it at https://code.visualstudio.com.  

You will also need to download the svelte extension for visual studio code.  Click on the extension button and type in svelte.  It should be the first on the comes up.  All you will need to do is install it.  Optionally you can install prettier for code formatting.  

You will also need to install nodejs as well.  Go to nodejs.org and download the latest version.


1. Open visual studio code to the project folder you are going to use for your tip calculator.

2. Open a terminal on visual studio code and type in 

```base
npx degit sveltejs/template .
npm install 
npm run dev
```

3. Go to your local website, localhost:3000 and make sure that svelte is running.

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

Open up the rollup.config.js file.  This is where svelte gets compiled.  Notice the bundle.js and bundle.css files are being compiled to the public/build folder.  These files will contain all the javascript and css for your components.

Open up source folder and you will see the main.js file.  This is the entry point in your application.  Notice that we are passing props into the App component.  Go ahead change the prop name to your name.  Notice that the webpage changes to Hello {YourName}.  Also look at the target.  In this app we are targeting the body element.  This means that the App.svelte file will control the body of the page.

Open the src/App.svelte file.  Notice that it is taking in prop name and showing that on the page.  This is why the page now says Hello {Yourname}.  All components will go into the src file.

Open up the public folder.  Here you will find the index.html, global css and the build folders we talked about previously.  global.css is just a css file no magic there.  Same for our index.html.  The notice that these files already have link and script tags for the bundle.js and bundle.css files.




