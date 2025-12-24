# cheng2's Personal Learning Journal

A Jekyll-based personal blog documenting my journey in AI Safety, Large Language Models (LLMs), and related projects. This site uses the [Clean Blog Jekyll theme](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll) and is hosted on GitHub Pages.

**Live Site**: [https://ccstan99.github.io](https://ccstan99.github.io)

## About

This blog serves as my personal learning journal, covering topics including:
- AI Safety and Alignment Research
- Large Language Models (LLMs)
- Human-Computer Interaction (HCI)
- Community involvement and advocacy in tech

## Prerequisites

Before running this site locally, ensure you have the following installed:

- **Ruby** (version 2.7 or higher recommended)
- **RubyGems**
- **Bundler** - Install with: `gem install bundler`
- **Jekyll** - Will be installed via Bundler

### Check Your Ruby Installation

```bash
ruby -v
gem -v
```

If Ruby is not installed, visit [ruby-lang.org](https://www.ruby-lang.org/en/downloads/) for installation instructions.

## Local Development Setup

### 1. Clone the Repository

```bash
git clone https://github.com/ccstan99/ccstan99.github.io.git
cd ccstan99.github.io
```

### 2. Install Dependencies

Install all required gems using Bundler:

```bash
bundle install
```

This will install Jekyll and all plugins specified in the [Gemfile](Gemfile):
- jekyll
- jekyll-feed
- jekyll-paginate
- jekyll-sitemap
- webrick

### 3. Run the Development Server

Start the local Jekyll server:

```bash
bundle exec jekyll serve
```

Or with live reload and drafts enabled:

```bash
bundle exec jekyll serve --livereload --drafts
```

The site will be available at: **http://localhost:4000**

### 4. Browse the Site

Open your browser and navigate to [http://localhost:4000](http://localhost:4000) to view your local copy of the site.

## Project Structure

```
.
├── _config.yml           # Site configuration
├── _includes/            # Reusable HTML components
├── _layouts/             # Page templates
├── _posts/               # Blog posts (YYYY-MM-DD-title.md format)
├── _drafts/              # Draft posts (not published)
├── _sass/                # Sass stylesheets
├── _site/                # Generated site (do not edit)
├── assets/               # CSS, JS, and other assets
├── docs/                 # Documentation files
├── img/                  # Images
├── Gemfile               # Ruby dependencies
├── index.md              # Homepage
├── events.md             # Events page
└── resources.md          # Resources page
```

## Creating New Posts

Blog posts are stored in the `_posts/` directory. To create a new post:

1. Create a new file with the naming format: `YYYY-MM-DD-title.md`
2. Add front matter at the top:

```markdown
---
layout: post
title: "Your Post Title"
subtitle: "Optional subtitle"
date: YYYY-MM-DD HH:MM:SS
background: '/img/posts/your-image.jpg'
---

Your content here...
```

3. Save the file and Jekyll will automatically regenerate the site

### Working with Drafts

Place draft posts in the `_drafts/` directory without a date in the filename. View drafts locally with:

```bash
bundle exec jekyll serve --drafts
```

## Configuration

Site settings are managed in [_config.yml](_config.yml). Key configurations include:

- **Site metadata**: title, description, author
- **Social profiles**: GitHub, LinkedIn, Twitter
- **Google Analytics**: tracking ID
- **Pagination**: posts per page
- **Plugins**: feed, paginate, sitemap

After changing `_config.yml`, restart the Jekyll server for changes to take effect.

## Building for Production

To build the site for deployment:

```bash
bundle exec jekyll build
```

The production-ready site will be generated in the `_site/` directory.

## Deployment

This site is configured for GitHub Pages deployment. Any commits pushed to the `main` branch will automatically trigger a rebuild and deployment.

## Troubleshooting

### Port Already in Use

If port 4000 is already in use, specify a different port:

```bash
bundle exec jekyll serve --port 4001
```

### Bundle Install Issues

If you encounter dependency issues, try:

```bash
bundle update
bundle install
```

### Jekyll Not Found

Ensure you're using `bundle exec` before Jekyll commands to use the correct gem versions:

```bash
bundle exec jekyll serve
```

## Technologies Used

- **Jekyll**: Static site generator
- **Ruby**: Programming language
- **Bootstrap 4.6**: CSS framework
- **jQuery**: JavaScript library
- **Font Awesome**: Icon toolkit
- **Kramdown**: Markdown processor
- **Rouge**: Syntax highlighter

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Contact

- **Email**: ccstan99@gmail.com
- **GitHub**: [@ccstan99](https://github.com/ccstan99)
- **LinkedIn**: [cheng2-tan](https://www.linkedin.com/in/cheng2-tan)
- **Twitter**: [@cheng2_tan](https://twitter.com/cheng2_tan)

## Acknowledgments

Built with the [Clean Blog Jekyll theme](https://startbootstrap.com/themes/clean-blog-jekyll) by Start Bootstrap.
