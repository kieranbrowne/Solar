# Solar

###THE SASS
```scss
@import "solar";
$container: 800px;

// gen-grid takes number of columns and gutter size as a percentage of column
@include gen-grid($col:12,$gut:50);
```

###THE HTML
```html
<div class="grid-12-50">
    <div class="span-4">Elit ad ipsum voluptate?</div>
    <div class="span-4">Dolor odio maiores ad.</div>
    <div class="span-4">Sit nobis blanditiis a!</div>
    <div class="span-4">Ipsum adipisci voluptatum repellat.</div>
    <div class="span-4">Adipisicing molestiae blanditiis reprehenderit?</div>
    <div class="span-4">Sit aspernatur optio sit.</div>
</div>
```
