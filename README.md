# Space Grid

A Responsive Grid System based on spaces.

## Getting Started

> If you don't (want to) use Sass, you can grab the specific CSS file for your desired grid system in the `dist` folder.

## How to use

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
