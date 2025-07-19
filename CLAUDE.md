# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website project for Tuaregs AI (tuaregsai.com) that serves educational content about AI and development tools. The site is hosted on Firebase and provides access to learning resources through embedded Notion pages. The project also includes Eduardo Vieira's professional profile and background information.

## Architecture

The project follows a simple static website structure:

```
/
├── README.md              # Eduardo's professional profile and background
├── CLAUDE.md              # Claude Code guidance file
├── firebase.json          # Firebase hosting configuration
└── site/                  # Public website files
    ├── index.html         # Main landing page
    ├── guide/             # AI learning guide section
    │   └── index.html     # Embeds Notion page for AI guide
    ├── git-fundamentals/  # Git tutorial section
    │   └── index.html     # Embeds Notion page for Git guide
    └── vibe-coding-with-cursor/ # Cursor IDE tutorial
        └── index.html     # Embeds Notion page for Cursor guide
```

## Key Components

- **Landing Page**: Bootstrap-styled welcome page linking to educational content
- **Guide Pages**: HTML wrappers that embed external Notion pages using iframes
- **Firebase Hosting**: Configured with SPA-style routing (all routes serve index.html)
- **Analytics**: Google Analytics (G-Z8X4VNFSQ0) integrated across guide pages
- **Social Meta**: Open Graph and Twitter card meta tags for social sharing

## Content Strategy

Each guide section serves as an iframe wrapper for external Notion content:
- Main AI guide: Embedded from Notion workspace (efvi.notion.site)
- Git fundamentals: Version control tutorial content
- Cursor coding series: IDE tutorial and references

## Development Workflow

Since this is a static site with no build process:

1. **Local Development**: Serve files directly or use any static file server
2. **Content Updates**: Modify HTML files directly in the `site/` directory
3. **Deployment**: Use Firebase CLI: `firebase deploy`

## Firebase Configuration

- Site ID: `tuaregsai`
- Public directory: `site/`
- Routing: All requests route to `/index.html` for SPA behavior
- Ignored files: `firebase.json`, hidden files, and `node_modules`

## Styling

- Uses Bootstrap 5.3.0 from CDN
- Custom CSS embedded in HTML files
- Dark theme (#191919 background) consistent across pages
- Georgia serif font for typography
- Responsive design with mobile-first approach