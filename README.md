# flexbox
Following along a Wes Bos tutorial and creating a few simple pages to learn flexbox.

## Resources
* Wes Bos tutorial, What the Flexbox - https://flexbox.io/
* MDN documentation - https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox
* https://css-tricks.com/snippets/css/a-guide-to-flexbox/

## Notes

### General Concepts / Terminology
* flex container - surrounding element, needs to have display: flex
* flex items - elements within a flex container element (do not need special class or css rule, automatically a flex item)

### Container Properties
* display
  - flex (whole width)
  - inline-flex (like span, used width of combined elements)
* flex-direction - sets axis
  - row (default) - side by side; main axis: left to right, cross axis: top to bottom
  - column - vertical; main axis: top to bottom
  - row-reverse - main axis: right to left
  - column-reverse - main axis: bottom to top
* flex-wrap
  - no-wrap (default)
  - wrap - will wrap items based on defined / set width, the sets height based on number of items to fit in container

### Item Properties
* 
