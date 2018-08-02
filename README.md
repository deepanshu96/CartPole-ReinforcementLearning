# CartPole-ReinforcementLearning

* [Program Code File](https://github.com/deepanshu96/CartPole-ReinforcementLearning/blob/master/QlearnAI.ipynb)
* [Video Link Youtube](https://youtu.be/b8coNNme4cw)

CartPole balancing problem is considered one of the benchmark problems in reinforcement learning. The problem requires to design a model that learns how to balance a pole vertically on a cartwheel. For simplicity, the system is considered to be two dimensional and the cartwheel is allowed to move only in one dimension. OpenAI gym provides simple, easy to use, environments for many such benchmark problems. The CartPole environment allows two actions, +1 and -1, to be taken at any instant. This action corresponds to the direction of application of force on the cart. The observation taken at any instant of the environment is a tuple consisting of horizontal position, horizontal velocity of the cart, angle of inclination of the pole and velocity of the tip of the pole.

### Implementation

* Q-learning algorithm was used to implement the Cartpole challenge which is a straightforward and powerful reinforcement learning algorithm. The given observation states were continuous in nature. At first I tried to implement simply a q learning table with each state in continuous form, due to this large number of states were encountered and as a result both the learning time and learning steps or episodes of the program increased exponentially. 


* Next I reduced the observation state space by first discretizing the observation into integers into a number of buckets. The components of the observation state were x, x_dot, theta, theta_dot where x and x_dot were the position and velocity and theta and theta_dot were the angle of pole and angle rate of change. For the problem I removed the x and x_dot component, thus the solution converged faster than the previous approach. 


* After the above modifications the solution was still not being obtained and then I decided to use adaptive learning and exploration rate in which they were decreased with passage of time using modify_epsilon() and modify_alpha() functions in the program code. This made a huge difference and the algorithm was able to learn in 150 to 200 episodes. Although the cart was going out of the bounds but the progress was so slow that it completed 200 time steps before it. 

### Results

* #### 100 Generations
<img src = "https://github.com/deepanshu96/CartPole-ReinforcementLearning/blob/master/ext/100gen.gif" width = "350">

* #### 125 Generations
<img src = "https://github.com/deepanshu96/CartPole-ReinforcementLearning/blob/master/ext/125gen.gif" width = "350">

* #### 200 Generations
<img src = "https://github.com/deepanshu96/CartPole-ReinforcementLearning/blob/master/ext/200gen.gif" width = "350">

* Q-learning algorithm is able to complete the given task in about 150 to 200 generations or episodes in which it completes more than 200 time steps quite easily without going out of the bounds of the environment. 

<img src = "https://github.com/deepanshu96/CartPole-ReinforcementLearning/blob/master/ext/Screen%20Shot%202018-08-02%20at%209.11.39%20PM.png" width = 600>

### References
* https://medium.com/@tuzzer/cart-pole-balancing-with-q-learning-b54c6068d947
* https://ferdinand-muetsch.de/cartpole-with-qlearning-first-experiences-with-openai-gym.html
* https://gym.openai.com/docs/
