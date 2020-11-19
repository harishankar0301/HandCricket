   Hand Cricket Game in C using Stack ADT as linked list

   

Data Structures Used: Stack as a Linked List

How to Run? 
Please use Linux based OS and GCC to compile and run  (Doesn't compile on Windows Mingw X64 properly)

gcc handcricket.c -o handcricket
./handcricket


Features in the project:

Hand cricket is a game in which any number of players can play a game of cricket using their hands (in this case machines) against each other.
 
It is like any typical hand cricket game where a batsman and a bowler put a number and if the numbers are the same the batsman is out. If not the batsman keeps adding his score.

In real life, the batsman and the bowler put the number simultaneously but here we cannot do that. So we hid or masked the input of the bowler and the batsman to prevent cheating.

This game not only allows one-on-one matches but also team matches where a team can have multiple players. All the players can input their names which we store in an array of structures. In the program, we use it as a pointer to the array of structures.

We also have a feature which allows the teams to have a toss to choose for batting or bowling which we coded using random.

We also have a feature where the batting team can decide the team’s batting order by inputting the order as numbers.

The players are then pushed into a stack according to the batting order in reverse order so that the opener is in the top of the stack and whenever the batsman gets out his record is popped.
 
We also have a well-formatted score board that displays the individual scores of each player from both teams.


Modules/Functions:

void order(struct player *team, int n, node *top, int overs, int innings, int team_no); -- Orders the players based on the input batting order.

void score_board(struct player *team1, struct player *team2, int n)
Displays the final scores of the teams after the match has ended.

void bat(node *top, int overs) Batting function for 1st innings.

void bat2(node *top, int overs, int team_no)  Batting function for 2nd innings

int isEmpty(node *top) -- Checks if stack is empty

node* create()-- Creates the stack as linked list data structure.

void push(node *top, player *p1)-- Pushes an element into the stack.

node* peek(node *top)-- Returns the top element of the stack.

player* pop(node *top)-- Pops the top element from the stack.









