# Scalable SASS Template

Base styling structure for projects small or large. This is designed with scalability in mind, separating styling of base, layouts, modules and states.

## Folder Structure

```
├── 01-base
│   ├── _base.sass
│   ├── _fonts.sass
│   ├── _functions.sass
│   ├── _mixins.sass
│   ├── _normalize.scss
│   └── _vars.sass
├── 02-layout
│   ├── _footer.sass
│   ├── _grid.sass
│   └── _header.sass
├── 03-module
│   ├── _buttons.sass
│   ├── _forms.sass
│   ├── _navs.sass
│   └── _social-icons.sass
├── 04-state
│   └── _state.sass
├── 05-hacks
│   └── _shame.sass
└── main.sass
```

## Sections
Parts are separated into folders that are imported into main.sass, this is compiled into a single css file. main.sass should only contain the links to other files no css.

### Base
This is where vendor code, helpers, mixins, variables, and general selector styles are kept.

### Layout
Layouts holds main styling for each section (header, grid, footer, etc.). I also put my grid setup here.

### Module
Here we put any reusable modules (nav, forms, cards, etc.). This enables us to reuse elements easily.

### State
Holds any state specific code (is-hidden, is-collapsed, etc.).

### Hacks
Any hacky css to be later improved, things like !important or overflow: hidden.

## Naming
I use a BEM style class naming convention like this:
- block `.icon` 
- element `.icon--icon`
- modifier `icon_wide`

This is how the sass looks:
```sass
.icons
  width: 140px
  display: flex
  justify-content: space-between

  &--icon
    width: 20px
    height: 20px
    fill: $primary-color

  &_wide
    width: 100%
```


## More Info
- Scalable and Modular Architecture for CSS by Jonathan Snook
[ SMACSS]('https://smacss.com/')
- Block Element Modifier methodology [BEM]('http://getbem.com/)