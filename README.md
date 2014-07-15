# Space Grid

A Responsive Grid System based on spaces.

>  Inspired on: https://github.com/mdo/table-grid

## Getting Started

If you don't (want to) use Sass, you can grab the specific CSS file for your desired grid system in the `dist` folder.

**Initial Configuration**

```bash
// Options
$use-gutter:        false;                              // Use gutter for container?
$use-max-width:     false;                              // Use max width for container?
$use-prefix:        ".";                                // Prefix for use "%" (placeholder) or "." (class).

// Classes
$class-padding:     "pad";                              // Class for paddings
$class-margin:      "off";                              // Class for margins
$class-centered:    "cen";                              // Class for vertical align
$class-middle:      "mid";                              // Class for horizontal align
$class-column:      "col";                              // Class for columns
$class-sides:       "left", "right", "top", "bottom";   // Do not change the names, but feel free to remove a side from the list

// Grid Values
$max-width:         980px;                              // value for max-width on container
$container-width:   100%;                               // value for container width
$container-gutter:  20px;                               // value for container gutter
```

## Usage

A quickly example on how to use the Grid System, with:

### Modular CSS

```html
<div class="container">
    <div class="row mid1">
        <div class="col col5">...</div>
        <div class="col col5">...</div>
    </div>
    <div class="row mid1">
        <div class="col col5">
            <div class="col col4">...</div>
            <div class="col col6">...</div>
        </div>
        <div class="col col5">...</div>
    </div>
</div>
```

#### Options:

- **columns:** 1 to 10
- **margins:** margin 1-10
- **paddings:** padding 1-10
- **centereds:** margin (left|right) 1-10
- **middles:** margin (top|bottom) 1-10
- **floats:** left, right
- **forces:** last (force to margin right), first (force to margin left)


### Semantic CSS

```css
.main {
    @include row;       /* -> width: 100%; display: table; table-layout: fixed; */
}
.content {
    @include col(7);    /* -> display: table-cell; width: 70%; */
    @include middle(1); /* -> margin: 10px auto 10px auto; */

}
.sidebar {
    @include col(3);    /* -> display: table-cell; width: 30%; */
    @include middle(1); /* -> margin: 10px auto 10px auto; */
}

@media screen and (max-width: 767px) {
    .content {
        @include col(10); /* -> display: table-cell; width: 100%; */
    }
    .sidebar {
        @include col(10); /* -> display: table-cell; width: 100%; */
    }
}
```


## License

[MIT License](http://vitorbritto.mit-license.org/) © Vitor Britto
