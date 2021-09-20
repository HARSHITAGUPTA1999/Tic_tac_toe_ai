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

![image](https://user-images.githubusercontent.com/76108859/134028076-cec81ea2-375d-42e1-be2d-dcc2e28c947f.png)

Lets play. The bot plays X and we play O.


![image](https://user-images.githubusercontent.com/76108859/134028225-013e73f9-3723-409b-9868-fa7519d78eac.png)



![image](https://user-images.githubusercontent.com/76108859/134028431-b39f246c-0984-4e7d-841c-9c3890cf4221.png)


![image](https://user-images.githubusercontent.com/76108859/134028543-56ad4fb1-e7a6-4d93-a2bc-bf0469f9ecc5.png)



As you can see , its always the bot that wins!

