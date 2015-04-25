
##Algorithm

The first part was ment to be an introduction to the digital power. For that we made an exercise that was repeated over three weeks. We had to think about a simple task involving drawing on a paper. It had to consist in simple steps that everyone could follow. This commands had to be given out, in the best cases in person, to friends and family. The results had to be collected and compared. We repeated the process each week, presented the results, and based on them, refined our steps.

My first task consisted of:

```
On a Paper: 
   
   1. draw two vertical lines parallel to eachother
   2. between the two, draw three circles
   3. in the middle circle, draw an rectangle
```
  
  The results I became back were diverse, some had done the task in a few seconds and others took more than a minute to complete it:
  
![1](http://i.imgur.com/QKQHPBJ.png?1)

For the next week I decided to complicate things more, adding complexer steps:

```
On a Paper: 
   
   1. draw a big circle, help yourself with a compass
   2. inside the circle, draw more geometrical forms. They have to cross 
      eachother. Not too many, you should still be able to recognise each one. 
   3. With this crossover, other forms have been created. Now you have to
      fillout the ones that haven't been crated by any  (the big
      circle)or by 2,4,6... overlappings.
```

Here the results. They were made more or less in the same time:

![2](http://i.imgur.com/vxsHUAt.jpg?1)


Except one, everybody understood what needed to be done.

For the next week, we had to try to convert the analog commands into digital code. For that, we used Processing, a Java based programming plattform, which allows the user to instantly see the result of what he has written. 

I structured my code the same way I did with the analog steps, instead of three, here I did it in two parts, merging step 1 and 2 of the analog indications.
So, basically, in the `setup()`, the program draws the different geometrical forms and in the `draw()` he fills them out in balck or white depending if they have been created by 0,2,4,6... overlappings or not.

in the `setup()`, the program generates a black background and on top  all the geometrical forms in random position  and rotation filled out in white with a 19% transparency:

![3](http://i.imgur.com/j6DAQ6x.png?1)

in the `draw()` the program uses this image to generate the result. How? As you can observe, each time a form overlaps, the color changes to a lighter tone. The exact color codes are:

| No. of overlappings | Color code  | filled out in |
|:------------- |:---------------:| :---------------: |
|none(black)| -16777216 | white |
| 1     |  -13487566 | black
| 2 | -10855846 | white |
| 3  | -8750470  | black
|4 |-7039852| white |
| 5| -5658199 | black
| 6| -4539718 | white |
| 7 | -3618616 | black

Now, the program does look at each individual pixel of the image generated and tell witch color it is, then, he fills out he pixel in black or withe color based on  the color. From the image above, he can generate this:

![4](http://i.imgur.com/3vStZqw.png?1)

Here a comparison between both:

![5](http://i.imgur.com/SlTovX3.png?1)
 
 
  [Here][link1] you can find the code.

 The first program I wrote was inneficient (on the rendering time), so I made some other versions, all based on this  principal. 
 
 In the forth week we had to find a practical implementation of this code in the analog world. I began thinking about a way to make my drawing more interesting, and came across the idea of making an animation of it, the different geometrical forms moving and rotating in the circle. 
 
This made it more interesting but was still digital. I thought, as I have some experience in Timelapse photography, to merge this animation with the photographic technique. I finished finding a theorical way of mixing both together. The idea is simple, to draw each frame using a selfmade printer, take a photo of each frame and put it togeter into a video. The selfmade printer would be placed somewhere in a City, or in a landscape, so that you would see movment in the final video (people, cars, clouds passing by...).
 
 
 This is how the selfmade printer would look like:
 
 ![6](http://i.imgur.com/yvS02aE.png)
 
It would consist of four motorized sliders, one short and three longer ones. that would be positioned on top of a whiteboard. 

The pen would be able to move in a three dimensional space. Two dimensions for positioning it on the right point, and the third to mark with it on the whiteboard.
  
 ![7](http://i.imgur.com/wPF2uru.png)
 
 Everything would be driven by an Arduino, which would control the four motors and trigger the camera. When the drawing is printed, The Camera is triggered and takes a photo. Then, the printer erases the drawing with an eraser placed under the pen's mechanism.
 
 ![8](http://i.imgur.com/vt8KJE7.png?1)
 
 

