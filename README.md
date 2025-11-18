# Portfolio Website

A minimal, dark-themed personal portfolio website built with Next.js 14, TypeScript, and Tailwind CSS. Inspired by [adryd.com](https://adryd.com/), [prpl.wtf](https://prpl.wtf/), and [matdoes.dev](https://matdoes.dev/).

## ✨ Features

- 🎨 **Minimal Dark Theme** - Clean, modern design with fully customizable colors
- 📝 **Markdown Blog** - Write blog posts in markdown with frontmatter support
- 💼 **GitHub Projects Integration** - Automatically fetches and displays your GitHub repositories
- 🔍 **Advanced Search & Filters** - Search blog posts and filter by tags/year with pagination
- 📄 **Pagination** - Navigate through projects and blog posts with smart page controls
- 🎮 **Hidden Easter Eggs** - Multiple interactive easter eggs throughout the site
- ⚙️ **Fully Configurable** - Everything customizable via centralized `config/site.ts`
- 📱 **Fully Responsive** - Works beautifully on all devices
- 🌈 **Rainbow Mode** - Toggle colorful overlay with keyboard shortcut

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ 
- npm, yarn, or pnpm

### Installation

1. Clone the repository:
```bash
git clone https://github.com/59n/folio.git
cd folio
```

2. Install dependencies:
```bash
npm install
```

3. Configure your site:
Edit `config/site.ts` with your information:
- Site name, title, description
- Social links (GitHub, email, solo.to)
- Colors and theme
- GitHub username for projects

4. Run the development server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see your site.

## 📝 Blog Posts

Create markdown files in `content/posts/` to add blog posts. See [BLOG_README.md](./BLOG_README.md) for detailed instructions.

**Example post structure:**
```markdown
---
title: "My First Post"
date: "2024-01-15"
tags: ["javascript", "react", "tutorial"]
excerpt: "A short description of your post"
---

Your blog post content here! Supports full markdown.
```

## ⚙️ Configuration

All customization is done through `config/site.ts`. See [CONFIG_README.md](./CONFIG_README.md) for detailed configuration options.

### Quick Config Examples

**Change Site Name:**
```typescript
name: 'YourName',
title: 'Your Name',
header: {
  title: 'Your Name',
  subtitle: 'Your subtitle here',
}
```

**Change GitHub User for Projects:**
```typescript
projects: {
  githubUser: 'yourusername',
  perPage: 6, // Projects per page
  sortBy: 'updated', // 'updated' | 'created' | 'stars'
}
```

**Change Colors:**
```typescript
colors: {
  background: '#000000',
  foreground: '#ffffff',
  text: {
    primary: '#ffffff',
    secondary: '#9ca3af',
    muted: '#6b7280',
  },
  // ... more color options
}
```

**Toggle Footer:**
```typescript
footer: {
  enabled: true, // Set to false to hide footer
}
```

## 🎮 Easter Eggs

The site includes several hidden easter eggs:

- **Konami Code**: `↑ ↑ ↓ ↓ ← → ← → B A` - Classic gaming easter egg
- **Secret Words**: Type `secret`, `hello`, `magic`, `surprise`, or `hidden` anywhere
- **Title Click**: Click the site title 5 times quickly
- **Rainbow Mode**: Press `Ctrl/Cmd + Shift + R` to toggle colorful overlay

## 🏗️ Project Structure

```
.
├── app/
│   ├── blog/
│   │   ├── [slug]/      # Individual blog post pages
│   │   └── page.tsx     # Blog listing page
│   ├── projects/
│   │   └── page.tsx     # Projects page
│   ├── layout.tsx       # Root layout with metadata
│   ├── page.tsx         # Home page
│   └── globals.css      # Global styles and animations
├── components/
│   ├── Header.tsx       # Site header with social icons
│   ├── Footer.tsx       # Site footer
│   ├── ClickableTitle.tsx # Title component with easter egg
│   ├── BlogFilters.tsx  # Blog search and filter controls
│   └── EasterEgg.tsx   # Easter egg system
├── config/
│   └── site.ts          # Centralized site configuration
├── content/
│   └── posts/           # Blog post markdown files
├── lib/
│   └── posts.ts         # Blog post utilities and parsing
├── public/              # Static assets (favicons, etc.)
├── netlify.toml         # Netlify deployment configuration
└── package.json
```

## 🛠️ Technologies

- **Next.js 14** - React framework with App Router
- **TypeScript** - Type safety
- **Tailwind CSS** - Utility-first CSS framework
- **gray-matter** - Markdown frontmatter parsing
- **remark** - Markdown processing and HTML conversion

## 📦 Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm start        # Start production server
npm run lint     # Run ESLint
```

## 🚀 Deployment

### Netlify

This project is configured for Netlify deployment with `netlify.toml`. Simply:

1. Connect your GitHub repository to Netlify
2. Netlify will automatically detect Next.js and deploy
3. No additional configuration needed!

The build command and output directory are already configured in `netlify.toml`.

### Manual Build

```bash
npm run build
```

The build output will be in the `.next` directory.

### Environment Variables

No environment variables are required. All configuration is done through `config/site.ts`.

## 🎨 Customization Guide

### Colors & Theme
Edit `config/site.ts` → `colors` section

### Layout & Spacing
Edit `config/site.ts` → `layout` section

### Content
- **Header**: Edit `config/site.ts` → `header`
- **Navigation**: Edit `config/site.ts` → `navigation`
- **Footer**: Edit `config/site.ts` → `footer`

### Blog
- Add markdown files to `content/posts/`
- Configure in `config/site.ts` → `blog`

### Projects
- Configure GitHub user in `config/site.ts` → `projects`
- Customize display options (stars, language, dates)

## 📚 Documentation

- [BLOG_README.md](./BLOG_README.md) - Blog post creation guide
- [CONFIG_README.md](./CONFIG_README.md) - Complete configuration reference

## 🤝 Contributing

Feel free to fork and customize for your own portfolio! This is a personal portfolio template, so contributions should align with the minimal design philosophy.

## 📄 License

MIT

## 🙏 Credits

Design inspired by:
- [adryd.com](https://adryd.com/)
- [prpl.wtf](https://prpl.wtf/)
- [matdoes.dev](https://matdoes.dev/)

---

Built with ❤️ using Next.js and TypeScript
