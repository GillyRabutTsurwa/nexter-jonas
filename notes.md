## Version 1 Notes

*     grid-template-rows: 80vh min-content 40vw repeat(3, min-content);
*     grid-template-columns: 8rem minmax(6rem, 1fr) repeat(8, minmax(min-content, 14rem)) minmax(6rem, 1fr);
*     grid-template-columns: [sidebar-start] 8rem [sidebar-end full-start] minmax(6rem, 1fr) [centre-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end]) [centre-end] minmax(6rem, 1fr) [full-end];
* Peux-tu traduire tout le code au-dessûs ?

## Version 2 & 3 Notes
* J'ai **beaucoup** appris
  * I finally understand **Sass Extends**
    * Extends **is the inverse of a mixin**. A mixin takes the code inside
    it and pastes it to the desired selectors whereas an extend **takes the selector and pastes it to the general extend selector** where the code is defined.
    * %heading { font-family: "somefont"; font-weight: 400; }
    then...
    .heading-1 { @extend %heading; }

    With this, .heading-1 gets pasted to %heading.
    * Combining **autofit** and the **minmax()** to set up your grid columns is very powerful. It makes widths and heights responsive **without writing a single line of media query** I'm really starting to like CSS Grids.
    * Usually, we define the grid columns and not the grid rows. We let the content define the rows. Meaning, we have implicit grid rows. 
    * For implicit grid sections, (in our case, mostly rows), we cannot use -1 to span until the end. This works for explicit grid sections only

## Version 4 Notes

* align-items, justify-items, align-self, justify-self, align-content, justify-content. Master these

## Version 5 Notes

* Grid Gallery
  * For something like a gallery, use your smallest unit (smallest image) and make your columns and rows using that item
* To stop image gallery GRID OVERFLOW
  * give the image a container
  * give the image INSIDE the container a property of object-fit: cover;
    * object fit property should always go to the child element
  * To summarize, make the image container the direct child of the grid container instead of the image itself
  * IMPORTANT: height and width declarations are needed for object-fit: cover to work

## Version 6 Notes
* Text and pseudoelements can be grid items