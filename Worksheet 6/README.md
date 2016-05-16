# Worksheet 6

##Flowchart for NPC Placement
![NPC Placement Flowchart](https://github.com/NecroReindeer/comp110-worksheets/blob/master/Worksheet%206/NPC%20placement%20flow%20chart.png)

##Pseudocode for Maze Generation
```
FUNTION generateLevel()
  Create a list of activeCells
  Choose a random coordinate in the level space
  Create a cell at those coordinates
  Add the created cell at to the list of activeCells
  
  WHILE activeCells is not empty
    DO FUNCTION generateMaze(activeCells)
  ENDWHILE
END FUNCTION

FUNCTION generateMaze(activeCells)
  currentCell = last cell added to activeCells
  IF all edges of currentCell are initialised
    remove currentCell from activeCells
    return
  ENDIF
  
  get a randomDirection where the corresponding edge of currentCell isn't initialised
  
  IF moving in randomDirection from currentCell is still inside the level
    IF no cell exists in randomDirection
      create a cell in randomDirection
      set the edge between the created cell and currentCell to a passage
      add the created cell to activeCells
    ELSE
      set the edge between the created cell and currentCell to a wall
    ENDIF
  ELSE
    set the edge of currentCell in the randomDirection to a wall
  ENDIF

END FUNCTION
```


##UML Diagrams

###Use Case Diagram

###Class Diagram

###State Diagram

###Sequence Diagram
