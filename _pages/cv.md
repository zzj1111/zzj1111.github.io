---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

You can download a PDF version of my CV [here](../assets/ZijianZhang_CV.pdf).

Education
======
* **University of Minnesota**, MN, USA (2025.09 – 2030.06)
  * Full-funded PhD Student in Department of Electrical and Computer Engineering
  * Advised by Prof. Mingyi Hong
  * Direction: LLM agents, Post-training, Multi-agent system
  * GPA: 4/4

* **East China University of Science and Technology**, Shanghai, China (2021.09 – 2025.06)
  * B.S. in Computer Science
  * GPA: 88/100

Research Experience
======
* **PhD Student**, Mingyi Hong's Lab @ University of Minnesota (2025.08 – present)
  * Introduced StitchCUDA, a multi-agent workflow for End-to-End CUDA code generation and optimization, enhanced by Rubric-based Agentic RL. It achieves SOTA performance in End-to-End CUDA code generation, defeating GPT-5.2 by a 32B RL-based model, while avoiding reward-hacking and significantly reducing rollout overhead by decomposing atomic skills of Coding Agent. Submitted to ICML 2026.
  * Introduced CudaForge, a simple, effective and low-cost multi-agent workflow for CUDA kernel generation and optimization. It achieves SOTA performance in KernelBench Levels 1-3, while only costs $0.3 in API and 25 minutes in single RTX 6000. Submitted to ICML 2026.
  * Introduced InfantAgent-NEXT, which undertakes detailed modularization of agent workflows, tool selection, and tool execution, in favor of a modular architecture with a unified dialogue context. Accepted by NeurIPS 2025.
  * Advisor: Prof. Mingyi Hong

* **Research Assistant**, Huaxiu Yao's Lab @ University of North Carolina at Chapel Hill (2024.05 – 2025.01)
  * Introduced AnyPrefer, a new method to improve VLA model through DPO and iterative training framework, eventually the robots perform better in several tasks.
  * Introduced GRAPE, a Trajectory-wise DPO for VLA model posttraining, which enhances the safety, efficiency, and success rate of the VLA model.
  * Authored 1\*ICLR'25, 1\*ICRA'26.
  * Advisor: Prof. Huaxiu Yao

* **Research Assistant**, Machine Learning Group @ Microsoft Research Asia (2024.10 – 2025.04)
  * Worked on efficiently training LLM from mixing NLP datasets by dynamic sampling.
  * Worked on enhancing LLM's math reasoning ability by selecting high-quality CoT data via LLM-as-a-Judge.
  * Worked on analyzing dynamic parameters (such as loss) during model training to better control the training process.
  * Advisor: Prof. Zhong Li

* **Research Assistant**, InternLM2 Team @ Shanghai AI Lab (2023.11 – 2024.05)
  * Proposed an efficient data selection method to extract high-quality samples from the original SFT dataset of InternLM2. By fine-tuning InternLM2 on the top 10% of the highest-scoring examples, the model achieved superior performance compared to using the entire instruction dataset.
  * Solved the Identity Attack problem in InternLM. Constructed a special finetune dataset to enhance the cognitive ability of the model. Introduced a benchmark to evaluate the model's ability to resist Identity Attacks.
  * Participated in the research and development of InternLM/InternLM2, which are well-known open source LLMs.
  * Advisor: Prof. Yining Li

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Invited Talks
======
* **LLM for Kernel: Automated Agentic GPU Programming Framework — From Single Kernel to E2E Programs**  
  Amazon | Feb 2026
* **RL for VLA Models: Generalizing Robot Policy via Preference Alignment**  
  Department of Electronic Engineering, Tsinghua University (清华大学电子工程系) | Jan 2025
* **VLA RLHF: Generalizing Robot Policy via Preference Alignment**  
  3D Vision Workshop (3D视觉工坊) | Jan 2025

Academic Service
======
* Reviewer for ICML 2026
* Reviewer for ICLR 2026
* Reviewer for CVPR 2025
* Reviewer for NeurIPS Workshop 2024

Skills
======
* **Programming**: C/C++, Python, PyTorch, LaTeX, Git
* **Language**: Mandarin (native), English (TOEFL 100: R 27, L 24, S 22, W 27)
* **Engineering**: Agentic RL / RLVR on VeRL framework

Awards
======
* Department Fellowship — University of Minnesota
* Scholarship for Outstanding Students, First Prize — East China University of Science and Technology
* Outstanding Student Leaders — East China University of Science and Technology
* National Scholarship — Ministry of Education, China
* National Mathematics Competition for College Students, First Prize — Chinese Mathematical Society
* Suzhou Industrial Park Scholarship — Suzhou Government
