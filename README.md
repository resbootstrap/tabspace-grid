# Space Grid

A Responsive Grid System based on spaces.

## Getting Started

If you don't (want to) use Sass, you can grab the specific CSS file for your desired grid system in the `dist` folder.

**Initial Configuration**

```bash
// GRID SYSTEM CONFIG
// ------------------------------

// Options
$use-gutter:        true;                               // Use gutter for container?
$use-max-width:     true;                               // Use max width for container?
$use-prefix:        ".";                                // Prefix for use "%" (placeholder) or "." (class).

// Classes
$class-padding:     "sg-pd";                            // Class for paddings
$class-margin:      "sg-mg";                            // Class for margins
$class-centered:    "sg-mid";                           // Class for blocks
$class-column:      "sg-col";                           // Class for columns
$sides:             "left", "right", "top", "bottom";   // Which side do you want to use?

// Grid Values
$max-columns:       10;                                 // max value is 10
$max-margins:       10;                                 // max value is 10
$max-paddings:      10;                                 // max value is 10
$max-width:         980px;                              // value for max-width on container
$container-width:   100%;                               // value for container width
$container-gutter:  20px;                               // value for container gutter
```

## Usage

A quickly example on how to use the Grid System, with:

### Modular CSS

```html
<div class="container">
    <div class="row">
        <div class="#{column-class}#{columns} off-#{side}#{column-number} pad-#{side}#{column-number} mid#{column-number} #{force}">...</div>
        <div class="#{column-class}#{columns} off-#{side}#{column-number} pad-#{side}#{column-number} mid#{column-number} #{force}">...</div>
    </div>
    <div class="row">
        <div class="#{column-class}#{columns} off-#{side}#{column-number} pad-#{side}#{column-number} mid#{column-number} #{force}">
            <div class="#{column-class}#{columns} off-#{side}#{column-number} pad-#{side}#{column-number} mid#{column-number} #{force}">...</div>
            <div class="#{column-class}#{columns} off-#{side}#{column-number} pad-#{side}#{column-number} mid#{column-number} #{force}">...</div>
        </div>
        <div class="#{column-class}#{columns} off-#{side}#{column-number} pad-#{side}#{column-number} mid#{column-number} #{force}">...</div>
    </div>
</div>
```

#### Options:

- columns: 1 to 10
- off: margin 1-10
- pad: padding 1-10
- mid: margin (left|right) 1-10
- force: last, first, omega, alpha, centered

### Semantic CSS

```css
.main {
    @include col(7);
}
.sidebar {
    @include col(3);
}

@media screen and (max-width: 767px) {
    .main {
        @include col(10);
    }
    .sidebar {
        @include col(10);
    }
}
```


## License

[MIT License](http://vitorbritto.mit-license.org/) © Vitor Britto
