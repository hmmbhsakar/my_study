# Other Tools

## OBS

### How To

#### Make Shared Screen Background Invisible
Let's say I have shared my laptop screen and it is leading to also sharing of the background even in the areas where there is no applications placed, That looks clumsy, So, to make it clean, one can make the background hide and just window on top of the background would be visible. 
Steps:
1. Change the color of the Background to a custom solid color which is generally not used in most of the application Window in either black/white there. Copy the Hex of this Color from the Custom Background Color Pick
2. In OBS select the screen to hide background and add Filter `Chroma Key`. Now change the Key Color Type to Custom Color, In Key Color go to select color and then paste the Hex color code copied. 
3. Make Similarity, Smoothness, Key Color Spill Reduction to 1
4. Save It. 