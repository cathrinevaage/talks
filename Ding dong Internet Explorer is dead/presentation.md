![](preroll.mp4)

---

# Ding dong Internet Explorer is dead

---

## CSS

---

### :is

```css
:is(.foo, .bar, .baz) :is(.qux, .aæx12) {
  color: green;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/:is](https://developer.mozilla.org/docs/Web/CSS/:is)]

---

### :is

```scss
/* scss source */
.foo, .bar, .baz {
  .qux, .aæx12 {
    color: green;
  }
}

/* output */
.foo .qux,
.foo .aæx12,
.bar .qux,
.bar .aæx12,
.baz .qux,
.baz .aæx12 {
  color: green;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/:is](https://developer.mozilla.org/docs/Web/CSS/:is)]

---

### ::marker

```css
:is(ul, ol) li::marker {
  color: purple;
  font-size: 1.25em;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/::marker](https://developer.mozilla.org/docs/Web/CSS/::marker)]

---

### ::placeholder

```css
input::placeholder {
  color: purple;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/::placeholder](https://developer.mozilla.org/docs/Web/CSS/::placeholder)]

---

### :focus-within

```css
div:focus-within {
  outline: 0.125rem blue;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/:focus-within](https://developer.mozilla.org/docs/Web/CSS/:focus-within)]

---

### :any-link

```scss
a {
  text-decoration: none;

  &:any-link {
    text-decoration: underline;
  }
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/:any-link](https://developer.mozilla.org/docs/Web/CSS/:any-link)]

---

### Interaction media queries

```css
@media (any-pointer: none) {}
@media (any-pointer: fine) {}
@media (any-pointer: coarse) {}

@media (pointer: none) {}
@media (pointer: fine) {}
@media (pointer: coarse) {}

@media (any-hover: none) {}
@media (any-hover: hover) {}

@media (hover: none) {}
@media (hover: hover) {}
```

[.footer: [https://developer.mozilla.org/en-US/docs/Web/CSS/@media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)]

---

### Resolution media queries

```css
@media (min-resolution: 192dpi) {}

@media (max-resolution: 192dpi) {}

@media (-webkit-device-pixel-ratio: 2) {}
```

[.footer: [https://developer.mozilla.org/en-US/docs/Web/CSS/@media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)]

---

### Feature queries

```scss
div {
  display: flex;
  flex-gap: 1rem;

  @supports not (flex-gap: 1rem) {
    &:not(:last-child) {
      margin-right: 1rem;
    }
  }
}
```

---

### `object-fit`

```css
img, video {
  object-fit: fill;
  object-fit: contain;
  object-fit: cover;
  object-fit: none;
  object-fit: scale-down;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/object-fit](https://developer.mozilla.org/docs/Web/CSS/object-fit)]

---

### `object-position`

```css
img, video {
  object-position: left top;
  object-position: right center;
  object-position: 100% 50%;
  object-position: 10rem 15rem;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/object-position](https://developer.mozilla.org/docs/Web/CSS/object-position)]

---

### Intrinsic & Extrinsic Sizing

```css
div {
  width: min-content;
  width: max-content;
  width: fit-content;
}
```

---

### `justify-content: space-evenly;`

```css
div {
  display: flex;
  justify-content: space-evenly;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/justify-content](https://developer.mozilla.org/docs/Web/CSS/justify-content)]

---

### `text-stroke` & `text-fill`

```css
h1 {
  -webkit-text-stroke: 1px green;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: green;

  -webkit-text-fill-color: blue;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/-webkit-text-stroke](https://developer.mozilla.org/docs/Web/CSS/-webkit-text-stroke) [https://developer.mozilla.org/docs/Web/CSS/-webkit-text-fill-color](https://developer.mozilla.org/docs/Web/CSS/-webkit-text-fill-color)]

---

### `will-change`

```css
div {
  will-change: scroll-position;
  will-change: contents;
  will-change: transform;
  will-change: opacity;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/will-change](https://developer.mozilla.org/docs/Web/CSS/will-change)]

---

### `#rrggbbaa`

```css
div {
  background-color: #00000088;
}
```

```html

<svg viewBox="0 0 60 60">
  <rect
    x="15"
    y="15"
    height="30"
    width="30"
    fill="#2f4a31cc"
  />
</svg>
```

---

### `scroll-snap`

```scss
.container {
  scroll-snap-type: y mandatory;
}

.item {
  height: 100vh;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/CSS_Scroll_Snap](https://developer.mozilla.org/docs/Web/CSS/CSS_Scroll_Snap)]

---

### Shapes

```css
img {
  float: left;
  shape-outside: circle(50%);
  shape-margin: 1rem;
}

img {
  float: right;
  shape-image-threshold: 0.4;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/CSS_Shapes/Overview_of_CSS_Shapes](https://developer.mozilla.org/docs/Web/CSS/CSS_Shapes/Overview_of_CSS_Shapes)]

---

### `resize`

```css
textarea {
  resize: vertical;
}

div {
  resize: horizontal;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/resize](https://developer.mozilla.org/docs/Web/CSS/resize)]

---

### `position: sticky`

```css
header {
  position: sticky;
  top: 0;
  height: 5rem;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/position#sticky](https://developer.mozilla.org/docs/Web/CSS/position#sticky)]

---

### `font-variant-numeric`

```css
p {
  font-variant-numeric: normal;
  font-variant-numeric: ordinal;
  font-variant-numeric: slashed-zero;
  font-variant-numeric: lining-nums;
  font-variant-numeric: oldstyle-nums;
  font-variant-numeric: proportional-nums;
  font-variant-numeric: tabular-nums;
  font-variant-numeric: diagonal-fractions;
  font-variant-numeric: stacked-fractions;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/font-variant-numeric](https://developer.mozilla.org/docs/Web/CSS/font-variant-numeric)]

---

### `line-clamp`

```css
p {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/-webkit-line-clamp](https://developer.mozilla.org/docs/Web/CSS/-webkit-line-clamp)]

---

### CSS Grid

```css
#app {
  display: grid;
  grid-template-areas:
    "header header"
    "aside main"
    "footer footer";
}

header { grid-area: header; }
aside { grid-area: aside; }
main { grid-area: main; }
footer { grid-area: footer; }
```

[.footer: [https://developer.mozilla.org/docs/Learn/CSS/CSS_layout/Grids](https://developer.mozilla.org/docs/Learn/CSS/CSS_layout/Grids)]

---

### CSS Custom Properties (variables)

```css
:root {
  --orange: #ee5e46;
  --ugly: #2f4a31;

  /* --primary: var(--orange); */
  --primary: var(--ugly);
}

.FloyenLogo {
  color: var(--primary);
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties](https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties)]

---

### CSS Custom Properties (variables)

```scss
.Grid {
  --columns: 1;

  display: grid;
  grid-template-columns: repeat(var(--columns), 1fr);
  justify-content: space-between;

  @media (min-width: $sm) {
    --columns: 2;
  }

  @media (min-width: $md) {
    --columns: 3;
  }

  @media (min-width: $lg) {
    --columns: 4;
  }
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties](https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties)]

---

### `prefers-color-scheme` media queries

```scss
:root {
  --light: #fff;
  --dark: #111;

  @media (prefers-color-scheme: light) {
    --color: var(--dark);
    --background: var(--light);
  }

  @media (prefers-color-scheme: dark) {
    --color: var(--light);
    --background: (--dark);
  }
}

html {
  color: var(--color);
  background: var(--background);
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme](https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme)]

---

### `prefers-reduced-motion` media queries

```scss
:root {
  --transitionDuration: 0.25s;

  @media (prefers-reduced-motion: reduce) {
    --transitionDuration: 0;
  }
}

button {
  --background: blue;

  background: var(--background);
  transition: background var(--transitionDuration) ease;

  &:is(:hover, :focus) {
    --background: green;
  }
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion](https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion)]

---

### `min()`, `max()` & `clamp()`

```css
div {
  --lowerBound: 25vw;
  --upperBound: 50vw;

  width: min(var(--lowerBound), 20rem);
  width: max(20rem, var(--upperBound));
  width: clamp(var(--lowerBound), 20rem, var(--upperBound));
}
```

---

### `mix-blend-mode`

```css
::after {
  content: '';

  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;

  background: rgba(48, 48, 48, 0.6);
  mix-blend-mode: multiply;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/mix-blend-mode](https://developer.mozilla.org/docs/Web/CSS/mix-blend-mode)]

---

### `background-blend-mode`

```css
div {
  background: url('image.png'), linear-gradient(var(--orange), var(--ugly));
  background-blend-mode: hard-light;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/background-blend-mode](https://developer.mozilla.org/docs/Web/CSS/background-blend-mode)]

---

### `clip-path`

```css
.triangle {
  clip-path: polygon(0 0, 36% 100%, 100% 0);
  background: rebeccapurple;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/clip-path](https://developer.mozilla.org/docs/Web/CSS/clip-path)]

---

### `filter`

```scss
img {
  --filter: none;

  filter: var(--filter);

  @media (hover: hover) {
    --filter: grayscale(1) contrast(0.5);

    &:is(:hover, :focus) {
      --filter: none;
    }
  }
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/filter](https://developer.mozilla.org/docs/Web/CSS/filter)]

---

### `unset`

```scss
div {
  color: deeppink;

  p {
    color: darkcyan;

    &:hover {
      color: unset; /* deeppink */
    }
  }
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/unset](https://developer.mozilla.org/docs/Web/CSS/unset)]

---

### `all`

```css
div {
  all: unset;
}
```

[.footer: [https://developer.mozilla.org/docs/Web/CSS/all](https://developer.mozilla.org/docs/Web/CSS/all)]

---

### `rebeccapurple`

```css
html {
  background: rebeccapurple;
}
```

---

## JS

---

### ES6

---

#### `let` & `const`

```js
const foo = 1;

foo = 2 // TypeError: Assignment to constant variable.

let bar = 3;

bar = 4;
```

---

#### Arrow functions

```js
const double = (number) => {
  return number * 2
}

double(2) // 4

const tripple = (number) => (number * 3)

tripple(3) // 9
```

---

#### Template literals

```js
const exclaim = (string) => (
  `${string}!!!`
)

exclaim('Hei') // 'Hei!!!'
```

---

#### Default parameters

```js
const getContent = (area, column = 'text') => {
  return page[area][column]
} 
```

---

#### Destructuring

```js
const picture = (url, { height, width, mode = 'rc' }) => {
  /* ... */
}

const url = "1600000000000/logo.png"
const options = {
  height: 250,
  width: 250,
}

const pictureMediaUrl = picture(url, options)
```

---

#### Rest & spread

```js
const addItemsToArray = (array, ...newItems) => ([
  ...array,
  ...newItems,
])
```

---

#### `Map` & `WeakMap`

```js
const object = {}

object[true] = 'Does not support boolean as key'
object[{ foo: 1 }] = 'Does not support objects as key'
object[{ bar: 1 }] = 'Does not support objects as key'

Object.keys(object) // ['true', '[object Object]']


const map = new Map()

map.set(true, 'Supports boolean as key')
map.set({ foo: 1 }, 'Supports objects as key')
map.set({ bar: 1 }, 'Supports objects as key')

map.keys() // [true, { foo: 1 }, { bar: 1 }]
```

---

#### `Set` & `WeakSet`

```js
const someObject = {}


const array = []

array.push(someObject)
array.push(someObject)

array // [someObject, someObject]


const set = new Set()

set.add(someObject)
set.add(someObject)

set.values() // [someObject]
```

---

#### `async` / `await`

```js
const getItems = async () => {
  const response = await fetch('http://ip.jsontest.com/')
  
  if (!response.ok) {
    throw new Error('Fetch failed')
  }
  
  return await response.json()
}
```

---

### `Proxy`

```js
const target = { foo: 4 }

const doubleProxy = new Proxy(target, {
  get: (target, key) => (
    target[key] * 2
  ),
  set: (target, key, value) => {
    target[key] = value / 2
  }
})

doubleProxy.foo // 8
doubleProxy.foo = 12
doubleProxy.foo // 12
target.foo // 6
```

---

### ES Modules

```html
<script type="module" src="./main.js"></script>
```

```js
// ./main.js
import Vue from 'https://unpkg.com/vue@2.6.12'

new Vue()
```

---

### `ResizeObserver`

```html
<div style="resize: vertical;">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit.
</div>
```

```js
const resizeObserver = new ResizeObserver(() => {
  console.log('It resized')
})

resizeObserver.observe(divElement)
```

---

### `IntersectionObserver`

```html
<div class="ScrollContainer">
  <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
  <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
  <img>
  <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
  <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
</div>
```
```js
const intersectionObserver = new IntersectionObserver(([imgEntry]) => {
  if (imgEntry.isIntersecting ) {
    console.log('img is slightly on-screen')
  } else {
    console.log('img is completely off-screen')
  }
})

intersectionObserver.observe(imgElement)
```

---

### Speech Synthesis

```js
const utterance = new SpeechSynthesisUtterance('soi soi soi soi soi soi soi soi')

speechSynthesis.speak(utterance)
```

---

## HTML

---

### `<meter>`

```html
<meter
  value="50"
  max="100"
  optimum="100"
  low="20"
  min="0"
>
  Battery percent: 50%
</meter>
```
```html
<meter
  value="900000000000"
  max=" 1000000000000"
  min="0"
  high="950000000000"
>
  Disk usage: 900 GB / 1 TB
</meter>
```

---

### `<wbr>`

```html
<h1>Hør de beste trenings<wbr>hitsene</h1>
```

---

### `<details>` & `<summary>`

```html
<details>
  <summary>Det beste Olav vet å gjøre på voss er</summary>
  
  Å gønne litt puddersnø
</details>
```

---

### `download` attribute

```html
<a
  href="https://d3mp0n0ceuo60i.cloudfront.net/1600000000/timetable_2021.pdf"
  download="Rutetabell 2021.pdf"
>
  Rutetabell 2021
</a>
```

---

### Color input

```html
<input type="color" value="#00ffff">
```

---

# [fit] [github.com/cathrinevaage/talks](https://github.com/cathrinevaage/talks)
