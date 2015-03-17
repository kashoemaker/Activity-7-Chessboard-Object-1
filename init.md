#### Update the Board class
1. Include the creation of the GUI chessboard in the init method, assign it to self.GUI
2. Update your board list. Currently board is a list of pieces in FEN notation. To move a piece on the GUI we need to know it's tag, make each entry in the board list a list: [FEN, tag].
3. Update the move method so that it moves the corresponding piece on the board.

```
class Board:
  
  def __init__(self, root):
    self.board = ...
    self.pieces = 
    self.taken = []
    self.GUI = root
    
  def print(self):

  def check_move(self, pos, move):
  
  def move(self, pos, move):
  ```
