#### Update the Board class
1. Include the creation of the GUI chessboard in the init method, assign it to self.GUI
2. Update your board list. Currently board is a list of pieces in FEN notation. To move a piece on the GUI we need to know it's tag, and each tag needs to be unique. Make each entry in the board list a list: [FEN, tag]. 

For example, the initial board would be
```  
    board = [[["r","r1"], ["n","n1"], ["b","b1"], ["q","q"], ["k","k"], ["b","b2"], ["n","n2"], ["r","r2"]],
              ["p","p1"], ["p","p2"], ["p","p3"], ["p","p4"], ["p","p5"], ["p","p6"], ["p","p7"], ["p","p8"]],
              [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "]],
              [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "]],
              [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "]],
              [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "], [" "," "]],
              ["P","P1"], ["P","P2"], ["P","P3"], ["P","P4"], ["P","P5"], ["P","P6"], ["P","P7"], ["P","P8"]],
              ["R","R1"], ["N","N1"], ["B","B1"], ["Q","Q"], ["K","K"], ["B","B2"], ["N","N2"], ["R","R2"]]]
```

3. Update the move and check_move methods to use the new board format. For example, where you currently have code that says
```
  if board[column][row].upper() == "P"
```
you will need 
```
  if board[column][row][0].upper() == "P"
```

```
class Board:
  
  def __init__(self, root):
    self.board = ...
    self.pieces = ...
    self.taken = []
    self.GUI = tk.canvas(root, ....)
    
  def print(self):

  def check_move(self, pos, move):
  
  def move(self, pos, move):
```
