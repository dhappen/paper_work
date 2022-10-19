# paper_work
## 2022 ICRA(The International Conference on Robotics and Automation) paper review
### 1. IPC-GraspSim: Reducing the Sim2Real Gap for Parallel-Jaw Grasping with the Incremental Potential Contact Model([paper](https://arxiv.org/abs/2111.01391))
- IPC(incremental potential contact)라고 하는 computer graphics physics engien 기반으로 만든 grasp simulator
- 현실과 가까운 simulator 상의 soft compliant jaw tips 구현이 가장 큰 contribution
- 4-A Grasp simulation procedure에 대한 설명 참고할 만함
  - Environment의 scenario 순차적으로 설명
  
  
## Related paper
### 1. Visual-Tactile Multimodality for Following Deformable Linear Objects Using Reinforcement Learning([paper](https://arxiv.org/abs/2204.00117))
- Manipulation goal : 한 쪽 끝이 고정된 rope/cable을 고정된 끝에서 시작하여 반대쪽 끝으로 쭉 펼치는 task
- reference : 
  - [13] multiple sensory inputs(tactile sensing, proprioception, vision) are integrated in a grasping stability task (of mugs and bottles).  
  Y. Bekiroglu, D. Song, L. Wang, and D. Kragic, “A probabilisticframework for task-oriented grasp stability assessment,” in 2013 IEEE International Conference on Robotics and Automation. IEEE, 2013, pp. 3040–3047.
- simulation 기반(to real X) 
- model
  - observation
    - kinematic : position of gripper (x, y coordinate), gripper closure state(open or closed)
    - tactile : gripper y축과 맞닿은 rope의 중점의 y position과 rope가 맞닿은 각도
  - evaluation metrics
    - 끝까지 성공하는 경우
    - 중간에 멈춘 경우
    - 도착하지만 떨어뜨린 경우 등등 성공 실패 케이스로 나누어서 classification 
### 2. Visuotactile-RL: Learning Multimodal Manipulation Policies with Deep Reinforcement Learning
- Manipulation goal : 
  

