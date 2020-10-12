# Reactivity In Svelte

- How to make a variable in svelte to calculate the tip.

## Resources

- [Code](https://github.com/phptuts/udemy-svelte-tip-calculator/tree/video-7-reactive-variable)
- [Reactive Variables](https://svelte.dev/examples#reactive-declarations)
- [toStringLocale](https://www.w3schools.com/jsref/jsref_tolocalestring_number.asp)

## Steps

1) Create a function that calculates the tip amount.

```javascript
function calculatedTip(price, tip) {
    const calcTip = (price * (tip / 100));
    return calcTip.toLocaleString('en-US', {
        style: 'currency',
        currency: 'USD'
    });
}
```

2) Create a reactive variable

```javascript
$: tipAmount = calculatedTip(price, tip);
```

3) Output the reactive variable in the template

```svelte
<h2>Calculated Tip: {tipAmount}</h2>
```
