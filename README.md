# Flexbox
Following along a Wes Bos tutorial and creating a few simple pages to learn flexbox.

## Resources
* css-tricks (quick guide) - https://css-tricks.com/snippets/css/a-guide-to-flexbox/
* MDN documentation - https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox
* Wes Bos tutorial, What the Flexbox - https://flexbox.io/

## Notes

### Concepts / Terminology
* flex container - surrounding element, needs to have display: flex
* flex item - elements within a flex container element (does not need special css property, automatically a flex item)
* main axis - direction which items are laid out
* cross axis - direction perpendicular to main axis

#### Usage / Setup Steps
* important to know / understand / set the size and position of your container
* important to know / set the axis direction of your container 
* NOTE: be aware, that flex will / may override items' height and width properties based on flex settings
  - height and width are often automatically set / adjusted to align items per the flex settings
* NOTE: once your flexbox code is written, to make it compatible, it should be run through Autoprefixer
  - e.g.  https://autoprefixer.github.io/
  - you can use Gulp, Grunt, or some other build process

---------

### Container Properties
#### General
* __display__
  - flex (whole width)
  - inline-flex (like span, used width of combined elements)
* __flex-direction__ - sets axis direction
  - row (default) - items laid out side by side (ltr); main axis is horizontal, cross axis is vertical
  - column - items laid out atop of each other (ttb); main axis is vertical, cross axis is horizontal
    + NOTE: when setting flex-direction to column, __it is helpful to set a height (such as height or min-height 100vh) to see effects__
  - row-reverse - like row, but right to left
  - column-reverse - like column, bottom to top
* __flex-wrap__
  - no-wrap (default)
  - wrap - will wrap items based on their defined widths
    + sets items' heights based on number of items to fit in container (fill container's height)
    + also, enforces the true width of the items (doesn't override an item's width)

#### Justify
* __justify-content__ - __*justifies*__ items along __*main axis*__ (when there is space)
  - flex-start - default; analagous to left justified
  - others: flex-end (analagous to right justified), center, space-between, space-around, ...
* __align-content__ - __*justifies*__ items along __*cross axis*__ (when there is space)
  - stretch - default; strecthes items along cross axis
  - others: flex-start, flex-end, center, space-between, space-around

#### Align
* __align-items__
  - this property __*aligns*__ items within the container, along the __*cross axis*__
    + analagous to align top, align bottom, center
    + NOTE: __it is easier to notice the effects of align-items when the container height is set (or width)__
  - stretch - default, places items at top of container and stretches their height to the bottom of the container
  - others: flex-start, flex-end, center, baseline (aligns according to the bottom of text of each item)

### Item Properties
* __flex__ - the proportion to scale an item, up or down, when you have __extra space__ or __not enough space__
  - shorthand property for flex-grow, flex-shrink, flex-basis
    + "flex: 1;" is the same as setting "flex-grow: 1; flex-shrink: 1;"
  - NOTE: flex will override item width and height properties
* __flex-grow__ the proportion (a number) to scale an item up when there is __extra space__
    + if all set to 1, they are all equal; if one item is set to 2 that item is twice the width as all the others
* __flex-shrink__ - the proportion that item will shrink, compared to items when not enough space
* __flex-basis__ - default size of an element, before remaining space is distributed (auto or a length)
* __order__ - sets order of an element within container, regardless of element's dom order
  - kinda works like a z-index
  - default is 0 (if set to zero does not move it)
* __align-self__ - allows an item to override the align-items property of the container
