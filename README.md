# About the project

p5EasyScreen is a simple serverless solution to screen p5.js sketches sequentially during determined time. For educational purposes, it can screen all the class sketches to show them. This solution uses the localStorage to share the sketches code between the tabs.

# Built with

- p5.js
- jquery
- Bootstrap
- Bootstrap-table

# Installation

There is no need to install because it is a serverless application.
In the example section you will find a link that you can use whatever you want.
Another option is to download the code and uses a little server to use the application in your network.
Opening the html files without server in local it won't worked because this application uses the localStorage of the browser to store the sketch codes.

# LICENSE

Distributed under the GPLv3. See LICENSE for more information.

# How this work:

1. Select the sketches you want to screen with the file input. You can select more than one sketch files. When the files are selected, you will see a table with information about the files.

2. Decide how many seconds or minutes to show every sketch.

3. Open the display window or tab with the "open display button".
This tab is the screen where the sketches will be screened. It you project the sketches to the class, use this screen to show them.

4. To start showing the sketches, press the button "start".
When start button is pressed, the first sketch is send to the display tab and it is shown. You will see that the table with the sketches decreases. The first sketches that is send is erased from the list.

Every time the timeout is reached, another sketch code is send and the display tab is reloaded.

# Sketches

The sketches has to be regular p5.js files. If you want to show the author of the sketch, add one variable called "author" at the beginning:
```JS
let author = "Your name";
```

For full screen of the sketch, windowWidth and windowHeight has to be used in setup() function when creatingCanvas.

```JS
function setup() {
  let myCanvas = createCanvas(windowWidth, windowHeight);
  ...
}
```

Also, if the window changes:

```JS
function windowResized() {
   resizeCanvas(windowWidth, windowHeight);
}
```

# Example

You can see this working [here](https://isaacmg.gitlab.io/sketchs/p5EasyScreen/index.html).
