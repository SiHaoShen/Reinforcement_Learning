## Reinforcement Learning using Q-table and policy gradient learning

The Q-Tables are developed on

- Frozen Lake environment

- Implemented the Q-table and update it with update rule and action sampling

- Found a trade-off between exploration (choosing random actions) and exploitation (choosing the action with the highest expected reward)

- Policy Gradients: 

  - Model-free reinforcement learning algorithm

  - CartPole environment (see Figure 1)

    | Num  |        Observation         |  Min   |   Max |
    | ---- | :------------------------: | :----: | ----: |
    | 0    |     Cart Position (m)      |  -4.8  |   4.8 |
    | 1    |     Car Velocity (m/s)     |   -∞   |     ∞ |
    | 2    |      Pole Angle (rad)      | -0.418 | 0.418 |
    | 3    | Pole Velocity at tip (1/s) |   -∞   |     ∞ |

  - The episode ends when
    • the pole is more than 12 degrees from vertical, or
    • the cart position is more than 2.4 (center of the cart reaches the edge of or the display), or
    • episode length is greater than 500.

![Output sample](https://git.rwth-aachen.de/si.hao.shen/Reinforcement_Learning/-/raw/master/figure/Figure_1.png)

## Deep Q-networks on OpenAI Gym

- Implemented replay buffers to store ![\Large (s_t, a_t, r_t, s_{t+1}, d_t)](https://latex.codecogs.com/svg.latex?\Large&space;(s_t, a_t, r_t, s_{t+1}, d_t) )-tuples
- Use epsilon greedy strategy for action sampling to introduce randomness into the actions
- Loss function: 
