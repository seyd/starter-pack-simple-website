# Starter Pack - Simple website with AI

## Overview

This is a **starter pack for simple websites using AI agent to do the work**, designed for individual makers who need a basic web presence without complex technical requirements. The focus is on **static content** with minimal dynamic functionality.

## Target Use Cases

- Personal portfolios
- Small business websites
- Event pages
- Simple landing pages
- Informational websites
- and similar...

## Features

### Core Functionality

- **Static content** - Perfect for informational websites
- **Responsive design** - Works on desktop and mobile devices
- **Optional multilingual support** - Can be configured for multiple languages
- **Basic dynamic elements**: - Contact forms, Newsletter sign-up functionality, etc.

### What's NOT Included

- No Content Management System (CMS)
- No user registration or authentication
- No payment processing
- No advanced dynamic features

## Target User

This starter pack is designed for **individual makers** who:

- Often lack technical background
- Use Cursor IDE with pre-setup GIT project starter pack
- Want to achieve results through chat-based development
- Need a simple, straightforward website solution

## Development Approach

The project is structured to guide users through a **chat-driven development process**:

1. Pre-configured GIT repository
2. Cursor IDE integration
3. Chat-based guidance for customization
4. Automated deployment setup

## Technology Stack

## Must:

- **IDE powered by AI**: Cursor

## Core Tech Stack

Essential components that form the foundation of every project:

- **Frontend**: Astro 4 (static site generator), HTML, CSS, JavaScript
- **Backend**: Astro Actions (server-only logic)
- **Styling**: Global CSS (common styles + reusables e.g. .btn-primary) + Tailwind CSS
- **Responsive**: Mobile-first design approach (Tailwind CSS)
- **UI Components**: React islands
- **Analytics**: Cloudflare Web Analytics
- **SEO**: Astro SEO integration + Sitemap
- **Hosting**: Cloudflare Pages

## Optional Tech Stack

Additional features you can add based on your project needs:

- **Forms**: Cloudflare Pages Functions + Turnstile
- **Email**: Resend (EU region)
- **Multilang**: File-based routing per locale (`/sk/`, `/en/`, etc.)
- **Storage**: Workers KV (key-value), Neon (Postgres)
- **Cookie Consent**: Zaraz Consent Manager

## The new approach with the AI

This project takes an "AI-first" approach to website creation.

A traditional **CMS is not needed** because content creation is handled through AI agents. Posts can be stored in a local JSON file within the project's source code.

Similarly, there's **no need for a user management system** (even for multi-author capabilities) since all authors have access to the project's Git repository. Authors can manage site content through the AI agent, which can attribute content to specific authors as needed.

The **automatic deployment** via Git push functions like a CMS but without the web interface. Content management is done through the Cursor Editor or even mobile app for managing Background Workers.

## Getting Started

Users should begin with the pre-configured starter pack and use the chat interface to:

1. Press `Ctrl + L` to open a chat window
2. Write "**Let's start!**" or "**What's next?**" if you have already started
3. And submit the message (Send button)
4. Then follow the instructions...

This approach eliminates the need for deep technical knowledge while providing a solid foundation for a professional website.
