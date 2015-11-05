#Worksheet 2

##Flowcharts
###Flowchart for randomly shuffling pixels in an image

![Flowchart for randomly shuffling pixels in an image](http://i57.tinypic.com/35cinv5.png)

###Flowchart for changing colours that are above a certain threshold and mostly red, green or blue to completely red, green or blue respectively, then change everything else to black
![Flowchart for changing image to red, green, blue and black](http://i57.tinypic.com/2zisklh.png)

##Pseudocode

###Pseudocode for changing colours that are above a certain threshold and mostly red, green or blue to completely red, green or blue respectively, then change everything else to black

```
Get an image
Add pixels in image to an array  
READ minimumThreshold for colour to be allowed to changed 
DO FUNCTION changeColor(minThreshold, red)
DO FUNCTION changeColor(minThreshold, green)
DO FUNCTION changeColor(minThreshold, blue)
DO FUNCTION changeRestToBlack


FUNCTION changeColor(minThreshold, chosenColourComponent):
  FOR each pixel in image
    Get the RGB component values of current pixel
    IF chosenColourComponent > minimumThreshold AND each of other two colours < 0.9 * chosenColourComponent
      set the chosenColourComponent of the current pixel to 255
      set the other two colour components of the current pixel to 0
    ENDIF
  ENDFOR
END FUNCTION

FUNCTION changeRestToBlack:
  FOR each pixel in image   
    Get the colour of the current pixel
    IF colour of current pixel is NOT (red OR green OR blue)  
      set colour of current pixel to black 0/0/0
    ENDIF
  ENDFOR
END FUNCTION
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
