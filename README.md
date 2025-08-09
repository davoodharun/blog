# Personal Blog

A minimal, modern personal blog built with Hugo featuring three main sections: writing, music, and visual work.

## Features

- **Minimal, Modern Design**: Clean and responsive design with dark mode support
- **Three Main Sections**:
  - **Writing**: Text-based articles and blog posts
  - **Music**: SoundCloud integration for music posts
  - **Visual Work**: Image galleries for VJ/VFX projects
- **GitHub Pages Deployment**: Automatic deployment via GitHub Actions
- **Mobile Responsive**: Optimized for all device sizes
- **Dark Mode**: Automatic dark mode support

## Local Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (version 0.80.0 or later)

### Setup

1. Clone this repository:
```bash
git clone https://github.com/yourusername/blog.git
cd blog
```

2. Start the Hugo development server:
```bash
hugo server -D
```

3. Open your browser and navigate to `http://localhost:1313`

## Configuration

### Site Settings

Edit `config.toml` to customize your site:

```toml
baseURL = "https://yourusername.github.io/blog/"
title = "Your Blog Title"
[params]
  author = "Your Name"
  description = "Your site description"
  github = "your-github-username"
  [params.social]
    soundcloud = "your-soundcloud-username"
```

### Adding Content

#### Writing Posts

Create new writing posts in `content/writing/`:

```bash
hugo new writing/my-new-post.md
```

#### Music Posts

Create music posts with SoundCloud integration:

```markdown
---
title: "Track Title"
date: 2024-01-15
soundcloud_url: "https://soundcloud.com/username/track-url"
---
```

#### Visual Work Posts

Create visual work posts with image galleries:

```markdown
---
title: "Project Title"
date: 2024-01-15
visual_gallery:
  - image: "/images/project-1.jpg"
    caption: "Project description"
---
```

## Deployment

### GitHub Pages

1. Push your changes to the `main` branch
2. GitHub Actions will automatically build and deploy to GitHub Pages
3. Your site will be available at `https://yourusername.github.io/blog/`

### Manual Deployment

```bash
hugo --minify
```

The built site will be in the `public/` directory.

## Customization

### Styling

Edit `static/css/main.css` to customize the design.

### Templates

Modify templates in the `layouts/` directory:
- `layouts/_default/baseof.html`: Base template
- `layouts/index.html`: Home page
- `layouts/_default/list.html`: List pages
- `layouts/_default/single.html`: Single post pages

### Adding New Sections

1. Create a new directory in `content/` (e.g., `content/photography/`)
2. Add a `_index.md` file with front matter
3. Update the menu in `config.toml`

## Structure

```
blog/
├── content/           # Content files
│   ├── writing/      # Writing posts
│   ├── music/        # Music posts
│   └── visual/       # Visual work posts
├── layouts/          # HTML templates
├── static/           # Static assets (CSS, JS, images)
├── config.toml       # Site configuration
└── .github/          # GitHub Actions workflow
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Feel free to submit issues and enhancement requests!




