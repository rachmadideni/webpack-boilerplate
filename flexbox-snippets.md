## flexbox snippets

### CSS that can be applied to the container

<ul>
<li>display: flexbox | inline-flex;</li>
<li>flex-direction: row | row-reverse | column | column-reverse;</li>
<li>flex-wrap: nowrap | wrap | wrap-reverse;</li>
<li>flex-flow: <‘flex-direction’> || <‘flex-wrap’></li>
<li>justify-content: flex-start | flex-end | center | space-between | space-around;</li>
<li>align-items: flex-start | flex-end | center | baseline | stretch;</li>
<li>align-content: flex-start | flex-end | center | space-between | space-around | stretch;</li>
</ul>

### CSS that can be applied to items/elements in the container
<ul>
<li>order: integer;</li>
<li>flex-grow: number; /* default 0 */</li>
<li>flex-shrink: number; /* default 1 */</li>
<li>flex-basis: length | auto; /* default auto */</li>
<li>flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]</li>
<li>align-self: auto | flex-start | flex-end | center | baseline | stretch;</li>
</ul>

### CSS Display Flex
display: flex is tells your browser, "I wanna use flexbox with this container, please."

A div element defaults to display:block. An element with this display setting takes up the full width of the line it is on.


### Flex Direction
flex-direction allows you to control how the items in the container display. Do you want them left to right, right to left, top to bottom, or bottom to top? You can do all of these easily by setting the flex-direction of the container.

The default arrangement after applying display: flex is for the items to be arranged along the main axis from left to right. 
You can also set flex-direction to row-reverse and column-reverse.

### Justify Content
justify-content is a property to align items in the container along the main axis (see terminology diagram above). This changes depending on how content is displayed. It allows us to fill any empty space on rows and define how we want to ‘justify’ it.

Here are our the most common options used to justify content: flex-start | flex-end | center | space-between | space-around.

space-between distributes items so that the first item is flush with the start and the last is flush with the end. space-around is similar but items have a half-size space on either end.

### Flex Align Items
align-items allows us to align items along the cross axis (see terminology diagram above). This allows content to be positioned in many different ways using justify content and align items together.

Here are the most common options used to align items: flex-start | flex-end | center | baseline | stretch

For stretch to work how you would expect, the height of the elements must be set to auto instead of a specific height.

### Align Self
align-self allows you to adjust the alignment of a single element.

It has all the same properties of align-items.

In the following animation, the parent div has the CSS align-items: center and flex-direction: row. The first two squares cycle through different align-self values.

### Flex Wrap
Flexbox by default will try to fit all elements into one row. However, you can change this with the flex-wrap property. There are three values you can use to determine when elements go to another row.

The default value is flex-wrap: nowrap. This will cause everything to stay in one row from left to right.

flex-wrap: wrap  will allow items to pop to the next row if there is not enough room on the first row. The items will be displayed from left to right.

flex-wrap: wrap-reverse also allows items to pop to the next row but this time the items are displayed from right to left.

### Flex Flow
flex-flow combines the use of flex-wrap and flex-direction into one property. It is used by first setting the direction and then the wrap. Here is an example: flex-flow: column wrap;

### Align Content
align-content is used for aligning items with multiple lines. It is for aligning on the cross axis and will have no effect on content that is one line.

Here are the options: align-content: flex-start | flex-end | center | space-between | space-around | stretch;