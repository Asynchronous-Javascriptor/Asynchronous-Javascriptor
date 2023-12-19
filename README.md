![Asynchronous-Javascriptor GitHub Stats](https://github-readme-stats.vercel.app/api?username=Asynchronous-Javascriptor&show_icons=true&theme=dark)



![Html](https://img.shields.io/badge/html-orange)
![JavaScript](https://img.shields.io/badge/JavaScript-yellow)
![Python](https://img.shields.io/badge/Python-grey)

![Asynchronous-Javascriptor Activity Graph](https://activity-graph.herokuapp.com/graph?username=Asynchronous-Javascriptor&bg_color=000000&color=4fff67&line=4fff67&point=ffffff&area=true&hide_border=true)

name: Update README Stats
on:
  schedule:
    - cron: '0 * * * *'
jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repo
        uses: actions/checkout@v2
      - name: Update README
        run: |
          echo "![Your Name's GitHub Stats](https://github-readme-stats.vercel.app/api?username=Asynchronous-Javascriptor&show_icons=true&theme=dark)" > README.md
        commit_message: Update README
      - name: Commit and Push
        uses: stefanzweifel/git-auto-commit-action@v4
        with:
          commit_message: Update README

