# Processing Portfolio
Hey! My name is Mason Slover and I am a mathematics and computer science student at Fordham University Lincoln Center. I have been creating art using Processing, a visual Java environment, for 5 years. This GitHub is a repository of some of my favorite works, some of which are open source. Here are a few of my favorite pieces:

[toc]

## Facial Obfuscation Mirrors

Inspired by the peaceful protests in Hong Kong and the United States and the growing fear of government athorities using facial recognition to identify and prosecute protestors, I created several facial obfusication algorithms that prevent recognition of the observer.

### [Image Rasterization and "Ghosting"](./Ghosting)

This program hooks into a user's webcam and augments its input. Using the global `resolution` variable, the video feed is evaluated at several intervals where the brightness of selected pixels are mapped to the size of an ellipse at the same point. The color is also taken from this point. By progressively destroying older frame's content, the viewer is only recognizable when they are still.

<center>

<img src="./Ghosting/raster.gif" style="text-align:center;"/>

### [Facial Tracking and Dithering](./Dithering)

This project selects random pixels from the input of the and creates a rectangle using the color of the pixel selected. Using [OpenCV for Processing,](https://github.com/atduskgreg/opencv-processing) all faces within view of the webcam are detected, and the size of the rectangle drawn within the frame of the face are increased to obfuscate the viewer and prevent identification. Upon clicking on the window with the mouse, the sizes of the rectangles are reversed, revealing the viewer and obstructing the background.

<img src="./Dithering/dotted.gif" style="zoom:75%;" />

## [Dynamic Variable Width Fonts](./VariableWidthFonts)

Using processing, I was able to import a variable width font and dynamically adjust the type's weight and height. Using sinusoidal speed changes and random character attributes, this project creates dynamic type that allows for extreme flexibility.

<img src="./VariableWidthFonts/VariableWidthFont.gif" style="zoom:25%;" />

## [Flocking Algorithm](./FlockingAlgorithm)

Using a [Craig Reynold's Boids algorithm writeup](http://www.red3d.com/cwr/boids/), I implemented three main flocking behaviors to simulate natural behavior in Processing:

### Separation: 

Any "Boid" within 20 pixels with another Boid will steer away from the center of the other Boid to avoid colliding.

### Cohesion: 

Each Boid calculates the average position of all other Boids within 20px, and steers towards that point. This allows for "flocks" of Boids.

### Alignment: 

Each Boid will steer towards the average heading of all other Boids within 20px. This allows for flocks to fly in the same direction.



When the mouse is pressed, the location of the pointer acts as a point of avoidance for all Boids within the shown radius. If a Boid enters this radius, it will be steered away from the mouse. The mouse may also act as a point of attraction, steering all Boids to its center.



<img src="./FlockingAlgorithm/boids.gif" style="zoom:50%;" />



