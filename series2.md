---
title: Series Ⅱ
layout: default
nav_order: 4
---

# Series Ⅱ

<style>
  /* 与 Series Ⅰ 保持一致：两列卡片 + 统一图高 */
  .staff-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* 每行两个 */
    gap: 20px;
    justify-items: center;
    margin-bottom: 1rem;
  }
  .staff-card{
    background:#fff;
    padding:12px;
    border-radius:12px;
    box-shadow:0 1px 2px rgba(0,0,0,.06);
    width: 100%;
    max-width: 420px;
  }
  .staff-card img{
    width:100%;
    height:160px;         /* 统一高度避免被拉伸 */
    object-fit:cover;     /* 居中裁剪 */
    border-radius:8px;
    display:block;
  }
  .staff-card p{ margin:8px 0 0; text-align:center; }
  .staff-card a{ font-weight:600; }
  /* 没有邮箱时不占行 */
  .staff-card em:empty { display:none; }

  @media (max-width: 768px){
    .staff-grid { grid-template-columns: 1fr; } /* 小屏单列 */
  }
</style>

<hr>

## Lecture Guests

<div class="staff-grid">

  <div class="staff-card">
    <img src="{{ '/assets/images/sabina-yudi-nong.jpg' | relative_url }}" alt="Sabina (Yudi) Nong" />
    <p>
      <strong><a href="https://www.linkedin.com/in/sabinanong/" target="_blank">Sabina (Yudi) Nong</a></strong><br>
      Master of International Policy @ Stanford FSI<br>
      <em></em>
    </p>
  </div>

  <div class="staff-card">
    <img src="{{ '/assets/images/kumar-shridhar.jpg' | relative_url }}" alt="Kumar Shridhar" />
    <p>
      <strong><a href="https://www.linkedin.com/in/kumar-shridhar-ml/" target="_blank">Kumar Shridhar</a></strong><br>
      PhD @ ETH Zürich in Machine Learning<br>
      <em>shridhar.stark@gmail.com</em>
    </p>
  </div>

  <div class="staff-card">
    <img src="{{ '/assets/images/yuan-tian.jpg' | relative_url }}" alt="Yuan Tian" />
    <p>
      <strong><a href="https://www.linkedin.com/in/yuan-tian-3622a0172/" target="_blank">Yuan Tian</a></strong><br>
      Postdoc @ ETH Zurich<br>
      <em></em>
    </p>
  </div>

  <div class="staff-card">
    <img src="{{ '/assets/images/bang-liu.jpg' | relative_url }}" alt="Bang Liu" />
    <p>
      <strong><a href="https://www-labs.iro.umontreal.ca/~liubang/index.html" target="_blank">Bang Liu</a></strong><br>
      Associate Professor @ University of Montreal (UdeM)<br>
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
      <td>August 29th</td>
      <td>
        <strong>Governance: LLM + AI Agents</strong><br>
        Sabina (Yudi) Nong, Stanford<br><br>

        <strong>Key Points:</strong><br>
        <ul>
          <li>AI Governance & its Stakes</li>
          <li>Why AI Agents Require a Distinct Governance Lens (Procedural vs. Predictive)</li>
          <li>Developer Governance</li>
          <li>Regulatory Governance</li>
          <li>What does a good governance structure look like?</li>
        </ul>

        <a href="https://docs.google.com/presentation/d/145F-UnXUBswnz03WvZkliK7eLiLyhGY0bTrDJo8VUAk/mobilepresent?slide=id.g376427fc988_0_361" target="_blank">Slides (Website)</a> ·
        <em>Recording (To be uploaded)</em>
      </td>
      <td>
        <em>Supplemental Readings (To be updated)</em>
      </td>
    </tr>

  </tbody>
</table>
</div>
