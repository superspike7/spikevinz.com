# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio and blog site for Spike Vinz Cruz (spikevinz.com). Built with Jekyll (Ruby static site generator), hosted on GitHub Pages.

## Development Commands

- **Dev server:** `jekyll serve` (localhost:4000, with live reload)
- **Build:** `jekyll build` (output to `_site/`)
- Ruby version: 3.1.0 (see `.tool-versions`)
- No Gemfile — uses system Jekyll installation
- No test or lint setup

## Architecture

**Layouts** (`_layouts/`): `default.html` is the base HTML shell; `post.html` extends it for blog posts (adds navbar, back link, title, date).

**Includes** (`_includes/`): Only `navbar.html` — a simple nav linking home.

**Content**: `index.html` is the home/landing page. `blog.html` lists all posts. Blog posts live in `_posts/` using standard Jekyll `YYYY-MM-DD-title.md` naming with YAML front matter (`layout`, `title`, `published`).

**Styling** (`_sass/`): Two SCSS partials — `base.scss` (layout, home page, variables) and `post.scss` (blog styles). Entry point is `assets/css/main.scss`. Design uses Roboto Mono font, black/white palette with red (#d30001) accent. Single breakpoint at 900px.

## Key Config

`_config.yml` holds site metadata: name, job title, email, social links (GitHub, LinkedIn, Twitter/X). Referenced in templates via `{{ site.* }}`.

`CNAME` sets the custom domain to `spikevinz.com`.

## Conventions

- Posts can be hidden with `published: false` in front matter
- Minimalist design — keep things simple and lightweight
- No JavaScript; pure HTML/CSS/Jekyll
