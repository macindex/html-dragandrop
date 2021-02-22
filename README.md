### Using the HTML5 Drag and Drop API

## Creating draggable content

The HTML5 Drag and Drop (DnD) API means that we can make almost any element on our page draggable. In this post we'll explain the basics of Drag and Drop.
Creating draggable content #

It's worth noting that in most browsers, text selections, images, and links are draggable by default. For example, if you drag the Google logo on Google Search you will see the ghost image. The image can then be dropped in the address bar, an <input type="file" /> element, or even the desktop. To make other types of content draggable you need to use the HTML5 DnD APIs.

To make an object draggable set draggable=true on that element. Just about anything can be drag-enabled, images, files, links, files, or any markup on your page.

In our example we're creating an interface to rearrange some columns, which have been laid out with CSS Grid. The basic markup for my columns looks like this, with each column having the draggable attribute set to true.

<div class="container">
  <div draggable="true" class="box">A</div>
  <div draggable="true" class="box">B</div>
  <div draggable="true" class="box">C</div>
</div>

Here's the CSS for my container and box elements. Note that the only CSS related to DnD functionality is the cursor: move property. The rest of the code just controls the layout and styling of the container and box elements.

.container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 10px;
}

.box {
  border: 3px solid #666;
  background-color: #ddd;
  border-radius: .5em;
  padding: 10px;
  cursor: move;
}

At this point you will find that you can drag the items, however nothing else will happen. To add the DnD functionality we need to use the JavaScript API.
Listening for dragging events #

There are a number of different events to attach to for monitoring the entire drag and drop process.

continues at: [Links with title](https://web.dev/drag-and-drop/)