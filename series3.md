---
title: Series Ⅲ
layout: default
nav_order: 5
---

# Series Ⅲ

<style>
  .staff-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* 固定每行两列 */
    gap: 20px; /* 卡片间距 */
    justify-items: center; /* 卡片居中 */
  }
  .staff-card{
    background:#fff;
    padding:12px;
    border-radius:12px;
    box-shadow:0 1px 2px rgba(0,0,0,.06);
  }
  .staff-card img{
    width:100%;
    height:160px;
    object-fit:cover;
    border-radius:8px;
    display:block;
  }
  .staff-card p{ margin:8px 0 0; }
  .staff-card a{ font-weight:600; }
</style>

<hr>

## Lecture Guests 

<div class="staff-grid">

  <div class="staff-card">
    <img src="{{ '/assets/images/shengyao-lu.jpg' | relative_url }}" alt="Shengyao Lu" />
    <p>
      <strong><a href="https://sluxsr.github.io/" target="_blank">Shengyao Lu</a></strong><br>
      Assistant Professor @ University of Victoria (UVic)<br>
      <em>shengyaolu@uvic.ca</em>
    </p>
  </div>

  <div class="staff-card">
    <img src="{{ '/assets/images/haipeng-chen.jpg' | relative_url }}" alt="Haipeng Chen" />
    <p>
      <strong><a href="https://www.linkedin.com/in/haipeng-chen-060b74b8/" target="_blank">Haipeng Chen</a></strong><br>
      Assistant Professor @ William & Mary, Graduate Program Director of Data Science Department<br>
      <em></em>
    </p>
  </div>

</div>

<hr>

## Schedule

<div style="overflow-x:auto; -webkit-overflow-scrolling: touch;">
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
  <td>November 4th</td>
  <td>
    <strong>Towards Graph-Language Systems</strong><br>
    Shengyao Lu, University of Victoria (UVic)<br><br>

    <strong>Key Topics:</strong><br>
    <ul>
      <li>Bridging graph neural networks and large language models</li>
      <li>Explainable AI for graph-structured knowledge</li>
      <li>Natural language interaction with structured knowledge</li>
      <li>Reasoning and decision-making in graph-language systems</li>
      <li>Applications and challenges in building interpretable AI systems</li>
    </ul>

    <a href="https://www.youtube.com/watch?v=KeZ2m51X5gQ" target="_blank">Recording</a>
  </td>
  <td>
    <em>To be updated</em>
  </td>
</tr>

<tr>
  <td>December 19th</td>
  <td>
    <strong>Turing Smith Machine: AI of All, by All, for All: Decentralized AI aka AI + Blockchain</strong><br>
    Yuxi Li, University of Alberta, AI4All Institute<br><br>

    <strong>First principles:</strong><br>
    <ul>
      <li>Learning from experience</li>
      <li>Iterative improvement based on ground truth</li>
      <li>Exploration, exploitation, and evolution</li>
    </ul>

    <strong>Research:</strong><br>
    <ul>
      <li>Turing Smith Machine: decentralized AI platform integrating AI and blockchain</li>
      <li>Modules for infrastructure, decision making, marketplace, and applications</li>
      <li>Cross-disciplinary approach: AI, computer science, economics, behavioral sciences</li>
      <li>Building the "AI flywheel" through learning algorithms and incentive mechanisms</li>
      <li>Applications: finance x AI x blockchain, software real world assets (RWAs), decentralized education and research</li>
    </ul>

    <a href="https://www.youtube.com/watch?v=kYwMp0zVtSw" target="_blank">Recording</a>
  </td>
  <td>
    <em>To be updated</em>
  </td>
</tr>

<tr>
  <td>January 14th</td>
  <td>
    <strong>Reinforcement Learning for Language Models</strong><br>
    Haipeng Chen, William & Mary<br><br>

    <strong>Key Topics:</strong><br>
    <ul>
      <li>RL for fine-tuning the LLM: Reinforcement Learning from Human Feedback (RLHF) to align model behavior with human intent</li>
      <li>Text generation as a sequential decision process: refining pretrained models into agents</li>
      <li>Optimizing for quality, helpfulness, and safety rather than just raw likelihood</li>
      <li>RL for training separate, auxiliary models: smaller-scale models that interact with or guide LLMs</li>
      <li>Adaptive feedback loops: learning to evaluate, interpret, or modulate LLM outputs</li>
      <li>Extending LLM performance in dynamic or multi-agent environments</li>
    </ul>

    <a href="https://www.youtube.com/watch?v=twn_dpjkjNA" target="_blank">Recording</a>
  </td>
  <td>
    <em>To be updated</em>
  </td>
</tr>

  </tbody>
</table>
</div>
