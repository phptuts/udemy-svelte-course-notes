# Reactivity In Svelte

- How to make a variable in svelte to calculate the tip.

## Resources

- [Code](https://github.com/phptuts/udemy-svelte-tip-calculator/tree/video-7-reactive-variable)
- [Reactive Variables](https://svelte.dev/examples#reactive-declarations)

## Steps

1) Create a function that calculates the tip amount.

```javascript
function calcTip(tip, price) {
    const calcTip = (price * (tip / 100));
    return calcTip.toLocaleString('en-US',{
        currency: 'USD',
        style: 'currency'
    })
}
```

2) Create a reactive variable

```javascript
$: tipAmount = calcTip(tip, price);
```

3) Output the reactive variable in the template

```html
<h2>Calculated Tip: {tipAmount}</h2>
```
