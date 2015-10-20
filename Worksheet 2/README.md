#Worksheet 2 (draft)

##Flowcharts
###Flowchart for randomly shuffling pixels in an image

![Flowchart for randomly shuffling pixels in an image](http://i57.tinypic.com/35cinv5.png)

##Pseudocode

###Pseudocode for changing colours that are above a certain threshold and mostly red, green or blue to completely red, green or blue respectively, then change everything else to black

```
Main:
Get an image
Add pixels in image to an array  
READ minimumThreshold for colour to be changed 
DO Change reds to red  
DO Change greens to green  
DO Change blues to blue  
DO Change rest to black

Change reds to red:
FOR each pixel in image
  Get the RGB values of current pixel  
  IF red value > minimumThreshold AND green value < 0.9 * red value	AND blue value < 0.9 * red value  
    set colour of current pixel to red 255/0/0
  ENDIF
ENDFOR

Change greens to green:
FOR each pixel in image   
  Get the RGB values of pixel at current index 
  IF green value > minimumThreshold AND red value < 0.9 * green value	AND blue value < 0.9 * green value  
    set colour of current pixel to green 0/255/0  
  ENDIF
ENDFOR

Change blues to blue:
FOR each pixel in image
  Get the RGB values of current pixel  
  IF blue value > minThreshold AND red value < 0.9 * blue value	AND green value < 0.9 * blue value  
    set colour of current pixel to blue 0/0/255
  ENDIF
ENDFOR

Change rest to black:
FOR each pixel in image   
  Get the RGB values of current pixel
  IF colour is NOT (red OR green OR blue)  
    set colour of current pixel to black 0/0/0
  ENDIF
ENDFOR
```			

###Pseudocode for randomly shuffling pixels in an image

```
Get a startingImage
Create a copyOfImage  
Add pixels in original image to an array
Add pixels in copyOfImage to an array
Create a list of integers containing all index numbers of pixel array

FOR each pixel in startingImage
  Get the colour of the current pixel in startingImage
  Pick a randomNumber from the list of numbers
  Change pixel at index randomNumber in copyOfImage to the colour of pixel chosen from startingImage 
  Remove the randomNumber from the list of numbers
ENDFOR
```
