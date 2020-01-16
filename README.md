# grid-sass-function
This is a SASS (SCSS) function which implements kind of griding simply.

The function - which is called 'grid' - gets three paramters:
### [columns (default: 1)]
The number of columns that is goning to be displayed in the grid.
### [gapColumns (default: 0)]
The gap between columns which can be used with any valid unit.
### [gapRows (default: 0)]
The gap between rows which can be used with any valid unit.

Eventually the function sets three [CSS Variable](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) for you that might be used for responsiveness:
1. **--columns:**      The number of columns
2. **--gap-columns:**  The gap between columns
3. **--gap-rows:**     The gap between rows

*be sure that these variables are scoped to the block that the function be called*

## Example
HTML
```HTML
<ul class="card-list">
    <li class="card">card 1</li>
    <li class="card">card 2</li>
    <li class="card">card 3</li>
    <li class="card">card 4</li>
    <li class="card">card 5</li>
    <li class="card">card 6</li>
</ul>
```
SCSS
```SCSS
.card-list {
    @include grid(3, 10px, 20px);
    .card {
        // your card style
    }
}
```