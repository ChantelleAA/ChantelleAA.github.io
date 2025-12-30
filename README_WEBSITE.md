# Chantelle Amoako-Atta's Personal Website

This is the source code for my personal website and blog, hosted at [chantelleaa.github.io](https://chantelleaa.github.io).

## 🌟 About

This website serves as my:
- **Portfolio** – Showcasing my AI/ML research projects and applications
- **Blog** – Technical tutorials and insights on Python, machine learning, and data science
- **Python Course** – 5 project-based lessons teaching Python fundamentals
- **Professional Resume** – My experience, education, and achievements

## 🛠 Technologies Used

- **Jekyll** – Static site generator
- **GitHub Pages** – Hosting platform
- **EasyBook Theme** – Base theme (heavily customized)
- **HTML/CSS/JavaScript** – Frontend
- **Markdown** – Content writing
- **Liquid** – Template language

## 📁 Repository Structure

```
.
├── _config.yml          # Site configuration
├── _includes/           # Reusable HTML components
├── _layouts/            # Page templates
├── _posts/              # Blog posts and tutorials
├── _sass/               # Sass stylesheets
├── assets/              # Images, fonts, and static files
│   └── images/
│       └── projects/    # Project screenshots and demos
├── css/                 # Compiled CSS
├── js/                  # JavaScript files
├── about.md             # About page
├── portfolio.md         # Portfolio page
├── projects.md          # Projects page
├── Resume.md            # Resume page
├── index.html           # Homepage
└── README.md            # This file
```

## 🚀 Running Locally

### Prerequisites

- Ruby 2.7 or higher
- Bundler
- Jekyll

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/ChantelleAA/ChantelleAA.github.io.git
   cd ChantelleAA.github.io
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser and navigate to `http://localhost:4000`

### Live Reload

For automatic browser refresh on file changes:
```bash
bundle exec jekyll serve --livereload
```

## 📝 Adding Content

### Creating a New Blog Post

1. Create a new file in `_posts/` with the format: `YYYY-MM-DD-post-title.md`
2. Add front matter:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD
   categories: [category1, category2]
   excerpt: "Brief description"
   comments: true
   ---
   ```
3. Write your content in Markdown below the front matter

### Adding a Python Course Lesson

Include the following additional front matter:
```yaml
categories: [python-course, python, tutorial, mini-project]
order: [1-5]
difficulty: "Beginner"
lesson_title: "Descriptive title"
concepts: "Key concepts covered"
duration: "20-25 min"
```

### Adding Project Images

Place images in `assets/images/projects/` and reference them as:
```markdown
![Alt text](/assets/images/projects/image-name.png)
```

## 🎨 Customization

### Modifying Site Configuration

Edit `_config.yml` to change:
- Site title and description
- Navigation links
- Social media profiles
- SEO settings

### Updating Styles

Styles are in `_sass/` and compiled into `css/main.css`. Modify existing `.scss` files or add new ones.

### Changing Layout

Edit files in `_layouts/` to modify page structure:
- `default.html` – Base template
- `post.html` – Blog post layout
- `page.html` – Static page layout

## 📊 Features

- ✅ Responsive design (mobile-friendly)
- ✅ Project-based Python course
- ✅ Comprehensive portfolio with project demos
- ✅ SEO optimized
- ✅ Google Analytics integration
- ✅ Disqus comments
- ✅ RSS feed
- ✅ Sitemap
- ✅ Social media sharing metadata
- ✅ Lesson navigation for Python course

## 🤝 Contributing

This is a personal website, but if you notice any issues or have suggestions:

1. Open an issue describing the problem or suggestion
2. For typos or minor fixes, feel free to submit a pull request
3. For major changes, please open an issue first

## 📧 Contact

- **Email:** chantelatta@gmail.com
- **LinkedIn:** [linkedin.com/in/chantelleaa](https://linkedin.com/in/chantelleaa)
- **GitHub:** [github.com/ChantelleAA](https://github.com/ChantelleAA)

## 📄 License

The content of this project is licensed under the [MIT License](LICENSE).

The EasyBook theme is also licensed under MIT by [laobubu](https://github.com/laobubu/jekyll-theme-EasyBook).

## 🙏 Acknowledgments

- EasyBook theme by laobubu
- GitHub Pages for hosting
- All the open-source projects that made this possible

---

*Built with ❤️ by Chantelle Amoako-Atta*
