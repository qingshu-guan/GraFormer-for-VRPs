# Abstract
Deep reinforcement learning (DRL) has recently emerged as a compelling approach for tackling vehicle routing problems (VRPs). However, existing DRL-based methods typically rely on standard transformer architectures that calculate attention over all nodes, leading to prohibitive computational complexity and degraded scalability in large-scale instances. To overcome these challenges, we reformulate VRP as a Markov decision process (MDP) and introduce GraFormer, a graph-oriented transformer designed to learn constructive DRL policies. GraFormer incorporates an encoder-decoder framework within three key innovations. First, during encoding, we design a graph transformer that selectively computes attention interactions based on a structured connectivity graph, significantly improving computational efficiency and preserving critical topological information. Second, in the decoding phase, we integrate Bellman's Principle of Optimality within the MDP framework and depict a dynamic-aware context embedding to capture state transitions and graph variations with fine granularity, enabling adaptive and context-aware decision-making. Third, to enhance exploration in the solution space, we incorporate multiple decoders with identical structures but independent parameters and propose an entropy-regularized loss function to promote diverse route generation. Experimental evaluations across synthetic and real-world datasets demonstrate that our GraFormer consistently outperforms heuristic and DRL-based baselines, achieving improvements of up to \textbf{6.84\%} in solution quality. These findings highlight the potential of our approach in addressing computational and operational challenges of large-scale VRPs, offering robust and versatile solutions for real-world routing applications.

## Paper
This paper is submitted to Neurocomputing.

## Highlights
1. A novel DRL framework is proposed to tackle various VRPs with enhanced efficiency and scalability.
2. A graph-oriented transformer is designed to facilitate effective attention interactions and informative node embeddings.
3. A dynamic-aware context embedding is introduced to capture state transitions, enabling adaptive decision-making.
4. Extensive evaluations on both synthetic and real-world datasets across diverse problem scales demonstrate the superior performance of our proposed approach.

## Dependencies
1. Python>=3.7
2. NumPy
3. SciPy
4. PyTorch=1.3.0
5. tqdm
6. tensorboard_logger
7. Matplotlib (optional, only for plotting)

## Details
For more details, please see the fleet_v3 and fleet_v5 for HCVRP with three vehicles and five vehicles, respectively.
