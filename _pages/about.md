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

I'm preparing for the **25 fall** applications of CS PhD.

#### And my latest GPA is 3.8/4.0(90/100) 3%.

<div class='paper-box-2col'>
<div class='paper-box-2col-left' markdown="1">
## Research Interests:
I am broadly interested in the intersection between natural language processing (**NLP**) and **MLSys**, focusing on the **full potential** of LLMs and patterns of AI. I aim to achieve the **strongest** and most **complete** LLM capabilities, potentially leading to AGI or other advanced systems. Thus, I am particularly interested in the ***theoretical foundations** and **system architectures*, such as GPUs, required to support this goal.

</div>
<div class='paper-box-2col-right' markdown="1">
## Skills:
### Language
- Python(Pytorch, [Huggingface Transformers](https://huggingface.co/docs/transformers/index)), C/C++, Matlab 
- OpenMP, MPI, CUDA, 
- Shell, Git,  
- Verilog
</div>
</div>

## Knowledge Graph
<p class="aligncenter">
	<img src='images/about/1678872663298.png' alt="kg" width="80%">
</p>

# 📝 Publications 
<!-- longrope  -->
<div class='paper-box'><div class='paper-box-image'><div>
	<div class="badge">ICML Poster</div>
	<img src='_pages/about.assets/longrope-1.png' alt="sym" width="100%"><img src='_pages/about.assets/longrope-2.png' alt="sym" width="100%">
</div></div>
<div class='paper-box-text' markdown="1">
*Jul. 2023 - Jul. 2024*: LLM Sequence Extension: [LongRoPE](https://arxiv.org/pdf/2402.01694)
- Extends the context window of pre-trained LLMs(Llama, Mistral) to **2048k** tokens with up to only **1k fine-tuning steps** at 256k training lengths, maintaining original performance.
- Exploits **non-uniformities in positional interpolation** for better fine-tuning initialization, uses a progressive extension strategy, and **readjusts** LongRoPE to **recover short context** window performance.
- Supported fine-tuning of **Phi-3*(mini, small) to **128k contexts*: [Phi-3 Model]("https://huggingface.co/microsoft/Phi-3-mini-128k-instruct"), [Phi-3 Report]("https://arxiv.org/pdf/2404.14219").
  - Prepare and clean 128k-length datasets from different sources to finetuning, and methods to recover short context (4k) performance.

<img src='_pages/about.assets/longrope-step1.png' alt="sym" width="100%">
<img src='_pages/about.assets/longrope-step2.png' alt="sym" width="100%">
<img src='_pages/about.assets/longrope-step3.png' alt="sym" width="100%">
</div></div>


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

# 📈 Internships


# 🔥 Recent Task

*June 2023 - July 2024: LLM Sequence Extension
- Pioneered a groundbreaking **interpolation** technique for RoPE, significantly extending the sequence length of the Llama model to 32K with flash-attention, all without the need for fine-tuning.
- Successfully conducted evaluations on various downstream tasks, including **Passkey Retrieval** and **Quality** (reading comprehension).

*Mar. 2023 - (Now)*: Implement LLM(opt175b) inference in single GPU

<div class='paper-box'><div class='paper-box-image'><div>
	<img src="images/about/1686387116687.png" alt="image10" width="100%" />
</div></div>
<div class='paper-box-text' markdown="1">
*April 2023 - May 2023*: LLM inference in Edge Device: 
- Developed an **offline** large language model based on the **7B** Alpaca model to address privacy and security concerns with cloud deployment. 
- Implemented **Chinese Q&A** and dialogue functions, tested against similar models, and deployed on an 8GB edge device with 16Tops computing power in int8. 
- Expanded the Chinese vocabulary, **fine-tuned** the model with Chinese instruction data and utilized **int4** quantization to compress the model, significantly improving its understanding and execution of Chinese instructions.

</div></div>


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
- Using mathematical modeling to optimize forest management plans based on carbon sequestration, tree growth rates, and economic value.  
- The model aims to balance factors and maximize the forest's integrated value using carbon sequestration as the objective function and cutting rate as the decision variable. 
- Techniques include logistic regression, Monte Carlo simulation, and single-objective planning, and the model is applied to a specific forest to demonstrate effectiveness.
<img src="_pages/about.assets/image-20230109232046462.png" alt="image-20230109232046462" width="100%" />
</div></div>

<div class='paper-box'><div class='paper-box-image'><div>
	<img src="_pages/about.assets/MM_form.png" alt="MM_form" width="100%"/>
	<br><br>
	<img src="_pages/about.assets/MM_data.png" alt="MM_data" width="100%"/>
</div></div>
<div class='paper-box-text' markdown="1">
*Feb. 17-21 2022*: Optimizing Ride-Sharing Services: 
- Analyzes the problem of matching customers and suppliers in a large-scale ride-hailing service using greedy and simulated annealing algorithms. 
- Develop an online model that considers various factors, such as customer satisfaction, availability, and route optimization. 
- The models achieve high satisfaction rates(98%) and demonstrate strong stability and scalability.
<br>
<img align="middle" src="_pages/about.assets/MM_che.png" alt="MM_che" width="70%"/>
</div></div>


# 📖 Educations

- *2021.09 - 2024.06*, School of Electronics & Information, HDU, Bachelor's degree. 
- *2020.09 - 2021.06*, School of Mathematics, Hangzhou Dianzi University(HDU), Bachelor's degree. 

# 🎖 Honors and Awards

- *2021.09* The First Prize Scholarship, Award rate 5%
- *2022.09* Scholarship of Provincial Government, Award rate 5%

# 💻 Class

<div class='paper-box-2col'>
<div class='paper-box-2col-left' markdown="1">
## Online Courses
- UC Berkeley CS267: Applications of Parallel Computers (Ongoing 17/26) [My note](https://yiyi-philosophy.github.io/simplicity/Note_CS267/)
- UC Berkeley AI-Sys: Machine Learning Systems (Ongoing 3/11) 
- MIT 6.s081: Operating System Engineering (Ongoing 11/23) 
- CMU 15-213: Intro to Computer Systems (CSAPP)
- THU: Data Structures
- Hung-yi Lee: Machine learning 2021 [My note](https://github.com/Yiyi-philosophy/LHY_ML)
- Andrew Ng: Machine learning  
- MIT 18.06: Linear Algebra
</div>
<div class='paper-box-2col-right' markdown="1">
## College Courses
### Math and Science
- Higher Mathematics(Calculus) A1:		 98
- Higher Mathematics(Calculus) A2:		  96
- Analytic Geometry:		  90
- Probability Theory and Mathematical Statistics:		  91
- Complex Analysis:		  96
- Methods and Applications of Mathematical Modeling(A):		  90
- Mathematical Modeling Foundation(A):		 93
- Electromagnetic Field and Electromagnetic Wave:		 98
</div>
</div>

# 🎺 Activities

- Vice Minister of Data Processing Department, Student association in the Faculty of Mathematics
	- Taught new students about programming skills such as Python, Matlab, etc.
	- Instructed them to solve NP-hard Graph Theory Problems with Heuristic Algorithms, and Time Series Forecasting Problems with LSTM Neural Networks

<!-- -------------------- END of MAIN CONTENT -------------------- -->

# 📰 Summarize for some Papers

## Sys


<!-- <details> -->
<!-- <summary> -->

[Demystifying and Checking Silent Semantic Violations in Large Distributed Systems](https://yiyi-philosophy.github.io/simplicity/Oathkeeper/)
<!-- </summary> -->
        
- A vexing problem occurs when a system is operational but **silently** breaks its semantics without **apparent anomalies**.
- The silent violated semantics have these features: Early existence, Locally,  Difficult to detect, Easy convert to crash failures by assertions, vulnerable to violations when maintaining.
- Oathkeeper, a tool that automatically infers semantic rules from p**ast failures** and enforces the rules at runtime to detect new failures. And Oathkeeper runs the tests on both the buggy version and patched version of the system, and takes a **template-driven** approach to automatically infer semantic rules from the two traces. Besides, Oathkeeper only incurs 1.27% throughput overhead.

<!-- </details> -->
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


