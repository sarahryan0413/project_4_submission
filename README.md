# Machine Learning and Tic-Tac-Toe

This project is meant to demonstrate how machine learning can be used to analyze the game of tic-tac-toe and determine the optimal moves to achieve the best outcome possible in a given game. The dataset used provided every possible outcome and board position. In processing this data, we found that we needed a model that could handle the non-binary outcomes of the game (Win/Loss/Tie). 


### Methodology

This dataset contains 255,168 rows, where each row represents a complete Tic-Tac-Toe game, capturing the full sequence of moves made by both players. The structure supports game-by-game analysis and is ideal for studying strategies, move patterns, and outcomes.
Key Features:
Player X always goes first.
Moves are listed in order, alternating between X and O 

To prepare the data, we utilized a PySpark SQL database to hold the data that we would use for training and testing of the model. Initially, we used the RandomForest model for our dataset. This gave adequate accuracy for Win or Loss conditions, but did not account for Tie outcomes. From here, we further cleaned the data and changed models to decision tree. Additionally, we increased the depth of the decision tree from 10 to 20 to account for a larger set of possible game outcomes.

### Additional Learnings and Conclusions
When analyzing the data, we see patterns emerge in the gameplay. 
![image](https://github.com/user-attachments/assets/d170d405-e081-49bf-85e8-75b67addd800)

It is much more advantageous to have the first move in a game like this with so few moves. 

![image](https://github.com/user-attachments/assets/2fb16696-7bcd-4340-b2f4-24603471cd2d)

![image](https://github.com/user-attachments/assets/b5db3fb4-87e6-46b5-8dbc-04c7aab72034)


Utilizing what we learned here with machine learning, we think it would be interesting to scale up to more complex board games such as Connect 4 or sports with more complex decision making like baseball. We also see the potential with learning this children's game in exploring early childhood development and logical thinking in children.


### Reference for data source
The data used was sourced from: https://www.kaggle.com/datasets/anthonytherrien/tic-tac-toe-game-dataset
