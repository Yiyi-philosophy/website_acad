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
Now I'm studying at School of Electronics & Information, HDU (Hangzhou Dianzi University). You can visit [My Blog](https://yiyi-philosophy.github.io/simplicity/) to know more about me.

I'm preparing for the **24 fall** applications of CS PhD.

#### And my latest GPA is 3.73/4.0(4.37/5.0) 5%.



<div class='paper-box'>
<div class="box">
  	<div class="left">
		<!-- <div class='paper-box-text' markdown="1"> -->
		## Research Interests:
		- MLsys
		- Distributed, Parallel, and Cluster Computing
		- HPC
		- Computer Architecture
		- Machine Learning
		- Computer Vision
		<!-- </div> -->
	</div>
  	<!-- <div class="middle">中间a</div> -->
  	<div class="right">
  		<!-- <div class='paper-box-text' markdown="1"> -->
		## Skills:
		- C, C++, Python, Matlab
		- OpenMP, MPI, CUDA
		- Linux
		- Verilog
  		<!-- </div> -->
  	</div>
</div>
</div>


# 🔥 Recent Task

*Oct. 2022 - (Now)*: Preparing for **ASC** (Asian Supercomputer Community)

<div class='paper-box'><div class='paper-box-image'><div>
	<img src='_pages/about.assets/performance analysis.png' alt="pa" width="100%">
	<br><br>
	<img src="_pages/about.assets/block-Z.png" alt="image10" width="100%" />
</div></div>

<div class='paper-box-text' markdown="1">
*July 2022 - Sept. 2022*: **DGEMM**: Double Precision General Matrix Multiplication [Report](https://yiyi-philosophy.github.io/yiran.ding/_pages/about.assets/Matrix%20Multiplication_v2.2.pdf)
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



<div class='paper-box'><div class='paper-box-image'><div>
	<img src="_pages/about.assets/image-20230109232006051.png" alt="image-20230109232006051" width="80%"/>
</div></div>

<div class='paper-box-text' markdown="1">
*Feb. 17-21 2022*: Mathematical Modeling: MCM/ICM 2022 [Problem E](https://mathmodels.org/Problems/2022/ICM-E/2022_ICM_Problem_E.pdf) [Our article](https://yiyi-philosophy.github.io/yiran.ding/_pages/about.assets/E-2224327.pdf)
- Led the project of "Forestry for Carbon Sequestration to Forest Management".
- Developed logistic equation based model to estimate the carbon sequestration of different trees species. (Successful Participant)
- Drawn 20 image in the article, using MATLAB and PPT.
- Utilized: Least Squares method, Monte Carlo method.
<img src="_pages/about.assets/image-20230109232046462.png" alt="image-20230109232046462" width="100%" />
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

- UC Berkeley CS267: Applications of Parallel Computers (Ongoing 17/26) [My note](https://yiyi-philosophy.github.io/simplicity/Note_CS267/)
- UC Berkeley AI-Sys: Machine Learning Systems (Ongoing 3/11) 
- MIT 6.s081: Operating System Engineering (Ongoing 11/23) 
- CMU 15-213: Intro to Computer Systems (CSAPP)
- THU: Data Structures
- Hung-yi Lee: Machine learning 2021 [My note](https://github.com/Yiyi-philosophy/LHY_ML)
- Andrew Ng: Machine learning  
- MIT 18.06: Linear Algebra

# 📰 Summarize for some Papers

## Sys

[Demystifying and Checking Silent Semantic Violations in Large Distributed Systems](Demystifying and Checking Silent Semantic Violations in Large Distributed Systems)

- A vexing problem occurs when a system is operational but **silently** breaks its semantics without **apparent anomalies**.
- The silent violated semantics have these features: Early existence, Locally,  Difficult to detect, Easy convert to crash failures by assertions, vulnerable to violations when maintaining.
- Oathkeeper, a tool that automatically infers semantic rules from p**ast failures** and enforces the rules at runtime to detect new failures. And Oathkeeper runs the tests on both the buggy version and patched version of the system, and takes a **template-driven** approach to automatically infer semantic rules from the two traces. Besides, Oathkeeper only incurs 1.27% throughput overhead.

---

## MLsys

[Monarch: Expressive Structured Matrices for Efficient and Accurate Training](https://yiyi-philosophy.github.io/simplicity/Monarch/)

- This paper propose a form of matrix **Monarch** which is **hardware-efficient** and **expressive**. 
  - **Efficient** -> Monarch matrix: $\mathbf{M}=\mathbf{P L P}^{\top} \mathbf{R} \sim 2n\sqrt{n}$  parameters
    - Although Monarch total FLOPs is $O(n\sqrt{n}) > O(n\log n)$ (butterfly matrix), it is easy to implement, **#2x** faster than dense multiply.
  - **Expressive** -> $$\mathcal{M} \mathcal{M}^*, (\mathcal{M} \mathcal{M}^*)^2$$ can represent most of structured matrice.
  - **Projection** problem -> ***Theorem 1:*** Dense Matrix $A=LR \sim O(n^{5/2})$ 
  - **Factorization** of $\mathcal{M} \mathcal{M}^*$ Matrices -> 
    - $\mathbf{M}=\mathbf{(P L_1 P^{\top})} \mathbf{R (P L_2 P^{\top})} \sim O(n^{5/2})$ 
- This method can be use in End-to-End training #**2x** , PDE solving and MRI reconstruction tasks **error #-40%**, Sparse-to-Dense (GPT-2 #**2x**; BERT pretraining #**23%>** Nvidia MLPerf) and Dense-to-Sparse BERT finetuning #**1.7x**.

[Slide : In Defense Of Smart Algorithms Over Hardware Acceleration For Large-Scale Deep Learning Systems](https://yiyi-philosophy.github.io/simplicity/Slide/)

- This paper propose SLIDE (Sub-Linear Deep learning Engine) that uniquely blends smart randomized algorithms, with **multi-core parallelism** and workload optimization.
- Using the classical backpropagation **message passing** type implementation rather than vector multiplication based and taking full advantage of sparsity.
- The extreme sparsity and randomness in gradient updates allow us to asynchronously parallelize the accumulation step of the gradient across different training data without leading to a considerable amount of overlapping updates.



[QUADRALIB: A PERFORMANT QUADRATIC NEURAL NETWORK LIBRARY FOR ARCHITECTURE OPTIMIZATION AND DESIGN EXPLORATION](https://yiyi-philosophy.github.io/simplicity/QuadraLib/)

- DNNs' success depends on many supporting libraries.
- QDNNs ($(WX)^2+b$) show better **non-linearity** and **learning capability**
- The benefits of QDNNs: Stronger non-linearity, Higher model efficiency.
- New Neuron Architecture Design
  - Extra Weights and Linear Term for Approximation Capability Improvement
  - Hadamard Product for Computation Complexity Optimization
  - Linear Term for Converge Performance Enhancement
  - First-order Neuron Combination for Implementation Feasibility Improvement

---

## ML 
[A Medium-Grained Algorithm for Distributed Sparse Tensor Factorization](https://yiyi-philosophy.github.io/simplicity/splatt/)

- Present a medium-grained decomposition that avoids complete factor replication and communication, while eliminating the need for expensive pre-processing steps

[Why Globally Re-shuffle? Revisiting Data Shuffling in Large Scale Deep Learning](https://yiyi-philosophy.github.io/simplicity/Local-Shuffle/)

- **Random access** to the input samples has been in fact identified as one of the major contributors to **poor I/O performance**.
- Demonstrate that in practice validation accuracy of **global shuffling** exchange $\approx$ partial distributed exchange when carefully tuning.
  - Each worker store **#0.03%** datasets.
  - **Training time**: Local shuffling **#5x** < Global shuffling

---

## RL







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
