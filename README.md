# Spoon CoLearning 前端维护文档

本项目是基于 **Jekyll + Just the Docs** 的静态站点，用于维护 Spoon CoLearning 课程主页、讲者列表与各期系列日程页面。

线上地址：<https://xspoonai.github.io/spoon-colearning/>

---

## 1. 技术栈与运行方式

- 静态站点生成器：`jekyll`（`Gemfile` 当前为 `~> 4.4.1`）
- 主题：`just-the-docs`（`Gemfile` 固定 `0.10.1`）
- 部署方式：GitHub Pages（`main` 分支推送后自动构建与发布）
- 基础路径：`_config.yml` 中 `baseurl: "/spoon-colearning"`

本地预览（建议）：

```bash
bundle install
bundle exec jekyll serve
```

本地访问：

- `http://127.0.0.1:4000/spoon-colearning/`

---

## 2. 项目结构与文件关系

### 2.1 关键目录

- `_config.yml`：站点总配置（标题、主题、`baseurl`、集合 collections、默认布局等）
- `index.md`：首页（Home）
- `guests.md`：Lecture Guests 页面（自动读取 `_staffers` 集合）
- `series1.md` / `series2.md` / `series3.md`：三期页面（讲者区 + Schedule 表格）
- `_staffers/*.md`：讲者数据源（Front Matter）
- `assets/images/`：讲者头像等静态图片
- `_sass/custom/custom.scss`：全局自定义样式（影响 guests 等页面）
- `.github/workflows/pages.yml` / `deploy.yml`：自动构建与部署工作流

### 2.2 页面与数据流关系

1. 侧边导航来源于各页面 Front Matter：
   - `title` 决定显示名称
   - `nav_order` 决定顺序（`index=1`，`guests=2`，`series1=3`，`series2=4`，`series3=5`）
2. `guests.md` 使用 Liquid 遍历：
   - `{% assign all_guests = site.staffers | sort: "index" %}`
   - 因此讲者展示顺序由 `_staffers/*.md` 中 `index` 控制
3. `series*.md` 当前是“手写内容页”：
   - 讲者卡片、表格、链接直接写在页面中
   - 与 `_staffers` 没有自动绑定关系（两边都可能需要同步修改）

---

## 3. 讲者数据规范（`_staffers`）

每位讲者一个文件，例如：`_staffers/michael-mahoney.md`

建议字段：

```yaml
---
name: Michael Mahoney
role: Professor in University of California Berkeley, Amazon Scholar
index: 1
picture: assets/images/michael-mahoney.jpg
email: mmahoney@stat.berkeley.edu
external_url: https://www.stat.berkeley.edu/~mmahoney/
featured: true
layout: default
---
```

说明：

- `index`：数字越小排序越靠前
- `picture`：建议使用 `assets/images/xxx.jpg`（与 `guests.md` 渲染方式一致）
- `email`：可留空，但前端会渲染 `<em></em>`，如需更优显示可后续优化模板
- `layout`：当前项目默认是 `default`，可显式保留

---

## 4. 常见维护任务

### 4.1 新增讲者（Guests 页面）

1. 将头像放到 `assets/images/`
2. 新建 `_staffers/<slug>.md`，按上述字段填写
3. 设置合理 `index`（避免与已有讲者冲突）
4. 本地预览确认 `Lecture Guests` 页面显示正常

### 4.2 更新某期 Series 页面日程

修改目标文件：`series1.md`、`series2.md` 或 `series3.md`

- 在 `## Schedule` 的 `<table>` 内增删 `<tr>`
- 讲座信息在第 2 列（标题/讲者/要点/Slides/Recording）
- 补充阅读在第 3 列（可用 `<em>To be updated</em>` 占位）
- 链接统一加 `target="_blank"`

### 4.3 新增一个系列页面（例如 Series IV）

1. 新建 `series4.md`
2. Front Matter 设定：
   - `title: Series Ⅳ`
   - `nav_order: 6`（按现有顺序递增）
3. 复制现有 `series*.md` 的结构后改内容
4. 确认侧边栏顺序、移动端展示与链接可用性

### 4.4 调整样式

- 全局样式优先放 `_sass/custom/custom.scss`
- 当前 `series1/2/3.md` 内含页面级 `<style>`，会覆盖部分全局规则
- 若要统一三期样式，建议将重复 CSS 抽到 `_sass/custom/custom.scss`，并从页面内删除重复块

---

## 5. 部署与 CI

当前仓库存在两个 workflow：

- `.github/workflows/pages.yml`
- `.github/workflows/deploy.yml`

两者都在 `push main` 时执行“构建 + 部署”，功能存在重叠。  
维护建议：

- 保留一个主工作流，另一个停用，避免重复部署与排障复杂度上升
- 构建命令以 `bundle exec jekyll build` 为准
- 确保仓库 Settings 中 Pages 来源与 Actions 配置一致

---

## 6. 维护注意事项（高频踩坑）

1. **`baseurl` 问题最常见**  
   项目部署在子路径 `/spoon-colearning`，站内静态资源和内部链接应尽量使用：
   - `{{ '/assets/xxx' | relative_url }}`

2. **`guests.md` 与 `series*.md` 数据不是同一来源**  
   - `_staffers` 只驱动 `Lecture Guests`
   - `Series` 页面是手工维护，新增讲者时可能需要改两处

3. **图片命名与路径要稳定**  
   - 推荐小写英文与连字符，如 `haipeng-chen.jpg`
   - 文件名修改后要同步更新引用，避免线上 404

4. **`index/nav_order` 冲突会导致排序异常**  
   - `_staffers` 内 `index` 保持唯一
   - 顶层页面 `nav_order` 保持唯一且连续

5. **中英文符号统一**  
   页面同时有英文内容与中文注释，维护时注意全角/半角、特殊字符（如 `Ⅰ Ⅱ Ⅲ`）一致性。

---

## 7. 发布前检查清单

- `bundle exec jekyll build` 能通过
- 首页、Guests、Series I/II/III 页面可访问
- 新增/修改图片加载正常
- Slides/Recording/Reading 外链可打开
- 移动端下表格可横向滚动（不截断）
- Push 到 `main` 后 GitHub Actions 通过，Pages 页面更新成功

---

## 8. 后续可优化项（非必须）

- 将 `series1/2/3.md` 重复的讲者卡片样式抽离为全局 SCSS
- 将 Series 页面讲者信息改为复用 `_staffers` 数据，降低重复维护成本
- 增加一个数据层（例如 `_data/series.yml`）统一驱动 schedule 表格
- 增加链接校验（CI）防止外链失效
