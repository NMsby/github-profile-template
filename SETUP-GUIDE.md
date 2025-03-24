# 🚀 GitHub Profile README Template Guide

Thank you for using my GitHub profile template! This guide will help you set up and customize your own awesome GitHub profile README.

## 📋 Step-by-Step Setup

### 1. Create Your Profile Repository

GitHub allows you to create a special repository with the same name as your username to display a README on your profile:

1. Create a new repository with your GitHub username as the repository name (e.g., `yourusername/yourusername`)
2. Initialize it with a README
3. Copy the template content into your README.md file

### 2. Customize Your Information

Replace the following information with your own:

- **Name and Introduction**: Change the header and About Me section
- **Social Links**: Update all LinkedIn, Portfolio, and Email links
- **Current Focus**: Update the "What I Do" bullet points
- **Technical Skills**: Modify languages and technologies based on your expertise
- **Featured Projects**: Replace with your own projects and descriptions
- **Contact Information**: Update with your own details

### 3. Set Up External Services

This template uses several external services that need configuration:

#### GitHub Stats and Streak

The GitHub stats cards are powered by these services:
```
https://github-readme-stats.vercel.app/
https://streak-stats.demolab.com/
```

Change all instances of `YOUR_USERNAME` to your GitHub username in these URLs:
```
https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical
https://streak-stats.demolab.com/?user=YOUR_USERNAME&theme=radical
https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=radical
```

#### Profile Views Counter

Replace `YOUR_USERNAME` with your username:
```
https://komarev.com/ghpvc/?username=YOUR_USERNAME&color=brightgreen
```

#### Typing SVG

Customize the text shown in the typing animation:
```
https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&width=435&lines=YOUR+TEXT+HERE;ANOTHER+LINE;YET+ANOTHER+LINE
```

#### Contribution Snake

For the contribution snake animation, you'll need to set up a GitHub Action:

1. Create a `.github/workflows` directory in your repository
2. Add a file named `snake.yml` with the following content:

```yaml
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: YOUR_USERNAME
          svg_out_path: dist/github-contribution-grid-snake.svg
          gif_out_path: dist/github-contribution-grid-snake.gif

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Remember to replace `YOUR_USERNAME` with your actual GitHub username.

#### Now Playing (Spotify)

This requires setting up a Vercel deployment. Follow these steps:

1. Fork the [Novatorem project](https://github.com/novatorem/novatorem)
2. Deploy it to Vercel
3. Configure with your Spotify account
4. Update the URL in the README to point to your deployment

#### Latest Activity Section

To auto-update your activity section:

1. Set up the [GitHub Activity Readme](https://github.com/jamesgeorge007/github-activity-readme) action
2. Make sure to keep the comment markers in place: 
   ```
   <!--START_SECTION:activity-->
   <!--END_SECTION:activity-->
   ```

### 4. Project Badges

For project stars badges, update the repository names and links:
```
https://img.shields.io/github/stars/YOUR_USERNAME/YOUR_REPO?style=social
```

### 5. Tech Stack Badges

Keep or replace tech stack badges based on your skills. Find more badges at [shields.io](https://shields.io/).

## ⚠️ Common Issues & Troubleshooting

- **Stats cards not loading**: Make sure your repository is public
- **Contribution snake not appearing**: Check if the GitHub Action ran successfully
- **Profile views counter stuck**: It may take time to update
- **Typing SVG not working**: Verify the URL is correctly formatted
- **Activity section not updating**: Ensure the GitHub Action is properly configured

## 📝 Attribution Requirements

When using this template, please include the following attribution line at the bottom of your README:

```
⭐️ Template inspired by [Nelson Masbayi](https://github.com/NMsby)
```

## 🆘 Need Help?

If you encounter any issues or have questions, feel free to:
- Open an issue in the template repository
- Contact me via [LinkedIn](https://www.linkedin.com/in/nmsby/) or [email](mailto:nmsby.dev@gmail.com)

Happy coding! 🚀

---

## License

This template is available under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
