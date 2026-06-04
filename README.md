# RDA ambassador Website

🌐 **Live Website:** [https://alliance-rdm-gdr.github.io/RDA_AmabassadorsSite/](https://alliance-rdm-gdr.github.io/RDA_AmabassadorsSite/)

This is the official repository for the **RDA ambassador** website. The goal of this site is to centralize materials, resources, videos, and guides for community members and the general public, promoting FAIR data principles and Research Data Alliance (RDA) outputs.

## Project Description

The site is built using **Quarto**, allowing ambassadors to easily contribute new resources without needing to modify the site's source code.

## Project Architecture

The project follows a modular structure designed for scalability and organization:

- **`_quarto.yml`**: Global site configuration, navigation, and search.
- **`index.qmd`**: Dynamic landing page.
- **`/pages`**: Contains the main sections of the site:
  - `ambassadors/`: Experts directory.
  - `resources/`: Library of resources and materials.
  - `contribute/`: Contribution guide for the community.
- **`/data`**: Stores CSV databases (`resources.csv`, `ambassadors.csv`) that power the dynamic content.
- **`/assets`**: Repository for physical files (PDFs, images, thumbnails) organized by domain.
- **`/docs`**: Detailed technical documentation and update logs.

## Detailed Documentation

For more technical details on the design, dynamic content workflow, and style guide, please see:

- [**Detailed Architecture**](docs/ARCHITECTURE.md)
- [**Update Logs**](docs/UPDATES.md)

---

_Built with Quarto and a passion for open data._
