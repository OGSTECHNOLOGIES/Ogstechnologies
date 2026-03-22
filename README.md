# OGS Technologies Website

A modern, responsive, and professional website for OGS Technologies - a tech and energy solutions company based in Nigeria.

## About OGS Technologies

OGS Technologies provides:
- Solar power system installation and maintenance
- CCTV and security system installation
- Smart electrical wiring and maintenance
- Technical training through OGS Technologies Academy

## Features

- Modern, clean design with red, black, and white color scheme
- Fully responsive across all devices
- Smooth scrolling navigation
- Service showcase with detailed descriptions
- Academy section highlighting training programs
- Contact form with WhatsApp integration
- Floating WhatsApp chat button
- Fast loading and optimized for static hosting

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |

## Deploying to GitHub Pages

1. Push your code to a GitHub repository
2. Go to your repository settings on GitHub
3. Navigate to Pages section
4. Set Source to "GitHub Actions"
5. Create `.github/workflows/deploy.yml` with the following content:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout your repository using git
        uses: actions/checkout@v4
      - name: Install, build, and upload your site
        uses: withastro/action@v2

  deploy:
    needs: build
    runs-on: ubuntu-latest
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

6. Your site will be automatically deployed to `https://yourusername.github.io/repository-name/`

## Contact Information

**OGS Technologies**
- Phone: 09064424710, 09133970588
- Address: No: 25 Powa Shop, Opp. St. Finbarrs Catholic Church, Bende Rd, Umuahia, Abia State
- Website: [Coming Soon]

## Built With

- [Astro](https://astro.build) - Static Site Generator
- [Inter Font](https://fonts.google.com/specimen/Inter) - Typography
