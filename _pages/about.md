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

<div class='paper-box'><div class='paper-box-image'><div>
  <img src='_pages/about.assets/performance analysis.png' alt="pa" width="100%">
</div></div>
  
<div class='paper-box-text' markdown="1">
*July. 2022 - Sept. 2022*: **DGEMM**: Double Precision General Matrix Multiplication
- Using 9 ways to achieve Matrix Multiplication, including methods of **Cache-oblivious** (Recursive) and **Z-Morton**.
- Testing Matrix size is from 16 to 2048, the best function is **82% faster** than standard function.


<style type="text/css">
.tg  {border-collapse:collapse;border-color:#ccc;border-spacing:0;}
.tg td{background-color:#fff;border-color:#ccc;border-style:solid;border-width:1px;color:#333;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{background-color:#f0f0f0;border-color:#ccc;border-style:solid;border-width:1px;color:#333;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-4x00{background-color:#ffffff;border-color:#000000;color:#000000;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-8c31{background-color:#ffffff;border-color:#000000;color:#000000;text-align:left;vertical-align:middle}
.tg .tg-w22m{background-color:#ffffff;border-color:#000000;color:#000000;font-weight:bold;text-align:left;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">matrix size</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">Remark</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">16</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">32</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">64</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">128</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">256</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">512</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">1024</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">2048</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">Avg</span></th>
    <th class="tg-4x00"><span style="font-weight:var(--base-text-weight-semibold, 600)">Note</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-8c31">dgemm0</td>
    <td class="tg-8c31">Standard</td>
    <td class="tg-8c31">1.80E+04</td>
    <td class="tg-8c31">1.20E+05</td>
    <td class="tg-8c31">1.06E+06</td>
    <td class="tg-8c31">7.92E+06</td>
    <td class="tg-8c31">6.14E+07</td>
    <td class="tg-8c31">5.52E+08</td>
    <td class="tg-8c31">6.49E+09</td>
    <td class="tg-8c31">5.62E+10</td>
    <td class="tg-8c31"></td>
    <td class="tg-8c31">Running time</td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm1</td>
    <td class="tg-8c31">1 register</td>
    <td class="tg-8c31">0.5778</td>
    <td class="tg-8c31">0.5769</td>
    <td class="tg-8c31">0.4326</td>
    <td class="tg-8c31">0.4755</td>
    <td class="tg-8c31">0.5350</td>
    <td class="tg-8c31">0.6277</td>
    <td class="tg-8c31">0.6871</td>
    <td class="tg-8c31">0.8118</td>
    <td class="tg-8c31">0.5905</td>
    <td class="tg-8c31">Ratio to dgemm0</td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm2</td>
    <td class="tg-8c31">2*2 block +12*reg</td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.2667</span></td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.2843</span></td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.2072</span></td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.2061</span></td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.2052</span></td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.2138</span></td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.1865</span></td>
    <td class="tg-8c31">0.2159</td>
    <td class="tg-8c31">0.2232</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm4</td>
    <td class="tg-8c31">2*2 (B=2)</td>
    <td class="tg-8c31">0.4333</td>
    <td class="tg-8c31">0.4447</td>
    <td class="tg-8c31">0.3186</td>
    <td class="tg-8c31">0.3647</td>
    <td class="tg-8c31">0.3468</td>
    <td class="tg-8c31">0.3641</td>
    <td class="tg-8c31">0.2510</td>
    <td class="tg-8c31">0.2545</td>
    <td class="tg-8c31">0.3472</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm5_1</td>
    <td class="tg-8c31">matrix wise B=2</td>
    <td class="tg-8c31">1.4088</td>
    <td class="tg-8c31">1.6700</td>
    <td class="tg-8c31">1.5201</td>
    <td class="tg-8c31">1.4458</td>
    <td class="tg-8c31">1.3407</td>
    <td class="tg-8c31">1.2780</td>
    <td class="tg-8c31">1.2933</td>
    <td class="tg-8c31">1.2396</td>
    <td class="tg-8c31">1.3995</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm5</td>
    <td class="tg-8c31">matrix wise B=4</td>
    <td class="tg-8c31">1.7500</td>
    <td class="tg-8c31">1.6966</td>
    <td class="tg-8c31">1.2433</td>
    <td class="tg-8c31">1.4510</td>
    <td class="tg-8c31">1.3825</td>
    <td class="tg-8c31">1.3520</td>
    <td class="tg-8c31">0.9201</td>
    <td class="tg-8c31">0.8443</td>
    <td class="tg-8c31">1.3300</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm6</td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">Recursive</span></td>
    <td class="tg-8c31">1.2611</td>
    <td class="tg-8c31">1.4489</td>
    <td class="tg-8c31">0.9475</td>
    <td class="tg-8c31">1.1851</td>
    <td class="tg-8c31">1.0745</td>
    <td class="tg-8c31">1.2724</td>
    <td class="tg-8c31">0.7083</td>
    <td class="tg-8c31">0.6602</td>
    <td class="tg-8c31">1.0698</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm7</td>
    <td class="tg-8c31">Rec+2*2</td>
    <td class="tg-8c31">0.4111</td>
    <td class="tg-8c31">0.4713</td>
    <td class="tg-8c31">0.3027</td>
    <td class="tg-8c31">0.3341</td>
    <td class="tg-8c31">0.3486</td>
    <td class="tg-8c31">0.3711</td>
    <td class="tg-8c31">0.2455</td>
    <td class="tg-8c31">0.2276</td>
    <td class="tg-8c31">0.3390</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm8</td>
    <td class="tg-8c31">Rec+2*2+reg</td>
    <td class="tg-8c31">0.3222</td>
    <td class="tg-8c31">0.3791</td>
    <td class="tg-8c31">0.2524</td>
    <td class="tg-8c31">0.2611</td>
    <td class="tg-8c31">0.2675</td>
    <td class="tg-8c31">0.2885</td>
    <td class="tg-8c31">0.2012</td>
    <td class="tg-8c31">0.1832</td>
    <td class="tg-8c31">0.2694</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm9</td>
    <td class="tg-8c31">Rec+2*2+Z</td>
    <td class="tg-8c31">0.4667</td>
    <td class="tg-8c31">0.6500</td>
    <td class="tg-8c31">0.3016</td>
    <td class="tg-8c31">0.2914</td>
    <td class="tg-8c31">0.2884</td>
    <td class="tg-8c31">0.2667</td>
    <td class="tg-8c31">0.2086</td>
    <td class="tg-8c31">0.1747</td>
    <td class="tg-8c31">0.3310</td>
    <td class="tg-8c31"></td>
  </tr>
  <tr>
    <td class="tg-8c31">dgemm10</td>
    <td class="tg-8c31">Rec+2*2+reg+Z</td>
    <td class="tg-8c31">0.4722</td>
    <td class="tg-8c31">0.4821</td>
    <td class="tg-8c31">0.3019</td>
    <td class="tg-8c31">0.2962</td>
    <td class="tg-8c31">0.2929</td>
    <td class="tg-8c31">0.2819</td>
    <td class="tg-8c31">0.1992</td>
    <td class="tg-w22m"><span style="font-weight:var(--base-text-weight-semibold, 600)">0.1743</span></td>
    <td class="tg-8c31">0.3126</td>
    <td class="tg-8c31"></td>
  </tr>
</tbody>
</table>
  
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
