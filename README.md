# Advanced CSS-SCSS

Udemy course: https://www.udemy.com/advanced-css-and-sass/

## Downloads 

- (Linea)[http://linea.io/] for fonts; grab `_basic/_ICONFONTS/fonts` and `_basic/_ICONFONTS/styles.css (which should be renamed to icon-font.css)`. Move both in css folder of project directory.

## Run

- Navigate to home directory where main.scss is and run `live-server`.

## Notes

Responsive Design
- Fluid layout
- media queries
- responsive images
- correct units
- desktop-first vs mobile-first

Maintainable and Scalable Code
- clean
- easy to understand
- growth
- reusable
- how to organize files, name classes, and structure HTML

Web Performance
- less HTTP requests
- Less code
- compress code
- use a css preprocessor
- less images
- compress images

OnLoad
- Load HTML --> Parse HTML --> DOM
- (from Parse HTML) Load CSS --> Parse CSS --> CSSOM
- (from DOM and CSSOM) Render tree --> website render

Cascade 
- Resolving combined CSS that is conflicted
- Sources: Author (coder), User, Browser
- Importance: User `!important`, Author `!important`, Author declaration, User declaration, Default browser
- Specificity (per css blocks that effect the same element in DOM): inline, ID, class, elements (0,0,0,0) Highest number wins left to right
- When using 3rd party stylesheets, include your import last to ensure your changes take effect

Standard font-size
- Use for scalability with mobile and standard (no need for media queries)
- Divide default html font-size (if px) by 10 to get rem
- So if we set `font-size: 10px;` in html tag then 10px = 1rem
- `font-size: 62.5%` in html tag then 62.5% = 10px (.625/16 = 10px)

<strong>B</strong>lock <strong>E</strong>lement <strong>M</strong>odified
- Block: Standalone component
- Element: part of block
- Modifier: different version of block or element (e.g. --round)

Sass
- Compiles css
- Variables, nesting, operators, partials and imports, mixins, functions, extends, control directives
- Sass different than SCSS (preserves original css syntax)
- Examples:
    - `$color-primary: #444`
    - When nesting, use & to get parent full path. E.g. A nested `&:first-child` inside an `li` === `li:first-child`. Using `:first-child` alone inside of an `li` === `li :first-child`
    - `darken($color,15%)`
    - mixin: specific content you would include in multiple locations, can pass in variables (`@mixin style-text($color)` ... `@include style-text($dark-color))
    - `@function divide($a,$b) { return $a / $b; }` ... `margin: divide(60,2) * 1px;`
    - @extend %placeholder
    - Extend takes selectors and combines them (same inner code), mixin adds code to selectors

Layouts
- Float, flexbox, css grid

Emmet extension VSCode
- creates html easily
- .className (then tab)
- htmlElementName.className (then tab)
- .className> ('>' continues as child of div)

Other
- inherit on property to force inherit
- :not sudo-class (`:not(:last-child)` = select everything except last child)
- Selectors: grab everything that starts with (^), contains (*), or ends with ($)
- '>' direct children
- '*' all children
- Perspective: Really cool, makes it pop off the page more or less
- coverr.co - free background videos for websites
