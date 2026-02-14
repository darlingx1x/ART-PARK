# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ART PARK is a single-file business proposal and system specification document (`artpark.html`) for a GovTech platform targeting Uzbekistan's creative industry residencies. The document is written in Uzbek and presented as an interactive, self-contained HTML page. It was created by Geedbro.

## How to Run

Open `artpark.html` directly in any web browser. There is no build system, package manager, or server required.

## Architecture

This is a **single-file static HTML document** (~43KB) containing all HTML, CSS, and JavaScript inline:

- **CSS** (~225 lines): CSS custom properties in `:root` for theming. Gold accent (`#b8943f`), light blue background (`#F2F8FC`). Uses CSS Grid layouts throughout. Responsive breakpoint at 900px. Fonts: Playfair Display (serif headings), DM Sans (body), JetBrains Mono (code/numbers) loaded from Google Fonts.
- **JavaScript** (~47 lines): Minimal vanilla JS for scroll-based nav styling (Intersection Observer for fade-in animations), smooth anchor navigation, and copy/right-click/devtools protection (the document is meant for controlled distribution).
- **Content sections**: Hero, Platform Overview, 8 Core Modules, 4-Layer Role Architecture (11 roles), 6-Step Approval Flow, Security Framework, Government Integrations, Standards Compliance, 3-Phase Roadmap, Team (16 specialists), Budget ($350K-$450K), Why Geedbro.

## Proposed Tech Stack (described in the document, not implemented here)

The HTML document specifies a platform to be built with: FastAPI + Python backend, React frontend, PostgreSQL, OpenFGA (authorization), NATS (messaging), Docker/Kubernetes, HashiCorp Vault, Redis, SIEM monitoring.

## Key Conventions

- All content is in **Uzbek language** (`lang="uz"`)
- CSS uses BEM-like naming (e.g., `.hero-meta-item`, `.module-card`, `.flow-content`)
- Color theming is centralized via CSS custom properties (`--accent`, `--bg`, `--surface`, `--text`, etc.)
- The document disables text selection, right-click context menu, and common devtools shortcuts via JS
