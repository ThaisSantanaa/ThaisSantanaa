<div align="center">
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdWZ5eDVwYTdzaDUwNWhqN25yZ2x1a3NwYm1peWtocGFrZTliYnFxYSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/x5HlLDaLMZNVS/giphy.gif" width="500">

🌿✨ Thais Santana ✨🌿

💚 “Os sonhos ganham vida quando encontramos coragem para persegui-los.”

👩🏾‍💻 Desenvolvedora Java Full Stack em formação pela Generation Brasil
🎓 Bacharel em Administração de Empresas
📚 Estudando inglês e construindo minha carreira na tecnologia
🌎 Sonho em viajar o mundo, ajudar minha família e impactar vidas através da inovação

⸻

🐸 Tecnologias

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,mysql,git,github,html,css,vscode,eclipse" />
</p>

⸻

🌱 Atualmente                                                                              
🌷 Desenvolvendo projetos em Java Full Stack
📖 Aprimorando o inglês diariamente
🚀 Em busca da minha primeira oportunidade como desenvolvedora

⸻

<p align="center">
<img height="180em" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNTJiM3NyYnF4dnJvNjFyN3JqeDVndzk5MTYycHY2emhmbWlscjUyNSZlcD12MV9zdGlja2Vyc19zZWFyY2gmY3Q9cw/46yPfgO81ZalJSKu74/giphy.gif"/>
<img height="180em"


⸻

🌸 “O sucesso floresce quando dedicação e coragem caminham juntas.” 🌸

</div>f

name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"

  workflow_dispatch:

jobs:
  generate:
    permissions:
      contents: write

    runs-on: ubuntu-latest

    steps:
      - name: Generate snake
        uses: Platane/snk@v3
        with:
          github_user_name: ThaisSantanaa
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
