# AWS-DeepRacer
Welcome to my AWS DeepRacer repository. This repo showcases my experiment that ranked among the **top 10** in **Egypt_DR_Jan25**. My model achieved a qualifying time of **8.4 seconds** with **0 off-tracks**, demonstrating strong performance in autonomous racing.

This repository includes my approach, training strategy, and key optimizations that contributed to this result.
## About AWS DeepRacer
[AWS DeepRacer](https://aws.amazon.com/deepracer/) is a cloud-based autonomous racing platform that helps developers learn reinforcement learning (RL) through hands-on experience. It provides a **1/18th scale autonomous car**, a **3D racing simulator**, and a **global competition** where participants train RL models to navigate virtual tracks efficiently.

DeepRacer allows users to experiment with different reward functions, hyperparameters, and training strategies to improve their model’s performance. The platform supports **sim-to-real transfer**, enabling trained models to run on physical DeepRacer cars.

Competitions are held at **AWS DeepRacer League** events, where participants compete for the fastest lap times while minimizing penalties like off-tracks and collisions.
## Experiment details
| Category | Details |
|-|-|
|Race type | Time trial |
| Ranking method | Best lap time |
| Style | Individual lap |
| Entry criteria | 3 consecutive laps |
| Off-track penalty | 3 seconds |

### Overview of the Experiment:
The experiment involved training an AWS DeepRacer agent over **10 iterations**, taking **7 hours and 45 minutes**. Different reward functions and hyperparameters were tested throughout the training process to optimize performance. The model achieved a **best lap time of 8.4 seconds** while maintaining **0 off-tracks**.

### The approach
I first focused on enhancing the reward function to improve the agent's learning process. Then, I worked on optimizing speed and hyperparameters together to balance exploration and exploitation for better performance.

### The best lab time
<img src="./aws deepracer video.gif" width="500">

### Iterations:
| Iteration | Model name | Idea |
|-|-|-|
| 1 | [CenterTrack-Stable](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/CenterTrack-Stable/CenterTrack-Stable.md) | **CenterTrack-Stable** optimizes center alignment while minimizing sharp steering. |
| 2 | [EdgeAware-SpeedOptimized](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/EdgeAware-SpeedOptimized/EdgeAware-SpeedOptimized.md) | **EdgeAware-SpeedOptimized** rewards left-edge alignment, smooth steering, high speed, and consistent progress while allowing slight off-track flexibility. |
| 3 | [TrackAware-Optimized](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/TrackAware-Optimized/TrackAware-Optimized.md) | **TrackAware-Optimized** enhances track adherence with a dual-stage off-track penalty while increasing speed for faster, stable laps. |
| 4 | [AdaptivePathOptimizer](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer/AdaptivePathOptimizer.md) | **AdaptivePathOptimizer** optimizes speed and direction based on track curvature using waypoints. |
| 5 | [AdaptivePathOptimizer-Speed](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer-Speed/AdaptivePathOptimizer-Speed.md) | A model that optimizes speed and stability by dynamically adjusting speed and steering based on track conditions. |
| 6 | [AdaptivePathOptimizer-Speed-V2](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer-Speed-V2/AdaptivePathOptimizer-Speed-V2.md) | The model enhances track alignment and speed control for improved performance. |
| 7 | [AdaptivePathOptimizer-Speed-V3](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer-Speed-V3/AdaptivePathOptimizer-Speed-V3.md) | The model encourages speed for improved performance. |
| 8 | [AdaptivePathOptimizer-Left-Speed](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer-Left-Speed/AdaptivePathOptimizer-Left-Speed.md) | The model encourages speed in the right-side turns and the street forward for improved performance. |
| 9 | [AdaptivePathOptimizer-High-Entropy](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer-High-Entropy/AdaptivePathOptimizer-High-Entropy.md) | The model increases exploitation while minimizing exploration. |
| 10 | [AdaptivePathOptimizer-Speed-with-High-Entropy](https://github.com/MohamedSameh410/AWS-DeepRacer/blob/main/Iterations/AdaptivePathOptimizer-Speed-with-High-Entropy/AdaptivePathOptimizer-Speed-with-High-Entropy.md) | The model increases exploitation while minimizing exploration and Increase the speed. |
