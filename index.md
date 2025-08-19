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



Powered by [SpoonOS](https://spoonai.io) <br>
Supported by [Berkeley Emerging Technology Association (BETA)](https://mp.weixin.qq.com/s/VBFUAU8MyaeIjd93FrWLhQ) <br>
Follow on [X (Twitter)](https://x.com/SpoonOS_ai)