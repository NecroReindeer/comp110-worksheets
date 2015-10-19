#Worksheet 2

##Pseudocode

###Changing colours that are above a certain threshold of red/green/blue to completely red/green/blue and everything else to black

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
  Get the RGB values of pixel at current index  
  IF red value > minimumThreshold AND green value < 0.9 * red value	AND blue value < 0.9 * red value  
    set colour of pixel at current index to red 255/0/0
  ENDIF
ENDFOR

Change greens to green:
FOR each pixel in image   
  Get the RGB values of pixel at current index 
  IF green value > minimumThreshold AND red value < 0.9 * green value	AND blue value < 0.9 * green value  
    set colour of pixel at current index to green 0/255/0  
  ENDIF
  Add 1 to index
ENDFOR

Change blues to blue:
FOR each pixel in image
  Get the RGB values of pixel at current index  
  IF blue value > minThreshold AND red value < 0.9 * blue value	AND green value < 0.9 * blue value  
    set colour of pixel at current index to blue 0/0/255
  ENDIF
ENDFOR

Change rest to black:
FOR each pixel in image   
  Get the RGB values of pixel at current index  
  IF colour is NOT (red OR green OR blue)  
    set colour of pixel at current index to black 0/0/0
  ENDIF
  Add 1 to index
ENDFOR
```			
