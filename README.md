# My Dev Site 🧑‍💻

A fast, clean, and responsive **developer portfolio** and **blog** built with [Hugo](https://gohugo.io/) and the beautiful [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. This site showcases my technical blog posts, open-source projects, and a detailed About Me section with links to my socials.

---

## 🚀 Features

- ⚡ Blazing fast static site generation using Hugo
- 🌓 Dark/light theme toggle
- 📚 Technical blog with syntax highlighting
- 💼 Project portfolio with structured layout
- 📱 Responsive design for all screen sizes
- 🧠 Custom CSS & social media icons
- 🖼️ Computer science-themed styling and imagery

---

## 🛠️ Project Structure

```bash
my-dev-site/
├── archetypes/             # Default archetypes for posts
├── assets/                 # Custom CSS or JS if needed
├── config.toml             # Site configuration
├── content/
│   ├── about.md            # About Me page
│   ├── blog/               # Blog posts
│   ├── projects/           # Project showcases
├── layouts/
│   ├── _default/
│   │   └── baseof.html     # Base HTML template
│   └── partials/
│       ├── header.html
│       └── toggle-theme.html
├── static/
│   ├── css/
│   │   └── styles.css      # Custom site styles
│   └── js/
│       └── toggle-theme.js # Theme toggle logic
├── themes/
│   └── PaperMod/           # PaperMod theme (as Git submodule)
└── README.md

📦 Getting Started
1. Clone the Repo

git clone <repo>

2. Install Hugo

Make sure you have Hugo Extended installed:

hugo version

3. Run Locally

hugo server -D

Visit http://localhost:1313 to view your site.
🎯 Deployment to GitHub Pages

You can deploy using:

hugo --minify

🧠 Credits

    Hugo

    PaperMod Theme

    Font Awesome for icons
