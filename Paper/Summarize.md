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

    <img src="Paper/Summarize.assets/image (3).png" alt="image (3)" width="100%" />

      - **Initialization:**

      - **Sparse Feed-Forward Pass with Hash Table Sampling:**

        

    <img src="Paper/assets/Summarize.image (4).png" alt="image (4)" width="80%" />

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






## DB







