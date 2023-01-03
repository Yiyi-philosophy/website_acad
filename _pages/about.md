---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<span class='anchor' id='about-me'></span>
Now I'm studying at School of Electronics & Information, HDU (Hangzhou Dianzi University). 
I'm preparing for the **24 fall** applications of CS PhD.

#### And my latest GPA is 3.73/4.0(4.37/5.0) 5%.

## Research Interests:

- MLsys (Machine Learning System)
- HPC (High Performance Computing)
- Distributed, Parallel, and Cluster Computing
- Computer Architecture
- Machine Learning
- Computer Vision

## Skills:
- C, C++, Python, Matlab
- OpenMP, MPI, CUDA
- Linux
- Verilog

# 🔥 Recent Task

*Oct. 2022 - (Now)*: Preparing for **ASC** (Asian Supercomputer Community)

<div class='paper-box'><div class='paper-box-image'><div>
	<img src='_pages/about.assets/performance analysis.png' alt="pa" width="100%">
	<br><br>
	<img src="_pages/about.assets/block-Z.png" alt="image10" width="100%" />
</div></div>
  
<div class='paper-box-text' markdown="1">
*July. 2022 - Sept. 2022*: **DGEMM**: Double Precision General Matrix Multiplication
- Using 9 ways to achieve Matrix Multiplication, including methods of **Cache-oblivious** (Recursive) and **Z-Morton**.
- Testing Matrix size is from 16 to 2048, the best function is **82% faster** than standard function.
- Pseudo-code for recursive methods
	```C
	Define C = RMM (A, B, n)
	if (n==1) { 
	    C00 = A00 * B00 ; 
	} else{ 
		C00 = RMM (A00 , B00 , n/2) + RMM (A01 , B10 , n/2)
		C01 = RMM (A00 , B01 , n/2) + RMM (A01 , B11 , n/2)
		C10 = RMM (A10 , B00 , n/2) + RMM (A11 , B10 , n/2)
		C11 = RMM (A10 , B01 , n/2) + RMM (A11 , B11 , n/2) 
	} 
	return C
	```

</div></div>

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div>
  <div class="badge">SCI submitted in</div>
  <img src='_pages/about.assets/Figure01.jpg' alt="sym" width="100%"><img src='_pages/about.assets/Figure06.jpg' alt="sym" width="100%">
</div></div>
  
<div class='paper-box-text' markdown="1">
  
*Nov. 2021 - Aug. 2022*: Medical Image Processing
- Led and designed the project of automatically evaluating finger tapping videos of Parkinson’s disease patients. 
- Developed LSTM-FCN based model to classify patients. The result has 83.7% accuracy, which in dataset of this paper defeats the state-of-the-art results in literatures. 
- Utilized: Pose estimation (Mediapipe Hands), RIFE algorithm (Time Series Interpolation), LSTM, FCN.

<img src="_pages/about.assets/Figure10.jpg" alt="Figure10" width="100%" />
</div></div>


# 💻 Online Courses

- UC Berkeley CS267: Applications of Parallel Computers (Ongoing 17/26)
- UC Berkeley AI-Sys: Machine Learning Systems (Ongoing 3/11)
- CMU 15-213: Intro to Computer Systems (CSAPP),
- MIT 6.s081: Operating System Engineering
- THU: Data Structures
- Hung-yi Lee: Machine learning 2021
- Andrew Ng: Machine learning
- MIT 18.06: Linear Algebra

# 📰 Summarize for some Papers

## MLsys
[Slide : In Defense Of Smart Algorithms Over Hardware Acceleration For Large-Scale Deep Learning Systems](https://github.com/Yiyi-philosophy/yiran.ding/blob/main/Paper/Summarize.md#slide--in-defense-of-smart-algorithms-over-hardware-acceleration-for-large-scale-deep-learning-systems)
- This paper propose SLIDE (Sub-Linear Deep learning Engine) that uniquely blends smart randomized algorithms, with **multi-core parallelism** and workload optimization.
- Using the classical backpropagation **message passing** type implementation rather than vector multiplication based and taking full advantage of sparsity.
- The extreme sparsity and randomness in gradient updates allow us to asynchronously parallelize the accumulation step of the gradient across different training data without leading to a considerable amount of overlapping updates.

[QUADRALIB: A PERFORMANT QUADRATIC NEURAL NETWORK LIBRARY FOR ARCHITECTURE OPTIMIZATION AND DESIGN EXPLORATION](https://github.com/Yiyi-philosophy/yiran.ding/blob/main/Paper/Summarize.md#quadralib-a-performant-quadratic-neural-network-library-for-architecture-optimization-and-design-exploration)
- DNNs' success depends on many supporting libraries.
- QDNNs ($(WX)^2+b$) show better **non-linearity** and **learning capability**
- In this paper, author proposed a new QDNN neuron architecture design, and further developed QuadraLib. 
- The benefits of QDNNs: Stronger non-linearity, Higher model efficiency.
- New Neuron Architecture Design
  - Extra Weights and Linear Term for Approximation Capability Improvement
  - Hadamard Product for Computation Complexity Optimization
  - Linear Term for Converge Performance Enhancement
  - First-order Neuron Combination for Implementation Feasibility Improvement

# 📖 Educations

- *2021.09 - 2024.06 (now)*, School of Electronics & Information, HDU, Bachelor's degree. 
- *2020.09 - 2021.06*, School of Mathematics, Hangzhou Dianzi University(HDU), Bachelor's degree. 

# 🎖 Honors and Awards

- *2021.09* The First Prize Scholarship, Award rate 5%
- *2022.09* Scholarship of Provincial Government, Award rate 5%

# 🎺 Activities

- Vice Minister of Data Processing Department, Student association in the Faculty of Mathematics
	- Taught new students about programming skills such as Python, Matlab, etc.
	- Instructed them to solve NP-hard Graph Theory Problems with Heuristic Algorithms, and Time Series Forecasting Problems with LSTM Neural Networks




# 📈 Internships
