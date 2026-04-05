<h1 align="center">Oie, eu sou a Nahtaly! ୨ৎ</h1>

<p align="center">
  <img src="https://cdn.discordapp.com/attachments/1410243455073910835/1490209378018656377/Purple_and_Pink_Gradient_Modern_Programmer_Presentation_1.gif?ex=69d33922&is=69d1e7a2&hm=309178f94009ba7cca32b940ea7693f2a72366e24b9d6c16851b2c990a0ad5f5&animated=true" width="100%" />
</p>

---

## 
💻 Marketing + Tech  
🎮 Comunidade & Eventos  
🚀 Evolução constante  

---

## 🌐 Connect with me
<p align="center">
  <a href="https://www.instagram.com/nahxsnnr/"><img src="https://img.shields.io/badge/Instagram-ff69b4?style=for-the-badge&logo=instagram&logoColor=white"/></a>
  <a href="SEU-LINKEDIN"><img src="https://img.shields.io/badge/LinkedIn-6a0dad?style=for-the-badge&logo=linkedin&logoColor=white"/></a>

---

## ⚙️ Tech & Tools
<p align="center">
  <img src="https://skillicons.dev/icons?i=js,java,html,css,react,nodejs,git,github" />
</p>

---

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *" # atualiza todo dia
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: naahtaly
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
