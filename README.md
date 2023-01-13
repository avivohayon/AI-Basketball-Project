# AI-Basketball-Project
Teaching a  robot to find and throw ball into a basket using AI models

# Problem Description
The problem we chose to solve is of a robot that learns to pick up the ball and throw the ball
into the basket. This problem consists of two subproblems: pick up the ball and throw the
ball into the basket.
For the first sub problem: robot picks up the ball, we use the Q-Learning which we learned in
this course and implemented in exercise 4. For the second sub problem: robot throws the
ball into the basket, we choose to solve with Genetic Algorithm, and we also implemented a
throw heuristic that tries to learn from the shot what actions should be taken to have a
higher chance of shooting.

#How the game work
We built all the graphics of the game using the 𝑝𝑦𝑔𝑎𝑚𝑒 and 𝑝𝑦𝑚𝑢𝑛𝑘 packages. There are 3
types of objects in the game: STATIC objects that do not move in the game like the limits of
the game, KINEMATIC objects that have all their moves done by the computer and DYNAMIC
objects which are affected by physical data given to objects and space.
The object in the game:
* Robot - has arms, hands, and wheels. The robot can move left or right and up or
down the arms or the hands, when the robot is close enough with it's hands to the
ball it can also pick up the ball, and if the robot is already picking up the ball it can
throw the ball with a certain power at the angles of the hands and arms. The robot is
a kinematic object that receives command from the computer (lines code in the
project).
* Ball - a dynamic object such that it is affected by the gravity of the space of the game
and will stop his velocity.
* Basket - a static object the ball collides with.

During the run of the game the default run is learning of the robot to pick up the ball and
throw the ball into the basket using the genetic algorithm. There is an option to replace the
genetic algorithm with the learning heuristic we implemented and there is another option to
run only the genetic algorithm, in this case the robot throws the ball into the basket from all
possible positions to shooting.

There are several stages in the game, so that in each stage the robot has different possible
actions.
The stages:
* The robot's distance from the ball is over 60 pixels.
* The robot's distance from the ball is less or equal to 60 pixels.
* The robot's hands distance from the ball is close enough to pick up the ball.
* The robot picks up the ball and moves to the shooting position
* The robot grabs the ball and tries to throw it.
* The ball is thrown
