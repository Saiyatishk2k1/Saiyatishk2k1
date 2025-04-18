<div align="center">
 <img height="150" src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" />
</div>

###

<div align="center">
 <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="linkedin logo" />
 <img src="https://img.shields.io/static/v1?message=Youtube&logo=youtube&label=&color=FF0000&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="youtube logo" />
 <img src="https://img.shields.io/static/v1?message=Twitter&logo=twitter&label=&color=1DA1F2&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="twitter logo" />
</div>

###

<div align="center">
 <img src="https://visitor-badge.laobi.icu/badge?page_id=Saiyatishk2k1.Saiyatishk2k1&" />
</div>

###

<h1 align="center">hey there 👋</h1>

###

<h3 align="left">👩‍💻 About Me</h3>

###

<p align="left">I'm ... from ....<br><br>- 🔭 I’m working as ...<br>- 📚 I'm currently learning ...<br>- ⚡ In my free time I ...</p>

###

<h3 align="left">🛠 Language and tools</h3>

###

<div align="left">
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" height="40" alt="go logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-original.svg" height="40" alt="rust logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-plain-wordmark.svg" height="40" alt="ruby logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dot-net/dot-net-plain-wordmark.svg" height="40" alt="dot-net logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain-wordmark.svg" height="40" alt="firebase logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-line-wordmark.svg" height="40" alt="amazonwebservices logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/circleci/circleci-plain.svg" height="40" alt="circleci logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-plain.svg" height="40" alt="kubernetes logo" />
 <img width="12" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-plain-wordmark.svg" height="40" alt="docker logo" />
</div>

###

<h3 align="left">🔥 My Stats :</h3>

###

<div align="center">
 <img src="https://github-readme-stats.vercel.app/api?username=Saiyatishk2k1&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false&order=1" height="250" alt="stats graph" />
 <img src="https://github-profile-trophy.vercel.app?username=Saiyatishk2k1&theme=radical" height="150" alt="trophy graph" />
 <img src="https://github-readme-activity-graph.vercel.app/graph?username=Saiyatishk2k1&" height="150" alt="activity-graph graph" />
</div>

###

<img src="https://raw.githubusercontent.com/Saiyatishk2k1/Saiyatishk2k1/output/snake.svg" alt="Snake animation" />

###

try this code

and follow the next steps that i have mentioned in my youtube

😁
😅
😑



name: Generate snake animation

on:
 schedule: # execute every 12 hours
 - cron: "* */12 * * *"

 workflow_dispatch:

 push:
 branches:
 - main

jobs:
 generate:
 permissions:
 contents: write
 runs-on: ubuntu-latest
 timeout-minutes: 5

 steps:
 - name: generate snake.svg
 uses: Platane/snk/svg-only@v3
 with:
 github_user_name: ${{ github.repository_owner }}
 outputs: dist/snake.svg?palette=github-dark


 - name: push snake.svg to the output branch
 uses: crazy-max/ghaction-github-pages@v3.1.0
 with:
 target_branch: output
 build_dir: dist
 env:
 GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
