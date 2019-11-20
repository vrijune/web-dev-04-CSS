Web Lab 04 &ndash; CSS II
==========

Begin by forking this repository into your namespace by clicking the ```fork``` button above, then selecting your username from the resulting window. Once completed, click the ```clone``` button, copy the ```Clone with HTTPS``` value. Open IntelliJ, and from the welcome screen click ```Check out from Version Control -> Git```, then paste the copied URL into the ```URL``` field of the resulting window. Provide your GitLab username and password if prompted.

Explore the files in the project, familiarizing yourself with the content.

When complete, demonstrate your code to your tutor. This must be verified with your tutor by the end of the week.

Exercise One
----------
In this exercise, you’re going to decorate an image of a Christmas tree with baubles, and place it all over a nice New Zealand landscape photograph. You will find the images used in this exercise in the ```ictgradschool/web/lab04/assets``` folder. Any HTML for this question should be placed in ```christmas_tree.html```, and any associated CSS should be written in ```style.css```. An example of what your page may look like when complete is shown below.

![](./spec/ex01-screenshot.png)

Begin by creating 8 ```<img>``` elements in the document, displaying each of the 8 images in the assets directory. Give each image a meaningful id, and additionally give each of the colored ball images a common class. Style the 'background' image so that it sits in the middle of the web browser viewport. Using CSS, move the 'pohutukawa' image so that it sits on top of the background image, in such a way that makes it look like it is a part of the background.

Style the colored baubles so that they appear to be decoratively scattered over the tree. Update at least one of the baubles so that it appears *behind* the pohutukawa tree.


##### HINTS:
- You may find it useful to use a container div with relative or absolute positioning, so that any elements within it can position themselves absolutely with respect to its box.
- Use absolute positioning on the background to cover the entire div starting at the top left. The image shouldn't have to resize if you make the container div the same size as the background image.
- To make items appear on top of one-another, you will want to look into the ```z-index``` of the elements.


Exercise Two
----------

Make a copy of the files in the ```ictgradschool/web/lab04/ex1``` folder and place them in the ```ictgradschool/web/lab04/ex2``` folder. You may need to create this folder yourself. Close all open editor tabs, then when opening files to edit, open them from the ex2 folder.

Open the ```christmas_tree.html``` file from the ex2 directory of the project. Add the necessary CSS to get any bauble hanging on the Christmas tree to become bigger when the user hovers over it.

##### HINT:
- Remember the ```:hover``` CSS pseudoclass.

##### NOTE:
Because one of the baubles has been styled so that it was behind the tree, you may notice that such a bauble doesn't respond to hover events. This is because the tree image, being in front of it, captures the hover event first. To change this default behaviour it is possible in CSS to set elements to ignore events from the mouse, stylus or touch &ndash; generically classified as *pointer events*. To get your tree image to ignore pointer events so that these events are passed on to elements behind the tree instead, add something like this:

```
#tree {
	pointer-events: none; /* to restore it, set value to: auto */
}
```

Try using this to get hover events to work on any obscured baubles you have. For more information refer to <https://css-tricks.com/almanac/properties/p/pointer-events/>.


Exercise Three
----------

Open the ```ictgradschool/web/lab04/ex3/sonnets.html``` file. Inside the body of this file, you should find some unformatted text, which makes up the Sonnets, by William Shakespeare.  In this exercise, you will develop this page so that it appears like the page shown in ```exercise-03-fullpage.png```.

Begin, by surrounding all five of the sonnets in an opening ```<pre>``` tag and corresponding closing pre tag, and the title and author line in ```<strong>``` tags. Add a style block to the head of the document and add a selector for the pre tag. Update this CSS rule so that the pre tag:
- Has a font color of purple
- Has a 1.5 line spacing
- Has a font size of 22pt
- Uses the 'Alex Brush' font - See the CSS I lab for details on obtaining and using this font.

Update your style so that it contains a selector that matches the title and author section of the document. Update this rule so that the title:
- Uses the 'Alex Brush' font
- Has a font size of 22pt
- Is bold

Modify the document so that the background colour appears as 'Lavender'. This change makes it difficult to read the text. To alleviate this, create a container ```<div>``` that encompasses the document content, and style this so that:
- It has a white background
- It occupies 60% of the screen width, and is centered
- It has rounded corners, with the top-left and bottom-right corners being more rounded than the others
- It has a drop-shadow

Update your container div so that the container cannot be smaller than the text inside it. This is important, as preformatted text does not flow, and would not look good if it overlapped the background.

Using the image assets found in the ```ictgradschool/web/lab04/ex3/assets``` directory, update the page so that there is a corner decoration in the top-left and bottom-right corners of the page, and a repeating image running vertically alongside the text.

Complete your work by tweaking paddings and margins of elements as necessary to bring the appearance as close to the reference image as possible.

##### HINTS:
- The ```background``` property of an element can be used to allow one or more images to be set as the background.
- To position the bottom-right corner image properly, investigate the ```calc``` CSS function.