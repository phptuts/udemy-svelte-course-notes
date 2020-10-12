# Binding Variables and Class

- How to connect variables to inputs
- How to toggle classes based on conditions
- How to create click events with buttons

## Resources

- [Code](https://github.com/phptuts/udemy-svelte-tip-calculator/tree/video-6-binding-variables-class)
- [Outputing Variables](https://svelte.dev/examples#hello-world)
- [Two Way Binding](https://svelte.dev/examples#text-inputs)
- [Class Binding](https://svelte.dev/examples#classes)

## Steps

1) Create a script tag with 2 variables one for the price and the other for the tip amount.

```html
<script>
  let price = 12.51;
  let tip = 15;
</script>
```

2) Bind the variables to the right inputs

```html
<input bind:value={tip} type="range" min="0" max="100" step="1" id="tip">
```

```html
<input bind:value={price} type="number" id="price">
```

3) Output the tip in the label

```
<label for="tip">Tip ({tip}%)</label>
``

4) Create a function changes the tip variable to a new value.

```javascript
function changeTip(newTip) {
  tip = newTip;
}
```

6) Hook up the function to the on click event in the button tags

```html
<div class="column">
    <button on:click={() => changeTip(15)} class="button button-outline">
        15%
    </button>
</div>
<div class="column">
    <button on:click={() => changeTip(25)}  class="button button-outline">
        25%
    </button>
</div>
<div class="column">
    <button on:click={() => changeTip(30)}  class="button button-outline">
        30%
    </button>
</div>
```

7) Bind the class button-outline to show up only if the tip amount does not equal what the button text equals.

```html
<div class="column">
    <button on:click={() => changeTip(15)} class:button-outline={tip !== 15}   class="button">
        15%
    </button>
</div>
<div class="column">
    <button on:click={() => changeTip(25)} class:button-outline={tip !== 25}  class="button">
        25%
    </button>
</div>
<div class="column">
    <button on:click={() => changeTip(30)} class:button-outline={tip !== 30}  class="button">
        30%
    </button>
</div>
```
