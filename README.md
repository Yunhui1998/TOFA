# TOFA

***This is the support material for paper : "You Only Train Once: A highly generalizable reinforcement learning method for dynamic job shop scheduling problem"***

## Abstract

Research in artificial intelligence demonstrates the applicability and flexibility of the reinforcement learning(RL) technique for the dynamic job shop scheduling problem(DJSP). However, the RL-based method will always overfit to the training environment and cannot generalize well to novel unseen situations at deployment time, which is unacceptable in real-world production. For this reason, this paper proposes a highly generalizable reinforcement learning framework named Train once or all (TOFA)  for the dynamic job shop scheduling problem. The trivial and non-trivial states are distinguished in the formulation process, and the DJSP is formulated as a semi-Markov decision process. A novel graph representation learning method based on attention mechanism and spatial pyramid pooling is implemented to compress the disjunctive graphs of different-size DJSP into fixed-length feature vectors. Combining the proposed dynamic frame skipping and an improved prioritized experience replay method that considers the sample quality, TOFA shows superb generalization capability, outperforms practically favored dispatching rules and even instance-by-instance training RL-based schedulers on various benchmark DJSP. Additionally, we proved that TOFA acquires a transferable scheduling policy that can be used to schedule a whole new DJSP  without additional training.

## Method

The overall framework of TOFA is shown in Fig. TOFA aims to train the model only once and use it for any size of JSP instance with good performance. The core component is the GRL module that converts a disjunctive graph of arbitrary size into a fixed-length vector. The remaining tricks are improved prioritized experience replay, non-trival state skipping, and heuristic rule-based actions. 

<img src=".\README pic\TOFA.png" alt="Overview of TOFA"/>

## Performance

A large number of methods that we tested on all instances in OR-LIBRARY were used to compare the performance of TOFA. These methods include：

1. SDRs: FIFO, LIFO, LPT, SPT, LTPT, STPT, MOR, LOR
2. Using random SDRs for a period of time
3. MDRs: MOR+LPT, LOR+SPT, FCFS*S, SI/Q
4. Meta-Heuristic: GA, GWO and DE
5. Other reinforcement learning: PPO, D3QPN
6. Different GRL modules: GNN, GAT, GKAT, MAX (maximum pooling), AVG (average pooling), Padding zero
7. Different frame skipping methods: Bellman
8. Optimal strategy

A detailed description of these methods can be found in the [full paper]()(*need paper link*).

The full results of the test are stored in the [table](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/result/result.htm). 

## Gantt

We test TOFA on JSP instances in [OR-LIBRARY](http://people.brunel.ac.uk/~mastjjb/jeb/orlib/files/jobshop1.txt), and generate the corresponding Gantt chart. You can jump to the results via the link below. Note that either clicking on the **image** or the **title** will bring you to the corresponding Gantt chart. 

### FT

[ft06](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft06-59.html); [ft10](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft10-1059.html); [ft20](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft20-1244.html); 

<p float="left">
    <a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft06-59.html"><img src=".\README pic\ft06.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft10-1059.html"><img src=".\README pic\ft10.png" width="400" />
</p>

<p float="left">
    <a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/ft20-1244.html"><img src=".\README pic\ft20.png" width="400" />
</p>

### LA

[la01](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la01-666.html); [la02](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la02-693.html); [la03](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la03-613.html); [la04](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la04.html); [la05](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la05-593.html); [la06](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la06-926.html); [la07](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la07-917.html); [la08](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la08-863.html); [la09](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la09-951.html); [la10](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la10-958.html); 

[la11](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la11-1222.html); [la12](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la12-1039.html); [la13](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la13-1150.html); [la14](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la14-1292.html); [la15](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la15-1314.html); [la16](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la16-1108.html); [la17](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la17-819.html); [la18](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la18-937.html); [la19](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la19-916.html); [la20](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la20-1013.html); 

[la21](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la21-1197.html); [la22](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la22-1091.html); [la23](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la23-1134.html); [la24](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la24-1149.html); [la25](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la25-1112.html); [la26](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la26-1412.html); [la27](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la27-1459.html); [la28](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la28-1406.html); [la29](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la29-1343.html); [la30](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la30-1565.html); 

[la31](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la31-1826.html); [la32](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la32-1883.html); [la33](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la33-1755.html); [la34](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la34-1791.html); [la35](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la35-1897.html); [la36](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la36-1459.html); [la37](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la37-1606.html); [la38](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la38-1377.html); [la39](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la39-1534.html); [la40](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la40-1384.html); 

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la01-666.html"><img src=".\README pic\la01.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la02-693.html"><img src=".\README pic\la02.png" width="400" /></p>
<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la03-613.html"><img src=".\README pic\la03.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la04.html"><img src=".\README pic\la04.png" width="400" /></p>
<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la05-593.html"><img src=".\README pic\la05.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la06-926.html"><img src=".\README pic\la06.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la07-917.html"><img src=".\README pic\la07.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la08-863.html"><img src=".\README pic\la08.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la09-951.html"><img src=".\README pic\la09.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la10-958.html"><img src=".\README pic\la10.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la11-1222.html"><img src=".\README pic\la11.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la12-1039.html"><img src=".\README pic\la12.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la13-1150.html"><img src=".\README pic\la13.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la14-1292.html"><img src=".\README pic\la14.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la15-1314.html"><img src=".\README pic\la15.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la16-1108.html"><img src=".\README pic\la16.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la17-819.html"><img src=".\README pic\la17.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la18-937.html"><img src=".\README pic\la18.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la19-916.html"><img src=".\README pic\la19.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la20-1013.html"><img src=".\README pic\la20.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la21-1197.html"><img src=".\README pic\la21.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la22-1091.html"><img src=".\README pic\la22.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la23-1134.html"><img src=".\README pic\la23.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la24-1149.html"><img src=".\README pic\la24.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la25-1112.html"><img src=".\README pic\la25.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la26-1412.html"><img src=".\README pic\la26.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la27-1459.html"><img src=".\README pic\la27.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la28-1406.html"><img src=".\README pic\la28.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la29-1343.html"><img src=".\README pic\la29.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la30-1565.html"><img src=".\README pic\la30.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la31-1826.html"><img src=".\README pic\la31.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la32-1883.html"><img src=".\README pic\la32.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la33-1755.html"><img src=".\README pic\la33.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la34-1791.html"><img src=".\README pic\la34.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la35-1897.html"><img src=".\README pic\la35.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la36-1459.html"><img src=".\README pic\la36.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la37-1606.html"><img src=".\README pic\la37.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la38-1377.html"><img src=".\README pic\la38.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la39-1534.html"><img src=".\README pic\la39.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/la40-1384.html"><img src=".\README pic\la40.png" width="400" />
</p>

### ORB

[orb01](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb01-1148.html); [orb02](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb02-997.html); [orb03](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb03-1179.html); [orb04](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb04-1122.html); [orb05](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb05-1004.html); [orb06](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb06-1101.html); [orb07](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb07-432.html); [orb08](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb08-1033.html); [orb09](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb09-1033.html); [orb10](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb10-1079.html); 

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb01-1148.html"><img src=".\README pic\orb01.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb02-997.html"><img src=".\README pic\orb02.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb03-1179.html"><img src=".\README pic\orb03.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb04-1122.html"><img src=".\README pic\orb04.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb05-1004.html"><img src=".\README pic\orb05.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb06-1101.html"><img src=".\README pic\orb06.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb07-432.html"><img src=".\README pic\orb07.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb08-1033.html"><img src=".\README pic\orb08.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb09-1033.html"><img src=".\README pic\orb09.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/orb10-1079.html"><img src=".\README pic\orb10.png" width="400" />
</p>

### SWV

[swv01](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv01-1956.html); [swv02](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv02-2070.html); [swv03](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv03-1680.html); [swv04](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv04-1781.html); [swv05](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv05-1668.html); [swv06](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv06-2161.html); [swv07](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv07-2047.html); [swv08](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv08-1852.html); [swv09](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv09-2083.html); [swv10](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv10-2131.html); 

[swv11](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv11-3465.html); [swv12](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv12-3492.html); [swv13](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv13-3681.html); [swv14](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv14-3498.html); [swv15](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv15-3505.html); [swv16](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv16-2924.html); [swv17](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv17-1802.html); [swv18](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv18-2823.html); [swv19](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv19-2900.html); [swv20](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv20-2823.html); 

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv01-1956.html"><img src=".\README pic\swv01.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv02-2070.html"><img src=".\README pic\swv02.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv03-1680.html"><img src=".\README pic\swv03.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv04-1781.html"><img src=".\README pic\swv04.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv05-1668.html"><img src=".\README pic\swv05.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv06-2161.html"><img src=".\README pic\swv06.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv07-2047.html"><img src=".\README pic\swv07.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv08-1852.html"><img src=".\README pic\swv08.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv09-2083.html"><img src=".\README pic\swv09.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv10-2131.html"><img src=".\README pic\swv10.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv11-3465.html"><img src=".\README pic\swv11.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv12-3492.html"><img src=".\README pic\swv12.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv13-3681.html"><img src=".\README pic\swv13.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv14-3498.html"><img src=".\README pic\swv14.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv15-3505.html"><img src=".\README pic\swv15.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv16-2924.html"><img src=".\README pic\swv16.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv17-1802.html"><img src=".\README pic\swv17.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv18-2823.html"><img src=".\README pic\swv18.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv19-2900.html"><img src=".\README pic\swv19.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/swv20-2823.html"><img src=".\README pic\swv20.png" width="400" />
</p>

### YN

[yn1](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn1-1033.html); [yn2](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn2-1067.html); [yn3](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn3-1035.html); [yn4](http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn4-1170.html); 

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn1-1033.html"><img src=".\README pic\yn1.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn2-1067.html"><img src=".\README pic\yn2.png" width="400" />
</p>

<p float="left">
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn3-1035.html"><img src=".\README pic\yn3.png" width="400" />
<a href="http://htmlpreview.github.io/?https://github.com/Yunhui1998/TOFA/blob/main/Gantt/yn4-1170.html"><img src=".\README pic\yn4.png" width="400" />
</p>
