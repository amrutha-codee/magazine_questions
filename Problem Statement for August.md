# The Fools Who Dream

My ant used to live in Paris. But now, he lives in La La Land, because of lower rents. 
There's only one disadvantage in living there: traveling in La La Land is a nightmare.

La La Land is a rectangular grid with dimensions 'r x c' ('r' rows, 'c' columns). 
Each cell can only have one of three colors: black, red, and white. 
And as you know, ants are colored either black or red. 

But because the mayor of La La Land is a bit crazy, he requires every walking ant in La La Land to follow these rules:

- A walking ant must always be facing in one of the four cardinal directions: north, south, east and west.
- A walking ant that goes into a white cell must keep walking forward, not changing directions.
- A walking ant that goes into a non-white cell with the same color as itself must turn left 90 degrees exactly once, and then keep walking forward.
- A walking ant that goes into a non-white cell with a different color from itself must turn right 90 degrees exactly once, and then keep walking forward.
- A walking ant that goes off the grid is foolish. It is very hard to go back into La La Land without tons of paperwork, so we can assume that a walking ant that goes off the grid will stay outside the grid forever.
As you can see, once an ant begins walking, it doesn't really have any choice. The ant's path is fully determined by the grid.

My ant is a black ant, and he wants to build a house in one of the cells in La La Land, and live there with his friend, which is a red ant. 
They also want to build their garage in one of the cells. The mayor has additional rules regarding houses and garages:

- There must be exactly one house and one garage.
- The cells containing the house and the garage must be different.
- The cells containing the house and the garage must be white cells.
- The house must have exactly one door, and it must point in one of the four cardinal directions. Thus, any walking ant leaving the house will be facing in that direction.
- Luckily, the garage can be entered from any direction, and the house and the garage cells don't have to be adjacent to each other.

Furthermore, my ant and his friend behave in the following way:

- If they reach the cell containing the house again, they just keep walking forward (since that cell is white). Note that this is not considered as "walking out of the house", so in particular, they will keep their current direction and not switch to the direction of the door.
- As soon as they reach the cell containing the garage, they immediately stop walking. (They will then ride their car. Yes, these ants are rich.)
- My ant, which is a black ant, has a special subset BB of the cells that he wants to visit every time he walks out from his house. His friend, which is a red ant, also has a special subset RR of the cells that she wants to visit every time she walks out from her house. They may optionally visit other cells outside their special subset, but they must visit all cells in their special subset. Also, they must end their walk at the garage.

You are friends with the mayor, and so you managed to talk him into changing the colors of the cells for you. The mayor has given you complete freedom to choose the color of every cell in the grid with only one restriction: since the mayor is a red ant, he doesn't like black, so he requires the final grid to have at most 1111 black cells.

Help my ant and his friend achieve their dream, foolish as they may seem, by choosing the coloring of the grid (subject to the mayor's restriction), choosing the locations of the house and the garage, and choosing where the door of the house points to. Or, if it is impossible, say so as well.

"A bit of madness is key
to give us new colors to see.
Who knows where it will lead us?
And that's why they need us."

## Input
The first line contains TT, the number of test cases. The following lines describe the test cases.

The first line of each test case contains four space-separated integers rr, cc, |B|∣B∣ and |R|∣R∣, where |B|∣B∣ and |R|∣R∣ denote the sizes of BB and RR, respectively.
Each of the next |B|∣B∣ lines contains two space-separated integers ii and jj denoting that the cell at row ii and column jj is in BB.
Each of the next |R|∣R∣ lines contains two space-separated integers ii and jj denoting that the cell at row ii and column jj is in RR.

## Output
For each test case, first output a single line containing either POSSIBLE (if it is possible) or FOOLISH (if it is impossible). 
In addition, if it is possible, you need to output at least one valid coloring. 

Output rr more lines, each containing a string of length cc whose letters are one of the following:
B denoting a black cell;
R denoting a red cell;
W denoting a white cell;
G denoting a white cell containing the garage;
^ denoting a white cell containing a house with door pointing north;
v denoting a white cell containing a house with door pointing south;
( denoting a white cell containing a house with door pointing west;
) denoting a white cell containing a house with door pointing east.

We assume that north is up, south is down, west is left, and east is right. Note that:

There must be exactly one cell containing G.
There must be exactly one cell containing one of the characters ^, v, ( or ).
There must be at most 1111 cells containing B.
There may be multiple possible answers; any one will be accepted.

Constraints
1 \leq T \leq 10^51≤T≤10 
5
 
1 \le r, c \le 1501≤r,c≤150
1 \le i \le r1≤i≤r
1 \le j \le c1≤j≤c
0 \le |B|, |R| \le 5000≤∣B∣,∣R∣≤500
The sum of the rcrc in a single file is \le 5\cdot 10^6≤5⋅10 
6
 
The sum of the |B|∣B∣ in a single file is \le 10^6≤10 
6
 
The sum of the |R|∣R∣ in a single file is \le 10^6≤10 
6
