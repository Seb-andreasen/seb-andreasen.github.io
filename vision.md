## Computer Vision

**Project description:** 
Counting can be a bit tricky, so I wanted to make something to make it easier.


### 1. How does the system work?

AI tracks the hands and each frame is treated as a coordinate system, where the relation between the scatters detected by AI determines the number of fingers in the frame. I.e. if the tip of the index finger is below any other point on the index finger the finger isn’t counted.

### 2. What is the output?

Currently the system counts the number of fingers that are held up.


<video controls autoplay muted style="width:100%;height:auto;">
  <source src="/videos/com_vis.mp4" type="video/mp4">
</video>


<br><br>
### 3. Future work
Essentially this technique can be used for so much more such as controlling machines, computers, unlocking doors, etc. 

