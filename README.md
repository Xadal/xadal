### Hi there 👋

Here are some ideas to get you started:

- 🔭 I’m currently working on mobile development
- 🌱 I’m currently learning React-Native and Swift
- 💬 Ask me about React native, Java and Swift
- 📫 How to reach me: abdullahadal8.aa@gmail.com
- [![Instagram Badge](https://img.shields.io/badge/-abdullahadall-C13584?style=flat-quare&labelColor=C13584&logo=instagram&logoColor=white&link=link)](link) 
- [![Github Badge](https://img.shields.io/badge/-XADAL-000?style=quare&labelColor=000&logo=Github&logoColor=white&link=link)](link) 

- ![Github stats 1](https://github-readme-stats.vercel.app/api?username=XADAL&show_icons=true&theme=gradient) 

-->


# Steps represent a sequence of tasks that will be executed as part of the job
steps:

# Checks repo under $GITHUB_WORKSHOP, so your job can access it
  - uses: actions/checkout@v2

# Generates the snake  
  - uses: Platane/snk@master
    id: snake-gif
    with:
      github_user_name: XADAL
      # these next 2 lines generate the files on a branch called "output". This keeps the main branch from cluttering up.
      gif_out_path: https://github.com/Xadal/Readme/blob/output/github-contribution-grid-snake.gif
      svg_out_path: https://github.com/Xadal/Readme/blob/output/github-contribution-grid-snake.svg

 # show the status of the build. Makes it easier for debugging (if there's any issues).
  - run: git status

  # Push the changes
  - name: Push changes
    uses: ad-m/github-push-action@master
    with:
      github_token: ${{ secrets.GITHUB_TOKEN }}
      branch: master
      force: true

  - uses: crazy-max/ghaction-github-pages@v2.1.3
    with:
      # the output branch we mentioned above
      target_branch: output
      build_dir: dist
    env:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
