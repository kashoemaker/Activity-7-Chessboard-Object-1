#### Update the Board class
1. Include the creation of the GUI chessboard in the init method, assign it to self.GUI
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

When a piece is moved the GUI will need to be updated. There are a couple of ways to do this. The simplest method is to just redraw the entire GUI using self.board. The most efficient method, which we will use, is to tag each piece on the GUI board. Using this method we can move one piece using the tag instead redrawing the entire board. 

Each piece on the GUI board will need to have a unique tag for this to work, and there will have to be a way to associate a piece on the list board to the piece on the GUI board. Therefore:

2. Update your list board. Currently the list board is a list of pieces in FEN notation. Make each entry in the list board a list: [FEN, tag]. 

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

4. Create tags for the pieces that you put in the GUI in Activity 6. This should be simple, just update the double loop you already have.
