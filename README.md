# Tic_tac_toe
The classic Tic-Tac-Toe game (also called Noughts and Crosses) or Xs and Os is a paper-and-pencil game for two players, X and O, who take turns marking the spaces in a 3×3 grid. The player who succeeds in placing three of their marks in a horizontal, vertical, or diagonal row is the winner.

It has been built using javascript, along with some nice HTML & CSS. It contains the implementation where the bot always wins or it ties. But never looses that is the bot is undefetable.In this code, I've used minimax algorithm to help the computer where to go for the next move and win the puzzle.

# Combinatorics :
When considering only the state of the board, and after taking into account board symmetries (i.e. rotations and reflections), there are only 138 terminal board positions. A combinatorics study of the game shows that when "X" makes the first move every time, the game is won as follows :

91 distinct positions are won by (X)
44 distinct positions are won by (O)
3 distinct positions are drawn (often called a "cat's game")

Pseudocode
function minimax(node, depth, isMaximizingPlayer, alpha, beta):

    if node is a leaf node :
        return value of the node
    
    if isMaximizingPlayer :
        bestVal = -INFINITY 
        for each child node :
            value = minimax(node, depth+1, false, alpha, beta)
            bestVal = max( bestVal, value) 
            alpha = max( alpha, bestVal)
            if beta <= alpha:
                break
        return bestVal

    else :
        bestVal = +INFINITY 
        for each child node :
            value = minimax(node, depth+1, true, alpha, beta)
            bestVal = min( bestVal, value) 
            beta = min( beta, bestVal)
            if beta <= alpha:
                break
        return bestVal
        // Calling the function for the first time.
        minimax(0, 0, true, -INFINITY, +INFINITY)

# Minimax Algorithm Visualisation
![image](https://user-images.githubusercontent.com/76108859/133998104-faf8a395-4bb4-4bdb-b9b7-b5700b82621a.png)

# Screenshots

This is the first page we see on the screen


![image](https://user-images.githubusercontent.com/76108859/133998431-0cdfe3d0-3a94-4414-89e1-1b13e7548741.png)

Lets play. The bot plays X and we play O.

![image](https://user-images.githubusercontent.com/76108859/133998601-0d71aa85-5ec0-4b1c-92bf-988a84466c6e.png)


![image](https://user-images.githubusercontent.com/76108859/133998742-e5f15f48-92a1-4bb9-b8aa-bd5b5d04de79.png)


![image](https://user-images.githubusercontent.com/76108859/133998817-1405c791-0011-406d-b1fd-8f879f06d42f.png)


As you can see , its always the bot that wins!

