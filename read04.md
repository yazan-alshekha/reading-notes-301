# Common Responsive Layouts with CSS Grid (and some without!)

CSS grid is now supported in Samsung internet v6.2 and many other modern browsers and has been the answer to many a prayer of web developers everywhere. In the same way that flexbox gave us a way to layout block elements next to each other, CSS grid lets us not only arrange elements in a row or a column, but in multiple rows and columns. Finally two dimensional layouts are becoming simpler!

When I was learning CSS and HTML the way that I learnt best was by copying layouts written by others and then changing bits, deleting bits and playing around with them until I understood what was going on. With that in mind, I’ve composed a few common responsive website layouts for you to copy, edit, mess around with. I’ll go over my thinking with each layout and will outline a few tricks from each one. (NB, you may have noticed that I’m not a designer, so I hope you like cats!). I’ve moved the CSS in each demo that is relevant to the layout up to the top of the CSS file in comment blocks so that you can see the important parts easily, don’t write your CSS like this.

This is a responsive template that you’ll see all over the web, a large intro image followed by smaller images, buttons or articles. Have a look at the code from the glitch link above.

The smaller images (in a grid!) are in the perfect layout to get you started with CSS grid. Grid gives us control over how wide or narrow each of the ‘grid cells’ get. This allows us to maintain a sensible aspect ratio to their height. In this example I’ve used:

```
grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));

```
There’s a lot going on here, so let’s break it down
The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.
In this case, for the first argument, I’ve used auto-fill which will create a grid with as many tracks as will fit into the container. The second argument, which defines the width of the tracks, I’ve set to minmax(250px, 1fr). The minmax function will create track widths that can be a minimum of 250px wide and a maximum of 1fr. An fr is a ‘fraction unit’, a unit of measurement to define a fraction of the available space of the container. The width of the elements in the row will increase from 250px until the point where another element could potentially fit beside the first. Try changing the width of your browser while looking at the example to see this in action.

Often when we put images in a responsive grid layout like this we come across the problem of the images stretching out of proportion. Using

```
object-fit: cover;

```
can help here, as that will stop the image from stretching, but it will cause cropping to happen. What we end up with is equally sized grid ‘cells’ which will fill increasing numbers of columns as the page width increases.

The final thing of note here is the grid-gap property. This defines the size of the space between the columns and the rows. This will affect the number of elements that will fit in a track, so you may need to adjust your minmax sizes accordingly. To create similar gaps between elements with flexbox we currently have to use a combination of margin and the justify-content properties, however column-gap and row-gap are in the works.

The rest of the position styling in this example has been done using flexbox, as these are one dimensional layouts. Flexbox is still my favourite tool for vertically centering elements on the page. Grid is brilliant for creating grids, but it doesn’t mean that our other layout tools are no longer necessary

