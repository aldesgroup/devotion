# Devotion Documentation

This repository contains the documentation for the Devotion project, a comprehensive full-stack development stack. This documentation is built using Docusaurus 2, a modern static website generator. And it's deployed as a [GitHub Page](https://aldesgroup.github.io/devotion/).

- [Devotion Documentation](#devotion-documentation)
  - [Installation](#installation)
  - [Development](#development)
  - [Deployment](#deployment)
  - [License](#license)

[top](#devotion-documentation)

---

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/devotion.git
cd devotion
```

2. Navigate to the website directory and install dependencies:
```bash
cd website
npm install
```

[top](#devotion-documentation)

---

## Development

To start the development server:

```bash
npm start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

The content is structured this way:

- First page is [here](./website/src/pages/index.tsx)
- The website config & layout is [here](./website/docusaurus.config.ts)
- The side bar is configured [here](./website/sidebars.ts)
- Global styles are in [here](./website/src/css/custom.css)
- The documentation pages are organised [here](./website/docs/)

[top](#devotion-documentation)

---

## Deployment

The documentation is automatically deployed to GitHub Pages using GitHub Actions. The workflow is configured in `.github/workflows/deploy.yml`.

[top](#devotion-documentation)

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

[top](#devotion-documentation)

---