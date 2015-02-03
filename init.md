### Convert your chessboard to OOP
#### Create a Board class
1. Your __init__ method should initialize the board and the pieces dictionary as Board attributes, and a taken pieces list.
2. You should have a print method that prints the board.
3. You should have a check_move method that takes a position (a list) and a move (another list) and returns True or False
depending on whether the move is acceptable or not.
4. A move method that checks if the move is valid, moves the piece if it is, updates the taken list if necessary, and prints
the updated board. 

```
class Board:
  
  def __init__(self):
    self.board = ...
    self.pieces = 
    self.taken = []
    
  def print(self):

  def check_move(self, pos, move):
  
  def move(self, pos, move):
  ```

### Create a Chessboard class. 
1. Use your code from acivity 6 to create the __init__ method.
2. Create a move method which accepts a start position [x,y] and and end position [x, y] and moves the piece at the start
position to the end position. If there is a piece at the end position remove it from the board.
This method does NOT need to check if the move is valid or not, it just does the move on the board.
