인간의 촉각, 시각 feedback의 중요성에 대한 paper도 relation 하는 편
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
### 2. Visuotactile-RL: Learning Multimodal Manipulation Policies with Deep Reinforcement Learning([paper](https://ieeexplore.ieee.org/document/9812019))
- Manipulation task : 1. make contact with an object(square, trianble, sphere) 2. open a hinged door 3. grasp and raise an object
- reference :
  - [2] Reinforcement learning approaches have shown an impressive ability to learn expressible controllers for robotic manipulation  
    
    D. Yarats, R. Fergus, A. Lazaric, and L. Pinto, “Mastering visual continuous control: Improved data-augmented reinforcement learning,” arXiv preprint arXiv:2107.09645, 2021. (DRQ v2 paper)
  - [3] combine camera observations with low-resolution tactile sensing  
      
    M. A. Lee, Y. Zhu, K. Srinivasan, P. Shah, S. Savarese, L. Fei-Fei, A. Garg, and J. Bohg, “Making sense of vision and touch: Selfsupervised learning of multimodal representations for contact-rich tasks,” in 2019 International Conference on Robotics and Automation (ICRA), Montreal, Canada, 2019, pp. 8943–8950.
  - [17] develop a model-based tactile controller using pixel-level feedback to manipulate small objects
  
    S. Tian, F. Ebert, D. Jayaraman, M. Mudigonda, C. Finn, R. Calandra, and S. Levine, “Manipulation by feel: Touch-based control with deep predictive models,” in International Conference on Robotics and Automation (ICRA), 2019, pp. 818–824.
  - [18] develop closed-loop tactile controllers are developed for a dual palm manipulation system able to manipulate objects with dexterity on a table top.
  
    F. R. Hogan, J. Ballester, S. Dong, and A. Rodriguez, “Tactile dexterity: Manipulation primitives with tactile feedback,” in 2020 IEEE international conference on robotics and automation (ICRA). IEEE, 2020, pp. 8863–8869.
  - [19] showcases robotic system capable of swining up and stabilizing objects by using the rich feedback provided by optical tactile sensors to estimate the object’s physical parameters.
  
    C. Wang, S. Wang, B. Romero, F. Veiga, and E. Adelson, “Swingbot: Learning physical features from in-hand tactile exploration for dynamic swing-up manipulation,” in 2020 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS). IEEE, 2020, pp. 5633–5640.
  - [20] model-free RL is used to develop a tactile policy to align and object and environment with a tactile-based feedback insertion policy
  
    S. Dong, D. K. Jha, D. Romeres, S. Kim, D. Nikovski, and A. Rodriguez, “Tactile-rl for insertion: Generalization to objects of unknown geometry,” arXiv preprint arXiv:2104.01167, 2021.
  - [21] shows that a VAE perceptual architecture is effective to extract meaningful state representations from visual and tactile inputs on a simple manipulation task.
  
    H. van Hoof, N. Chen, M. Karl, P. van der Smagt, and J. Peters, “Stable reinforcement learning with autoencoders for tactile and visual data,” in 2016 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), Daejon, Korea, 2016, pp. 3928–3934.
  - [22] use PPO with pixel-level visuotactile inputs to teach a simulated robot arm to perform several tactile-rich tasks in a simulation environment.
    combines RGB and tactile into RGBT 4ch image  
    A. Church, J. Lloyd, R. Hadsell, and N. F. Lepora, “Optical tactile sim-to-real policy transfer via real-to-sim tactile image translation,” 2021. 
- words 
  - intermittent : 간헐적인
- model
  - DRQ v2
  - gated tactile value
  - MP : vision tactile 각각의 encoding network 
  - SP : vision, tactile 같은 encoding network 
- idea
  - tactile gating
  - perception architecture (MP & SP)
  - visual degradation
  - tactile augmenting

### 3. Sim-to-Real Reinforcement Learning for Deformable Object Manipulation  
J. Matas, S. James, and A. J. Davison, “Sim-to-Real Reinforcement Learning for Deformable Object Manipulation,” in Proceedings of The 2nd Conference on Robot Learning, Oct. 2018, pp. 734–743. Accessed: Oct. 19, 2022. [Online]. Available: https://proceedings.mlr.press/v87/matas18a.html
- manipulation goal : to learn deformable object manipulation in an end-to-end manner,
- Reference
  - [14] we employ Reinforcement Learning (RL) to create an algorithm that is task agnostic and can learn many different behaviours based on the definition of a reward and a couple of provided demonstrations. This has been extensively studied in the context of rigid object manipulation  
  D. Quillen, E. Jang, O. Nachum, C. Finn, J. Ibarz, and S. Levine. Deep Reinforcement Learning for Vision-Based Robotic Grasping: A Simulated Comparative Evaluation of Off-Policy Methods. CoRR, 2018.
  - Cloth manipulation에 관련한 paper들
  - rigid object manipulation [21, 22]  
    [21] S. Gu, E. Holly, T. Lillicrap, and S. Levine. Deep Reinforcement Learning for Robotic Manipulation with Asynchronous Off-Policy Updates. International Conference on Robotics and Automation, 2016.  
    [22] J. Peters and S. Schaal. Reinforcement learning of motor skills with policy gradients. Neural Networks.
  - DDPG 관련 논문들
  - sim2real을 위한 관련 논문(domain randomization, additional training in real world)

### 4. Grasp State Assessment of Deformable Objects Using Visual-Tactile Fusion Perception  
S. Cui, R. Wang, J. Wei, F. Li, and S. Wang, “Grasp State Assessment of Deformable Objects Using Visual-Tactile Fusion Perception,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 538–544. doi: 10.1109/ICRA40945.2020.9196787.
- Manipulation goal : how to endow robots the ability to evaluate the grasp state of deformable objects using visualtactile fusion perception.
- Propse the 3D convolution-based visual-tactile fusion DNN to evaluate the grasp state, mimicking the strategy adopted by humans
- Reference
  - Grasp state assesment 관련 paper
  - Visual-tactile fusion perception 관련 paper
    - visual and tactile perception plays an important role in the robotics  
    R. Calandra, A. Owens, M. Upadhyaya, W. Yuan, J. Lin, E. H. Adelson, and S. Levine, “The feeling of success: Does touch sensing help predict grasp outcomes?,” arXiv preprint arXiv:1710.05512, 2017.
    - visuo-tactile fusion in classification[18], object recognition [19], object 3D shape perception [20]
    - end-to-end action-conditional model that learns re-grasping policies from rowed visual-tactile data was proposed in [21]
    - Michelle A. Lee et al. used self-supervision to learn a compact and multimodal representation of RGBs, depth, force-torque, and proprioception for different contact-rich manipulation [22].
- 강화학습을 이용한 manipulation은 아닌 image 와 tactile sensor fusion을 이용한 state assessment(classification)

### 5. Improved Learning of Robot Manipulation Tasks Via Tactile Intrinsic Motivation  
N. Vulin, S. Christen, S. Stevšić, and O. Hilliges, “Improved Learning of Robot Manipulation Tasks Via Tactile Intrinsic Motivation,” IEEE Robotics and Automation Letters, vol. 6, no. 2, pp. 2194–2201, Apr. 2021, doi: 10.1109/LRA.2021.3061308.
- Manipulation goal : Improve robot manipulation task performance of *"pick and place", "push", and "slide task"*  in Mujoco
- Idea :
  - Intrinsic force reward : tactile sensor 값을 이용한 reward(현재 state까지의 tactile force 총합이 임계값 이상일 때 on off reward)
  - Contact-prioritized experience replay
    - contact rich episode가 더 높은 확률로 sampling 되는 replay buffer
- Reference
  - Tactile feedback 관련 논문
  - Intrinsic reward 관련 논문
  - Experience replay 관련 논문