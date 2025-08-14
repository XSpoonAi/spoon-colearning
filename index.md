---
title: Home
layout: default
nav_order: 1
---

# AI Co-Learning


Large Language Models (LLMs) have profoundly reshaped the landscape of artificial intelligence. This course is designed to guide learners through the **core principles of LLMs and intelligent agents**, combining theoretical foundations with hands-on experience.

We will explore:
- The **architecture and capabilities** of large language models
- The **key features** needed to automate real-world tasks
- The **underlying framework** for building and deploying agent systems

In addition to foundational knowledge, we will delve into **practical applications**, including:
- Code generation
- Robotic control
- Web process automation

We will also examine the **limitations and risks** of current LLM agents — such as hallucination, misalignment, and brittleness — and discuss how future systems might address these challenges.


## Topics Covered

- Foundation of LLMs  
- LLM Inference & Reasoning          
- Agent Overview (Planning – Tool Use – Memory)       
- MCP (Modular Control Protocol) & A2A (Agent-to-Agent communication)
- Reinforcement Learning Foundations (MDPs, value functions, policy gradients)
- RL for Language Models: Tool use, exploration, and long-horizon reasoning
- RL in Practice: Code LLMs, experience data collection, and decentralized AI systems
- Alignment via RLHF (Reinforcement Learning from Human Feedback) 


## Lecture Guests

<div class="staff-grid">
{% assign featured_guests = site.staffers | where: "featured", true | sort: "index" %}
{% for staffer in featured_guests %}
  <div class="staff-card">
    <img src="{{ staffer.picture }}" alt="{{ staffer.name }}" />
    <p>
      <strong><a href="{{ staffer.external_url }}" target="_blank">{{ staffer.name }}</a></strong><br>
      {{ staffer.role }}<br>
      <em>{{ staffer.email }}</em>
    </p>
  </div>
{% endfor %}
</div>

## Schedule

<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Guest Lecture</th>
      <th>Supplemental Readings</th>
    </tr>
  </thead>
  <tbody>
<tr>
  <td>July 18th</td>
  <td>
    <strong>LLM Inference and Reasoning</strong><br>
    Zhou Zijian, NUS<br><br>

    <strong>Inference:</strong><br>
    <ul>
      <li>What are the inputs and outputs of an LLM model?</li>
      <li>Difference between pre-filling and auto-regressive decoding</li>
      <li>Auto-regressive decoding:
        <ul>
          <li>How are tokens sampled based on output</li>
          <li>What are top-k, top-p, temperature?</li>
          <li>How does the LLM know when to stop?</li>
        </ul>
      </li>
    </ul>

    <strong>Reasoning:</strong><br>
    <ul>
      <li>What is reasoning in its fundamental sense?</li>
      <li>Why reasoning is important for LLM?</li>
      <li>Two approaches of achieving reasoning:
        <ul>
          <li>Using a fine-tuned model</li>
          <li>Prompting</li>
        </ul>
      </li>
    </ul>

    <a href="/spoon-colearning/assets/slides/LLM_Inference_and_Reasoning.pdf" target="_blank">Slides</a> · 
    <a href="https://www.youtube.com/live/0ocJov63Zp4" target="_blank">Recording</a>
  </td>
  <td>
    <ul>
      <li><a href="https://arxiv.org/abs/2402.10200" target="_blank">Chain-of-Thought Reasoning Without Prompting</a></li>
      <li><a href="https://arxiv.org/abs/2309.03409" target="_blank">Large Language Models as Optimizers</a></li>
    </ul>
  </td>
</tr>


<tr>
  <td>July 23th</td>
  <td>
    <strong>Post-Training Reasoning Models</strong><br>
    Zhi Wang, UCSD<br><br>

    <strong>Key Topics:</strong><br>
    <ul>
      <li>Motivation for post-training: overcoming scaling limits of pre-training and enabling LLMs to "think"</li>
      <li>Introducing temporal reasoning via Chain-of-Thought (CoT) and Tree-of-Thought (ToT)</li>
      <li>Supervised Fine-Tuning (SFT) on reasoning data: objectives and benefits</li>
      <li>Reinforcement Learning with Verifiable Rewards (RLVR) and GRPO (Group Relative Policy Optimization)</li>
    </ul>

    <strong>Applications & Insights:</strong><br>
    <ul>
      <li>Practical design of reasoning-oriented pipelines for math and code tasks</li>
      <li>Techniques to enhance reasoning during inference without retraining</li>
      <li>Discussion on current limitations and future research directions in scalable reasoning for LLMs</li>
    </ul>

    <a href="/spoon-colearning/assets/slides/Post_Training_Reasoning_Models.pdf" target="_blank">Slides</a> · 
    <a href="https://www.youtube.com/watch?v=VWB5Y18eFso" target="_blank">Recording</a>
  </td>
  <td>
    <ul>
      <li><a href="https://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf" target="_blank">Introduction to Reinforcement Learning</a></li>
      <li><a href="https://courses.d2l.ai/berkeley-stat-157/index.html" target="_blank">Introduction to Deep Learning</a></li>
    </ul>
  </td>
</tr>


<tr>
  <td>August 8th</td>
  <td>
    <strong>Foundational Methods for Foundation Models for Scientific Machine Learning</strong><br>
    Michael Mahoney, UC Berkeley, Amazon <br><br>

    <strong>Key Points:</strong><br>
    <ul>
      <li>Pre-train & fine-tune paradigm for SciML, adapted from NLP/CV</li>
      <li>Scaling laws: model size, data size vs. fine-tuning performance</li>
      <li>Out-of-distribution transfer across physics parameters</li>
      <li>Multi-task pre-training across physics problems</li>
      <li>Failure modes at SciML–ML interface & mitigation strategies</li>
      <li>Deployment at scale using HPC environments like NERSC</li>
    </ul>

    <a href="/spoon-colearning/assets/slides/foundations7_apr25.pdf" target="_blank">Slides</a> · 
    <a href="https://www.youtube.com/watch?v=eKUKtz_BAK4" target="_blank">Recording</a>
  </td>
  <td>
    <ul>
      <li><a href="https://arxiv.org/abs/2506.13059" target="_blank">Multipole Attention for Efficient Long Context Reasoning</a></li>
      <li><a href="https://arxiv.org/abs/2507.10349" target="_blank">TAT: Temporal-Aligned Transformer for Multi-Horizon Peak Demand Forecasting</a></li>
      <li><a href="https://arxiv.org/abs/2501.06386" target="_blank">Using Pre-trained LLMs for Multivariate Time Series Forecasting</a></li>
    </ul>
  </td>
</tr>


<tr>
  <td>August 13th</td>
  <td>
    <strong>Learning from Experience AKA Reinforcement Learning (2024 Turing Award topic for research and business)</strong><br>
    Yuxi Li, University of Alberta, AI4All Institute <br><br>

    <strong>First principles:</strong><br>
    <ul>
      <li>Learning from experience</li>
      <li>Iterative improvement based on ground truth</li>
    </ul>

    <strong>Research:</strong><br>
    <ul>
      <li>Pursuing truth or following trend</li>
      <li>Autonomous, optimal and adaptive agents</li>
      <li>Simulation, integration of (world) model and data</li>
      <li>Explore alternative approaches w.r.t. data collection, architectures, and algorithms</li>
      <li>"Small" language models, modularity, generalist vs specialist</li>
    </ul>

    <strong>Business:</strong><br>
    <ul>
      <li>Value investment</li>
      <li>AI vs IT</li>
      <li>Code LLMs</li>
      <li>Experience data collection</li>
      <li>Decentralized AI aka AI + blockchain, in particular, for stablecoin</li>
    </ul>
    
    <a href="https://drive.google.com/file/d/1WVOBiwudUUiR7_pC9ILlcltJeAs--Faj/view?usp=share_link" target="_blank">Slides</a> · 
    <a href="https://www.youtube.com/watch?v=XmaPzLcNOco" target="_blank">Recording</a>
  </td>
  <td>
    <em>To be uploaded</em>
  </td>
</tr>

  </tbody>
</table>


Powered by [SpoonOS](https://spoonai.io) <br>
Supported by [Berkeley Emerging Technology Association (BETA)](https://mp.weixin.qq.com/s/VBFUAU8MyaeIjd93FrWLhQ) <br>
Follow on [X (Twitter)](https://x.com/SpoonOS_ai)