# 2.0-CellGame
# Project Journal
5/25
- Create a canvas for the program
- Create Cell objects with attributes, method: split and get info

? Need to figure out how to move object with mouse

Switch to Python for the Cell Game
- Create Cell Object as parent and Player Object as child
- Player Object: move with mouse; fix trailing circles from player object by screen fill the background
- Create an array of Food Cells

? Collision: need to figure out a better way for circle (middle of the circle?)

- Create split methods for the Player: Need to figure out how to not overlap the circles when draw (create a circle list?)
- Successfully split player’s cell: create a player cells array, when space bar is hit, resize the main player cell, append another cell object (use cell object not player object) into the playerList, update and draw playerList.
- Improved circle collisions, middle of the circle touches instead of edge. This makes it harder for player to eat enemies.
- Finish basic Virus part(arrays, collision, update, draw).
- Finish collisions on virus/food/enemies/player ( except player/player collision or reconnection).

* Need to work on renewal of enemies/ virus and food.
* Need to work on reattachment of players’ cells.
* Need to figure out how to slow down player as size get bigger
* Need to figure out window’s focus	

- Finished renewal of enemies/virus/food
- Figured out angles and speed for the objects to move without touching the mouse
- Mr. V figures out how to following mouse using angle, at a constant speed without touching mouse.
- Finish speed of object based on size and distances
- Get sizes to be equal when split

? Trouble with figuring out how to split

- Basic of splitting: main cell moves toward mouse (shorten distance/speed up), other cells stay at initial position, and both cells are moved by mouse.

? Problems: Glitch when 2 player cells are created; distance cannot be call; dx, dy does not work when a Player Cell Class is created( because the speed is updated by the mouse)

- Work on speed up object when split.(Mr. V ‘s idea: 2 different update states)
- Work on 2 states of Player Class.
- Finished getting the player to speed up when hit space (Set 2 states : 1 for regular with moving mouse and 1 for launching off. Set 2 if statements: The only thing that changed are the dx,dy values and how it bounce off of boundaries. The Player in launch state behaves more like a cell than a controlled player. When launched state is completed within a certain time or if the cell is near the mouse, state is changed back to being regular and reset the timer. Creating the timer: 3 trials. 1st trial, using time.time() function – does not work because time.time() cannot be reset. 2nd trial, setting timer in the Cell Game program instead of class – too confusing because of many while and if statements, 3rd trial: setting timer in the class --  success, timer is set in the beginning of the update, in the regular state, beginning of launch state, end of launch state. (If there’s time, might work on improving the speed control)
- Change split direction according to MouseX
- Finished players’ splitting and sizes (add players’ size values to a list, take the sum of that list and divide by length of list divided by 1)
- Finished reabsorption of cell with a timer.
- Working on splitting and reabsorption of enemies

? Problem: When to Split --- Solution: Create a Cell List that contains all cell, check the x,y values of each, if they are close, split(but only enemies split not player)(check enemies List first than compare enemies List with player’s x and y) ; also to avoid too much splitting, set a timer.
? Problem: Splitting direction
? Problem: Collision of Enemies and their Reabsorption

- Splitting Enemies: Use the same algorithms as player’s splitting
- Figured out how make one enemies follow the other around
- Figured out how to speed up when split

* Need to shorten and make code more efficient
* Need to check collision

- Collison of enemies and Splitting completed.

* Need to reorganize the code and figure out how to make many enemies
* Also need to figure out why doesn’t the enemies split at –x,-y
* Need to figure out how to determine distance from player and enemies ( if close, enemies will split)
6/8
* Need to figure out how to get enemies to split if near player

? Problem: Keep splitting when near player (Mr.V: size of enemies)
? Problem: Enemies does not update ( only one cell appear when split) --- Solution?: Only one enemy can split
? Problem: Shaking Cells when bounce and Removal of one Food cell by 2 or more other cell
