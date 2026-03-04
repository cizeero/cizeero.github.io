# Website Management Skill

This skill helps manage the personal website at /home/zeero/Desktop/oss/website.

## Site Structure

All pages use a persistent sidebar layout (CSS grid: 250px sidebar + main content).

- `index.html` - Homepage (intro + blog list)
- `blog.html` - Blog index page
- `blog/` - Blog posts directory (use `../` relative paths for CSS/links)
  - `selfish.html` - Building Product for Selfish Reasons
  - `bpe.html` - Byte-Pair Encoding
  - `differentiation.html` - Differentiation
  - `recursive-language-models.html` - Recursive Language Models
  - `inquiry.html` - Inquiry
- `reading-list.html` - Reading list with papers and blogs
- `completed-reading.html` - Completed reading with topic-based blog collections
- `currently-focused.html` - Currently focused areas hub page
  - `ml-fundamentals.html` - Machine Learning Fundamentals
  - `system-design-agentic.html` - System Design for Agentic Systems
  - `rna-folding.html` - RNA Folding Solutions
- `style.css` - Dracula-themed styles with sidebar layout

## Theme

Uses Dracula color palette:
- Background: `#282a36`, Secondary: `#21222c`
- Text: `#f8f8f2`, Muted: `#6272a4`
- Accent/Purple: `#bd93f9`, Pink: `#ff79c6`, Cyan: `#8be9fd`
- Green: `#50fa7b`, Orange: `#ffb86c`, Yellow: `#f1fa8c`, Red: `#ff5555`

Blog posts have larger font (1.15rem), colored bold (orange), italic (yellow), headings (purple), links (cyan). Code blocks and syntax highlighting classes are ready.

## Common Tasks

### Adding a Blog Post
1. Create a new HTML file in `blog/` (e.g., `blog/my-post.html`)
2. Use `blog/inquiry.html` as a template - includes sidebar with `../` relative paths
3. Add a link to the new post in both `blog.html` and `index.html` in the `<ul class="links">` sections
4. Set `class="active"` on the Blog nav link in sidebar

### Adding to Reading List
Edit `reading-list.html` and add a new `<li>` entry in the `<ul class="links">` section:
```html
<li><a href="URL" target="_blank">Title - Author</a></li>
```

### Adding New Pages
1. Create a new HTML file following the sidebar layout pattern
2. For root-level pages: use `style.css` and direct nav links
3. For `blog/` pages: use `../style.css` and `../` prefixed nav links
4. Include sidebar with: Cizeero header, El Psy Congroo tagline, nav links, hamburger toggle script

### Deploying
The site is hosted via GitHub Pages (cizeero.github.io).

**IMPORTANT**: Always commit and push changes after any edit to keep the live site in sync.
