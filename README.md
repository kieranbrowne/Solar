# Solar

## The Grid

## The Baseline Grid
```scss
@import "solar";

// define the grid as a sass map
$grid: (
  columns: 12,
  gutter: 2.5rem,
  container: 100vw,
  namespace: ""
);

// generate a set of classes from the information in the grid variable
@include gen-grid($grid);

// keeping this information in a map makes our code more reusable.
// for example we can use our grid to drive other parts of our code.
// below we set the width and height of a box to the width of 4 columns
// and the left and bottom margins to 1 gutter's width.
// this will create perfectly spaced square tiles which match our grid whether or not they are used inside a .grid element.
.movie-tile {
  width: col-width($grid,4);
  height: col-width($grid,4);
  margin: 0 0 map-get($grid,gutter) map-get($grid,gutter);
}

p {
  @include baseline(1.2rem,1.5rem);
}
h2 {
  @include baseline(3rem,4.5rem);
}
h1 {
  @include baseline(2rem,4.5rem);
}
```

### THE HTML
```html
<div class="grid">
  <div class="col-4">Elit ad ipsum voluptate?</div>
  <div class="col-4">Dolor odio maiores ad.</div>
  <div class="col-4">Sit nobis blanditiis a!</div>
  <div class="col-4">Ipsum adipisci voluptatum repellat.</div>
  <div class="col-4">Adipisicing molestiae blanditiis reprehenderit?</div>
  <div class="col-4">Sit aspernatur optio sit.</div>
</div>
```
