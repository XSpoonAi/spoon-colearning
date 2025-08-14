# Spoon CoLearning

Welcome to the official website of **Spoon CoLearning**, a collaborative lecture series on cutting-edge research in Large Language Models (LLMs) and intelligent agents.

This site serves as the central hub for our course schedule, guest lectures, supplemental readings, and workshop announcements.

##  Live Site

> The site is hosted via GitHub Pages:  
> [https://xspoonai.github.io/spoon-colearning/](https://xspoonai.github.io/spoon-colearning/)
> 
##  Highlights

- **Weekly Guest Lectures** by researchers from leading universities and companies.
- **Lecture Schedule** with detailed topics, slides, recordings, and readings.
- **Community Engagement** through live Q&A and prize draws during events.

# 本地调试检查：bundle exec jekyll serve

# 1. 查看有哪些修改
git status

# 2. 添加修改内容（可以一次性添加全部）
git add .

# 3. 提交修改，-m 后面写提交信息
git commit -m "lec 1.2"

# 4. 推送到 GitHub（假设主分支是 main）
git push origin main
（如果github有更新，先合并远程版本：git pull origin main --rebase）

# 5. 回退至上一个版本
git fetch origin
git reset --hard HEAD^ 
git push origin main --force
