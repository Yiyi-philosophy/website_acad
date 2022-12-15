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
And my latest GPA is 3.73/4.0(4.37/5.0) 5%.

## My Research Interests:

- MLsys (Machine Learning System)
- HPC (High Performance Computing)
- Computer Architecture
- Machine Learning
- Computer Vision

# 🔥 Recent Task

*Oct. 2022 - (Now)*: Preparing for **ASC** (Asian Supercomputer Community)

*July. 2022 - Sept. 2022*: **DGEMM**: Double Precision General Matrix Multiplication
- Using 9 ways to achieve Matrix Multiplication, including methods of **Cache-oblivious** (Recursive) and **Z-Morton**.
- Testing Matrix size is from 16 to 2048, the best function is **82% faster** than standard function.

| matrix size | Remark             | 16         | 32         | 64         | 128        | 256        | 512        | 1024       | 2048       | Avg    | Note            |
| ----------- | ------------------ | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ------ | --------------- |
| dgemm0      | Standard           | 1.80E+04   | 1.20E+05   | 1.06E+06   | 7.92E+06   | 6.14E+07   | 5.52E+08   | 6.49E+09   | 5.62E+10   |        | Running time    |
| dgemm1      | 1 register         | 0.5778     | 0.5769     | 0.4326     | 0.4755     | 0.5350     | 0.6277     | 0.6871     | 0.8118     | 0.5905 | Ratio to dgemm0 |
| dgemm2      | 2\*2 block +12\*reg | **0.2667** | **0.2843** | **0.2072** | **0.2061** | **0.2052** | **0.2138** | **0.1865** | 0.2159     | 0.2232 |                 |
| dgemm4      | 2\*2 (B=2)          | 0.4333     | 0.4447     | 0.3186     | 0.3647     | 0.3468     | 0.3641     | 0.2510     | 0.2545     | 0.3472 |                 |
| dgemm5_1    | matrix wise B=2    | 1.4088     | 1.6700     | 1.5201     | 1.4458     | 1.3407     | 1.2780     | 1.2933     | 1.2396     | 1.3995 |                 |
| dgemm5      | matrix wise B=4    | 1.7500     | 1.6966     | 1.2433     | 1.4510     | 1.3825     | 1.3520     | 0.9201     | 0.8443     | 1.3300 |                 |
| dgemm6      | **Recursive**      | 1.2611     | 1.4489     | 0.9475     | 1.1851     | 1.0745     | 1.2724     | 0.7083     | 0.6602     | 1.0698 |                 |
| dgemm7      | Rec+2\*2            | 0.4111     | 0.4713     | 0.3027     | 0.3341     | 0.3486     | 0.3711     | 0.2455     | 0.2276     | 0.3390 |                 |
| dgemm8      | Rec+2\*2+reg        | 0.3222     | 0.3791     | 0.2524     | 0.2611     | 0.2675     | 0.2885     | 0.2012     | 0.1832     | 0.2694 |                 |
| dgemm9      | Rec+2\*2+Z          | 0.4667     | 0.6500     | 0.3016     | 0.2914     | 0.2884     | 0.2667     | 0.2086     | 0.1747     | 0.3310 |                 |
| dgemm10     | Rec+2\*2+reg+Z      | 0.4722     | 0.4821     | 0.3019     | 0.2962     | 0.2929     | 0.2819     | 0.1992     | **0.1743** | 0.3126 |                 |


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

# 🎖 Honors and Awards

- *2021.09* The First Prize Scholarship, Award rate 5%
- *2022.9* Scholarship of Provincial Government, Award rate 5%

# 📖 Educations

- *2021.09 - 2024.06 (now)*, School of Electronics & Information, HDU, Bachelor's degree. 
- *2020.09 - 2021.06*, School of Mathematics, Hangzhou Dianzi University(HDU), Bachelor's degree. 


# 💻 Online Courses

- UC Berkeley CS267: Applications of Parallel Computers (Ongoing 17/26)
- UC Berkeley AI-Sys: Machine Learning Systems (Ongoing 3/11)
- CMU 15-213: Intro to Computer Systems (CSAPP),
- MIT 6.s081: Operating System Engineering
- THU: Data Structures
- Hung-yi Lee: Machine learning 2021
- Andrew Ng: Machine learning
- MIT 18.06: Linear Algebra



# 📈 Internships
