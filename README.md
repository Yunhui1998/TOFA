# TOFA

Research in artificial intelligence demonstrates the applicability and flexibility of the reinforcement learning(RL) technique for the dynamic job shop scheduling problem(DJSP). However, the RL-based method will always overfit to the training environment and cannot generalize well to novel unseen situations at deployment time, which is unacceptable in real-world production. For this reason, this paper proposes a highly generalizable reinforcement learning framework named Train once or all (TOFA)  for the dynamic job shop scheduling problem. The trivial and non-trivial states are distinguished in the formulation process, and the DJSP is formulated as a semi-Markov decision process. A novel graph representation learning method based on attention mechanism and spatial pyramid pooling is implemented to compress the disjunctive graphs of different-size DJSP into fixed-length feature vectors. Combining the proposed dynamic frame skipping and an improved prioritized experience replay method that considers the sample quality, TOFA shows superb generalization capability, outperforms practically favored dispatching rules and even instance-by-instance training RL-based schedulers on various benchmark DJSP. Additionally, we proved that TOFA acquires a transferable scheduling policy that can be used to schedule a whole new DJSP  without additional training.

# Gantt

We test TOFA on JSP instances in [OR-LIBRARY](http://people.brunel.ac.uk/~mastjjb/jeb/orlib/files/jobshop1.txt), and generate the corresponding Gantt chart. You can jump to the results via the link below.

