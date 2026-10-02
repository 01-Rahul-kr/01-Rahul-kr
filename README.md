<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./light.svg">
  <img src="./dark.svg" alt="Vaibhav Khushalani — Creative Developer profile banner">
</picture>

</div>

<br>

## About

Hi, I'm **Vaibhav Khushalani** — a creative developer working across **AI workflows** and **cinematic web design**.

## Building

- 💻 **Cinematic Portfolio** — [github.com/VaibhavKhushalani/cinematic-portfolio](https://github.com/VaibhavKhushalani/cinematic-portfolio)
- 🌐 **Portfolio site** — [vaibhav-create.vercel.app](https://vaibhav-create.vercel.app)

## Content

I share AI workflows, cinematic websites, and creative development content on Instagram, Medium, and YouTube.

## Connect

| | |
|---|---|
| 🐙 GitHub | [github.com/VaibhavKhushalani](https://github.com/VaibhavKhushalani) |
| 💼 LinkedIn | [linkedin.com/in/vaibhav-khushalani-760217136](https://www.linkedin.com/in/vaibhav-khushalani-760217136) |
| ✍️ Medium | [medium.com/@vaibhavkhushalani](https://medium.com/@vaibhavkhushalani) |
| 📸 Instagram | [instagram.com/vaibhav.create](https://www.instagram.com/vaibhav.create) |
| ▶️ YouTube | [youtube.com/@vaibhav.create](https://www.youtube.com/@vaibhav.create) |

<br>

## 🐍 Contribution Snake

Animated snake that "eats" your contribution graph, with dark/light mode support and daily auto-update.

**1. Add the workflow** — create `.github/workflows/snake.yml` in your profile repo:

```yaml
name: generate snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch: {}
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**2. Embed it in your README:**

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/<your-username>/<your-username>/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/<your-username>/<your-username>/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/<your-username>/<your-username>/output/github-contribution-grid-snake.svg">
</picture>
```

Replace `<your-username>` with your GitHub username. After the workflow runs once, an `output` branch will hold the generated SVGs.

</div>
