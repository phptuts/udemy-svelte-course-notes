# Svelte Cleanup / Install Package

1) Install packages

```bash
npm install milligram gh-pages rollup-plugin-css-only --save-dev
```

2) Import the rollup plugin into our rollup config file.

```javascript
import css from 'rollup-plugin-css-only';
```

3) Add the rollup plugin to the list of plugins 

```javascript
css({ output: 'public/extra.css'})
```

4) Import milligram css into our main.js file.

```javascript
import 'milligram/dist/millgram.min.css'
```

5) Remove the prop being inserted into our app component.

```javascript
const app = new App({
	target: document.body,
});
```

6) Delete everything inside our App.svelte file.

7) Delete everything inside our global css file

8) Install the Roboto font

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
body {
  font-family: 'Roboto', sans-serif;
}
```

9) Change the title to Tip Calculator in the index.html file.

```
<title>Tip Calculator</title>
```

10) Make all the links relative for github pages.

11) Insert a link css tag for our extra css file which will contian our milligram.css

```html
	<link rel='stylesheet' href='extra.css'>
```

12) Test Everything out by running npm run dev

13) Inspect element and make sure there are no 404s.

