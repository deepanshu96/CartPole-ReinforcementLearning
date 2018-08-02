# CartPole-ReinforcementLearning


CartPole balancing problem is considered one of the benchmark problems in reinforcement learning. The problem requires to design a model that learns how to balance a pole vertically on a cartwheel. For simplicity, the system is considered to be two dimensional and the cartwheel is allowed to move only in one dimension. OpenAI gym provides simple, easy to use, environments for many such benchmark problems. The CartPole environment allows two actions, +1 and -1, to be taken at any instant. This action corresponds to the direction of application of force on the cart. The observation taken at any instant of the environment is a tuple consisting of horizontal position, horizontal velocity of the cart, angle of inclination of the pole and velocity of the tip of the pole.

### Implementation
* Q-learning algorithm was used to implement the Cartpole challenge which is a straightforward and powerful reinforcement learning algorithm. The given observation states were continuous in nature. At first I tried to implement simply a q learning table with each state in continuous form, due to this large number of states were encountered and as a result both the learning time and learning steps or episodes of the program increased exponentially. 
