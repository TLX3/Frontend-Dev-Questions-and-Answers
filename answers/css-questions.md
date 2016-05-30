#### CSS Questions:

####  What is the difference between classes and ID's in CSS?
ID has a higher specificity value than class. Classes refer to multiple elements unlike ID.
####  What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
Resetting removes all styling from every element. Normalizing makes elements render consistently across browsers. I use normalize because it preserves useful defaults such as headings.
####  Describe Floats and how they work.
Float is a positioning property. Elements can be floated left or right or none or inherit. Floated elements remain a part of the normal flow of a page and allows elements to be stacked side by side. It has a collapsing effect on the parent container that can be fixed by clearing the float.
####  Describe z-index and how stacking context is formed.
A stacking context is an element that contains a set of layers. Positioning and assigning a z-index value to an element creates a stacking context.
####  Describe BFC(Block Formatting Context) and how it works.
Floats, absolutely positioned elements, block containers that are not block boxes, and block boxes with 'overflow' not visible establish new block formatting contexts for their contents.
####  What are the various clearing techniques and which is appropriate for what context?
Use the clear property or float the parent element or set overflow:visible on the parent element. Clearfix works for most contexts so it is recommended.
####  Explain CSS sprites, and how you would implement them on a page or site.
It is a collection of images combined into a larger image that help with performance. You have only a single HTTP request for one image.
####  What are your favourite image replacement techniques and which do you use when?
lazy loading
####  How would you approach fixing browser-specific styling issues?
Use responsive design and cross browser CSS
####  How do you serve your pages for feature-constrained browsers?
Progressive enhancement and graceful degradation
####  What are the different ways to visually hide content (and make it available only for screen readers)?
Absolute position the element containing the element and move it off the screen.
####  Have you ever used a grid system, and if so, what do you prefer?
Bootstrap
####  Have you used or implemented media queries or mobile specific layouts/CSS?
min-device-width and max-device-width
####  Are you familiar with styling SVG?
SVG is markup driven vector graphic rendering engine for the browser.
####  How do you optimize your webpages for print?
Use media queries
####  What are some of the "gotchas" for writing efficient CSS?
Avoid inline styles and CSS expressions, use modular classes, and avoid unnecessary spacing.
####  What are the advantages/disadvantages of using CSS preprocessors?
Preprocessors extend CSS with variables, operators, interpolations, functions, mixins, etc. Although you write small and lean SASS or LESS scss it can lead to a large CSS file.
####  How would you implement a web design comp that uses non-standard fonts?
Use a link tag for Google fonts or font-face.
####  Explain how a browser determines what elements match a CSS selector.
Browsers match selectors right to left by specificity.
####  Describe pseudo-elements and discuss what they are used for.
pseudo-elements are added to selectors but instead of describing a special state, they allow you to style certain parts of a document.
####  Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
The box model determines how much space an element will take on the screen. It includes height/width, padding, and borders.
####  What does ```* { box-sizing: border-box; }``` do? What are its advantages?
If you set a width, and add padding and border, the total width doesn't change. So, you can modify padding and border values without worrying about expanding your box.
####  List as many values for the display property that you can remember.
block, inline, inline-block, flex, none, table, table-cell, table-row
####  What's the difference between inline and inline-block?
With inline-block, you can set the height and width of the element.
####  What's the difference between a relative, fixed, absolute and statically positioned element?
Elements are by default positioned static. A relative positioned element will stay in the normal flow of the document but can be offset left/right/top/bottom without other elements being aware of it. A absolute positioned element are taken out of the normal flow and will move relative to its closest relative positioned parent element. Fixed positioned is similar to absolute but it moves elements relative to the viewport.
####  The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
Priority is determined by specificity and inheritance.
####  What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
Bootstrap.
####  Have you played around with the new CSS Flexbox or Grid specs?
Yes.
####  How is responsive design different from adaptive design?
Responsive sites respond to the size of the browser at any given time. Adaptive sites adapt to the width of the browser at specific points.
####  Have you ever worked with retina graphics? If so, when and what techniques did you use?
No.
####  Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?
translate() is better for transitions and animations because it doesn't cause the browser to repaint.
