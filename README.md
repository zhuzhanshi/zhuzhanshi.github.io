# Academic Homepage

Source repository for a personal academic homepage hosted at
[https://zhuzhanshi.github.io/](https://zhuzhanshi.github.io/).

The site is built with the [HugoBlox Academic CV template](https://hugoblox.com/templates/academic-cv)
and deployed to GitHub Pages through GitHub Actions.

## Scope

The homepage is designed to present verified academic information in English:

- Research interests and themes
- Publications
- Research projects
- Education and professional experience
- Academic services

No publication, project, appointment, or service record should be added without
verified information. Until details are available, pages deliberately contain
placeholders.

## Local Development

Prerequisites:

- Hugo Extended `0.161.1`
- Node.js `22`
- pnpm `10`

```bash
pnpm install
hugo server
```

Production build:

```bash
hugo --minify --cleanDestinationDir --baseURL "https://zhuzhanshi.github.io/"
pnpm run pagefind
```

## Deployment

Pushes to `main` trigger `.github/workflows/deploy.yml`. GitHub Pages must be
configured to use **GitHub Actions** as its deployment source.

## Content Maintenance

- Profile metadata: `data/authors/me.yaml`
- Homepage layout: `content/_index.md`
- Primary navigation: `config/_default/menus.yaml`
- Site configuration and styling: `config/_default/params.yaml`
- Section pages: `content/research/`, `content/publications/`,
  `content/projects/`, `content/experience.md`, and
  `content/academic-services/`

Keep changes focused and run a production build before publishing.
