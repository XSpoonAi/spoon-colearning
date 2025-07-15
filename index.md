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

 🔹 Foundation of LLMs  
 🔹 LLM Inference & Reasoning          
 🔹 Agent Overview (Planning – Tool Use – Memory)       
 🔹 MCP (Modular Control Protocol) & A2A (Agent-to-Agent communication)


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
    - What are the inputs and outputs of an LLM model?<br>
    - Difference between pre-filling and auto-regressive decoding<br>
    - Auto-regressive decoding:<br>
    &nbsp;&nbsp;&nbsp;&nbsp;- How are tokens sampled based on output<br>
    &nbsp;&nbsp;&nbsp;&nbsp;- What are top-k, top-p, temperature?<br>
    &nbsp;&nbsp;&nbsp;&nbsp;- How does the LLM know when to stop?<br><br>

    <strong>Reasoning:</strong><br>
    - What is reasoning in its fundamental sense?<br>
    - Why reasoning is important for LLM?<br>
    - Two approaches of achieving reasoning:<br>
    &nbsp;&nbsp;&nbsp;&nbsp;- Using a fine-tuned model<br>
    &nbsp;&nbsp;&nbsp;&nbsp;- Prompting
  </td>
  <td>
    - <a href="https://arxiv.org/abs/2402.10200" target="_blank">Chain-of-Thought Reasoning Without Prompting</a><br>
    - <a href="https://arxiv.org/abs/2309.03409" target="_blank">Large Language Models as Optimizers</a><br><br>
  </td>
</tr>
  </tbody>
</table>


Supported by [SpoonOS](https://spoonai.io)  
Follow on [X (Twitter)](https://x.com/SpoonOS_ai)