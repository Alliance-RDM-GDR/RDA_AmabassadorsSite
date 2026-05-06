# Project Architecture

## Overview
This repository contains the source code for the RDA Domain Ambassadors website, built using [Quarto](https://quarto.org/). It is designed to be a modern, dynamic static site that centralizes resources and ambassador profiles for the Research Data Alliance community.

## Directory Structure

To keep the project organized as it grows and participants add more resources, we use a modular and scalable structure:

### 1. Core Site Files (Root)
- `_quarto.yml`: Main Quarto configuration (navigation, metadata, theme).
- `styles.scss`: Custom styles (RDA colors, animations).
- `index.qmd`, `about.qmd`: Main static pages.

### 2. Documentation (`/docs`)
- `docs/ARCHITECTURE.md`: Technical project documentation (this file).
- `docs/UPDATES.md`: History of changes and updates.

### 3. Dynamic Content Generation (`/data`)
Instead of creating a page for each resource, we use simple databases:
- `data/ambassadors.csv`: Information about the ambassadors.
- `data/resources.csv`: Metadata for all resources (title, author, domain, file link).

### 4. Site Sections (`/pages`)
To avoid cluttering the root with `.qmd` files:
- `pages/ambassadors/index.qmd`: Ambassadors directory.
- `pages/resources/index.qmd`: Main resource search engine.
- `pages/contribute/index.qmd`: Contribution guide for users.

### 5. User-Uploaded Files (`/assets`)
This is where physical files (PDFs, images) are stored, organized logically to avoid chaos:
- `assets/images/ambassadors/`: Profile pictures.
- `assets/resources/domains/agriculture/`: Domain-specific documents for agriculture.
- `assets/resources/domains/humanities/`: Humanities documents.
- `assets/resources/shared/`: General guides (e.g., FAIR data principles) that apply to everyone.

This strict separation between **code** (`.qmd`), **data** (`.csv`), and **files** (`assets/`) ensures the repository remains easy to maintain even with thousands of resources.

## Dynamic Content Workflow
To make contributions seamless, the site will implement a data-driven architecture. 
Instead of hardcoding resources into Markdown, structured data (e.g., lists of resources or ambassadors) will be pulled from data files (like `data/resources.csv` or `data/ambassadors.csv`). 
During the Quarto build process, this data is rendered dynamically. This empowers non-technical contributors to update the site simply by editing a spreadsheet or CSV file.

## Theming & Styling
The site leverages Quarto's built-in Bootstrap 5 integration:
1. **Base Theme:** Starting with the `cosmo` theme for a clean, professional baseline.
2. **Customizations:** The `styles.scss` overrides Bootstrap default variables to introduce a bespoke primary/secondary color palette.
3. **Components:** Custom utility classes (`.hero-banner`, `.resource-card`) are used extensively to create premium layouts and subtle animations that enhance user experience.
