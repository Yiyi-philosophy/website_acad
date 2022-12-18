# Summarize for some papers.

## MLsys

### SLIDE : IN DEFENSE OF SMART ALGORITHMS OVER HARDWARE ACCELERATION FOR LARGE-SCALE DEEP LEARNING SYSTEMS

  - Abstract

    - It's hard to maintain **enough capacity to memorize many** parameters **and** obtain state-of-the-art accuracy **when training** large neural networks.

    - **Specialized hardware** for model training **is expensive** and hard to generalize**, compared to GPUs.**

    - This paper propose SLIDE (Sub-Linear Deep learning Engine) that uniquely blends **smart randomized algorithms**, with **multi-core parallelism and workload optimization**. 

    - Performance

      - 44 core CPU **=** **3.5*1** Tesla V100

      - **1** SLIDE **= 10x TF**

  - 1 Intro

    - the idea of **adaptive sparsity** or **adaptive dropouts**

    - design a system that can effectively leverage the **computational advantage** and at the same time compensate for the **hash table overheads using limited (only a few cores) parallelisms**. 

    - Our Contributions

      - This unique possibility is because the **parallelism** in SLIDE is **naturally asynchronous** by design. We have our code and benchmark scripts for reproducibility.

      - in designing the LSH based sparsification to minimize the computational overheads to a few **memory lookups** only (**truly O(1)**)

        - The implementation further takes advantage of the sparse gradient updates to achieve negligible update conflicts, which creates ideal settings for Asynchronous SGD

      - SLIDE is a memory-bound application

        - With careful workload and cache optimizations (eg. Transparent Hugepages) and a data access pattern (eg. SIMD instructions), we further speed up SLIDE by roughly 1.3x

  - 2 LOCALITY SENSITIVE HASHING

    <img src="Summarize.assets/image (3).png" alt="image (3)" width="100%" />

      - **Initialization:**

      - **Sparse Feed-Forward Pass with Hash Table Sampling:**

        

    <img src="Summarize.assets/image (4).png" alt="image (4)" width="50%" />

      - **Sparse Backpropagation or Gradient Update:**

        - **Here we use the classical backpropagation message passing type implementation rather than vector multiplication based.**

        - **take full advan-tage of sparsity.**

      - **Update Hash Tables after Weight Updates:**

        - Updating neurons typically involves deletion from the old bucket followed by an addition to the new bucket, which can be expensive.

      - **OpenMP Parallelization across a Batch:**

        - Each data instance in the batch runs in a separate thread and its gradients are computed in parallel.

      - **The extreme sparsity and randomness in gradient updates allow us to asynchronously parallelize the accumulation step of the gradient across different training data without leading to a considerable amount of overlapping updates.**

  - 4 REDUCING OVERHEAD

    - 4.2 Updating Overhead

      - Dynamically change the update frequency of hash tables to reduce the overhead.

        -  $N_0 e^{\lambda i}$

      - The gradient updates in the initial stage of the training are larger than those in the later stage

      - Reservoir sampling algorithm

  - 6 CONCLUSION AND FUTURE WORK

    - Our system SLIDE is a combination of carefully tailored randomized hashing algorithms with the right data structures that allow asynchronous parallelism.

    - Our next steps are to extend SLIDE to include convolutional layers. 

    - SLIDE has unique benefits when it comes to **random memory accesses** and **parallelism**. We anticipate that a **distributed implementation** of SLIDE would be very appealing because the communication costs are minimal due to sparse gradients.


### QUADRALIB: A PERFORMANT QUADRATIC NEURAL NETWORK LIBRARY FOR ARCHITECTURE OPTIMIZATION AND DESIGN EXPLORATION

- Abstract

  - DNNs' success depends on many supporting libraries.

  - QDNNs ($WX^2+b$) show better **non-linearity** and **learning capability**

  - In this paper, author proposed a new QDNN neuron architecture design, and further developed QuadraLib. 

  - **good accuracy** and computation consumption

- 1 Intro

  - the benefits of QDNNs stem from the unique characteristics of the second-order polynomial form: 

    - (1) **stronger non-linearity**, hence improved capability for feature extraction

    - (2) **higher model efficiency** as QDNN can approximate polynomial decision boundaries using smaller network depth/width

  - Contribution

    - four types of QDNN

    - new quadratic neuron architecture

    - QuadraLib

    - experiment

- 2 DRAWBACKS OF THE EXISTING QDNN NEURON ARCHITECTURE DESIGN

  - P1 Approximation Capability Issue:

  - P2 Computation Complexity Issue:

  - P3 Converge Performance Issue:

    - second-order term in QDNNs will introduce critical gradient vanishing issue

  - P4 Implementation Feasibility Issue:

    - need to rewrite the entire convolution operation to add extra multiplication between W and the second X.

  - P5 Structure Design Issue:

  - P6 Memory Usage Issue:

- 3 QDNN NEURON ARCHITECTURE OPTIMIZATION

  - 3.1 New Neuron Architecture Design

    <img src="Summarize.assets/image (5).png" alt="image (5)" width="50%" />

    - introduce extra trainable parameters on the second-order term

    - other term to prevent the gradient vanishing

    - Hardmard product

    - easily assembled

  - 3.2 Theoretical Performance Analysis

    - Extra Weights and Linear Term for Approximation Capa-
bility (P1) Improvement:

    - Hadamard Product for Computation Complexity (P2) Optimization:

    - Linear Term for Converge Performance ( P3 ) Enhancement

    - First-order Neuron Combination for Implementation Feasibility ( P4 ) Improvement

  -  4 QUADRALIB FOR QDNN DESIGN EXPLORATION

      <img src="Summarize.assets/image (6).png" alt="image (6)" width="100%" />

    - In **Model** Level, QuadraLib defines a set of encapsulated layer modules

      - auto-builder for converting first-order model to a corresponding QDNN version

    - In **Training**/Inference Level, QuadraLib leverages a memory profiler to monitor the memory cost of the generated QDNN model 

    - In **Application** Level, QuadraLib also provides model analysis tools such as activation and weight/gradient distribution **visualization**.

    - 4.3 QuadraLib Training Optimization

      - Hybrid Back-propagation for Memory Efficiency

      <img src="Summarize.assets/image (7).png" alt="image (7)" width="50%" />
      
      
      - Quadratic Optimizer Implementation
      
    - 6 CONCLUSION AND DISCUSSION

      - QDNNs show a significant potential on learning tasks which highly depends on **extracted objects,** such as object detection, segmentation, and position recognition.

      - the recognition process will more focus on the important objects while ignoring the unimportant background






## DB







