# HTML For Tip Calculator

We build out our html and css in this section.

## Resources
- [Code Branch](https://github.com/phptuts/udemy-svelte-tip-calculator/tree/video-5-html)
- [Emmet Cheat Cheat](https://docs.emmet.io/cheat-sheet/)
- [Milligram CSS](https://milligram.io/)


## Steps

1) Add the container section

```html
<main class="container">

</main>
```

2) The title to the page

```html
<main class="container">
  <section class="row">
        <div class="column">
            <h1>Tip Calculator</h1>
        </div>
    </section>
</main>
```

3) Add a style tag and center the h1 tag.

```html
<style>
  h1 {
    text-align: center;
  }
</style>
```

4) Add another for the price input

```html
  <section class="row">
    <div class="column">
      <label for="price">Price</label>
      <input type="number" id="price" />
    </div>
  </section>
```

5) Add the input for the tip 

```html
<section class="row">
    <div class="column">
      <label for="tip">Tip (15%)</label>
      <input type="range" min="0" max="100" id="tip" />
    </div>
  </section>
```

6) Make a style to make the range input take up 100% of width

```css
#tip {
    width: 100%;
}
```

7) Create a section with 3 buttons for preset tips.

```html
<section class="row">
    <div class="column"><button class="button button-outline">15%</button></div>
    <div class="column"><button class="button button-outline">25%</button></div>
    <div class="column"><button class="button button-outline">30%</button></div>
  </section>
```

8) Make the button take 100% of the width


```css
button {
    width: 100%;
}
```

9) Create the total tip at the button of the page

```html
<section class="row">
    <div class="column">
      <h2>Total Tip $12.12</h2>
    </div>
  </section>
```

10) Style the calculated Tip to be center and increase the top margin

```css
h2 {
    text-align: center;
    margin-top: 20px;
}
```

## Final Code

```html
<style>
    h1 {
        text-align: center;
    }
    h2 {
        text-align: center;
        margin-top: 20px;
    }
    #tip {
        width: 100%;
    }
    button {
        width: 100%;
    }
</style>
<main class="container">
    <section class="row">
        <div class="column">
            <h1>Tip Calculator</h1>
        </div>
    </section>
    <section class="row">
        <div class="column">
            <label for="price">Price</label>
            <input type="number" id="price">
        </div>
    </section>
    <section class="row">
        <div class="column">
            <label for="tip">Tip (15%)</label>
            <input type="range" min="0" max="100" step="1" id="tip">
        </div>
    </section>
    <section class="row">
        <div class="column">
            <button class="button button-outline">
                15%
            </button>
        </div>
        <div class="column">
            <button class="button button-outline">
                25%
            </button>
        </div>
        <div class="column">
            <button class="button button-outline">
                30%
            </button>
        </div>
    </section>
    <section class="row">
        <div class="column">
            <h2>Calculator Tip: $12.00</h2>
        </div>
    </section>
</main>

```

