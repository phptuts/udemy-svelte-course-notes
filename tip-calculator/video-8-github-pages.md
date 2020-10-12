# Github Pages

How to publish to github pages

## Resources

- [GH Pages](https://pages.github.com/)
- [Gh Pages NPM](https://www.npmjs.com/package/gh-pages)


## Steps

1) Import gh pages in your rollup config.

```javascript
import ghpages from 'gh-pages'
```

2) Go to the part that run only when production is on and upload to githpages

```javascript
production && terser() && ghPages.publish('public', (err) => {
      console.log(err, 'uploaded to gh pages');
    }),
```

3) Run npm run build

```bash
npm run build
```

4) Go to your github repository -> setting and find the url and make sure it's working.
