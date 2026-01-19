# Website Management Skill

This skill helps manage the personal website at /home/zeero/Desktop/oss/website.

## Site Structure

- `index.html` - Main homepage
- `blog.html` - Blog index page
- `blog/` - Blog posts directory
  - `inquiry.html` - Inquiry post
- `reading-list.html` - Reading list with papers and blogs
- `completed-reading.html` - Completed reading with topic-based blog collections
- `currently-focused.html` - Currently focused areas hub page
  - `ml-fundamentals.html` - Machine Learning Fundamentals
  - `system-design-agentic.html` - System Design for Agentic Systems
  - `rna-folding.html` - RNA Folding Solutions
- `style.css` - Site styles

## Common Tasks

### Adding a Blog Post
1. Create a new HTML file in `blog/` (e.g., `blog/my-post.html`)
2. Use `blog/inquiry.html` as a template
3. Add a link to the new post in `blog.html` in the `<ul class="links">` section

### Adding to Reading List
To add a new item to the reading list, edit `reading-list.html` and add a new `<li>` entry in the `<ul class="links">` section:
```html
<li><a href="URL" target="_blank">Title - Author</a></li>
```

### Adding New Pages
1. Create a new HTML file following the structure of existing pages
2. Link it from `index.html` navigation or relevant sections
3. Include the shared `style.css`

### Deploying
The site can be pushed to GitHub for hosting via GitHub Pages.

**IMPORTANT**: Always commit and push changes after any edit to keep the live site in sync.
