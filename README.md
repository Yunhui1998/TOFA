# TOFA

***This is the support material for paper : "You Only Train Once: A highly generalizable reinforcement learning method for dynamic job shop scheduling problem"***

## Abstract

Research in artificial intelligence demonstrates the applicability and flexibility of the reinforcement learning(RL) technique for the dynamic job shop scheduling problem(DJSP). However, the RL-based method will always overfit to the training environment and cannot generalize well to novel unseen situations at deployment time, which is unacceptable in real-world production. For this reason, this paper proposes a highly generalizable reinforcement learning framework named Train once or all (TOFA)  for the dynamic job shop scheduling problem. The trivial and non-trivial states are distinguished in the formulation process, and the DJSP is formulated as a semi-Markov decision process. A novel graph representation learning method based on attention mechanism and spatial pyramid pooling is implemented to compress the disjunctive graphs of different-size DJSP into fixed-length feature vectors. Combining the proposed dynamic frame skipping and an improved prioritized experience replay method that considers the sample quality, TOFA shows superb generalization capability, outperforms practically favored dispatching rules and even instance-by-instance training RL-based schedulers on various benchmark DJSP. Additionally, we proved that TOFA acquires a transferable scheduling policy that can be used to schedule a whole new DJSP  without additional training.

## Method

*need a pic*

## Performance

*need a table*

Overview of TOFA. 

## Gantt

We test TOFA on JSP instances in [OR-LIBRARY](http://people.brunel.ac.uk/~mastjjb/jeb/orlib/files/jobshop1.txt), and generate the corresponding Gantt chart. You can jump to the results via the link below.

### FT

[ft06](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft06-59.html); 

### LA

[la01](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la01-666.html); [la04](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la04.html); [la05](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la05-593.html); [la06](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la06-926.html); [la07](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la07-917.html); [la08](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la08-863.html); [la09](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la09-951.html); [la10](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la10-958.html); 

[la12](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la12-1039.html); [la13](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la13-1150.html); [la14](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la14-1292.html); [la15](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la15-1314.html); [la16](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la16-1108.html); 

[la22](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la22-1091.html); [la23](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la23-1134.html); [la24](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la24-1149.html); [la28](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la28-1406.html); [la29](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la29-1343.html); [la30](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la30-1565.html); 

[la32](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la32-1883.html); [la33](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la33-1755.html); [la34](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la34-1791.html); [la35](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la35-1897.html); [la37](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la37-1606.html); [la39](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la39-1534.html); 

### ORB

[orb01](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb01-1148.html); [orb02](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb02-997.html); [orb03](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb03-1179.html); [orb08](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb08-1033.html); [orb10](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb10-1079.html); 

### SWV

[swv02](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv02-2070.html); [swv07](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv07-2047.html); [swv08](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv8-1852.html); 

[swv16](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv16-2924.html); [swv17](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv17-1802.html); [swv20](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv20-2823.html); 

### YN

[yn1](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn1-1033.html); [yn2](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn2-1067.html); [yn3](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn3-1035.html); [yn4](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn4-1170.html); 