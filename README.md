# Wolverine Masters Water Polo Website

This is the official website for the Wolverine Masters Water Polo Club in Ann Arbor, Michigan.

## Development

### Prerequisites
- Node.js (v14 or higher)
- npm

### Getting Started
1. Clone the repository
   ```bash
   git clone https://github.com/<>/wolverine-masters-homepage.git
   cd wolverine-masters-homepage
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Start the development server
   ```bash
   npm run dev
   ```

4. Open your browser and visit `http://localhost:4321`

### Building for Production
```bash
npm run build
```

## Deployment to GitHub Pages

This website is automatically deployed to GitHub Pages using GitHub Actions. The deployment workflow is defined in `.github/workflows/deploy.yml`.

### How it works
1. When you push changes to the `main` branch, GitHub Actions will automatically build and deploy the site
2. The site is built using the Astro framework and deployed to GitHub Pages
3. The custom domain is configured using the CNAME file in the `public` directory

## Custom Domain Setup

### GitHub Pages Configuration
1. Go to your GitHub repository settings
2. Navigate to "Pages" in the sidebar
3. Under "Custom domain", enter `a2masterswaterpolo.com`
4. Check "Enforce HTTPS" (recommended)
5. Save the settings

### Domain Registrar Configuration
You need to configure your domain registrar with the following DNS records:

#### Option 1: Apex domain (a2masterswaterpolo.com)
Add A records pointing to GitHub Pages servers

#### Option 2: www subdomain (www.a2masterswaterpolo.com)
Add a CNAME record:
```
CNAME    www    your-username.github.io
```

#### Option 3: Both apex and www subdomain
- Set up the A records as in Option 1
- Add this CNAME record:
  ```
  CNAME    www    a2masterswaterpolo.com
  ```

## Content Updates

### Images
- Store website images in the `/public/images/` directory
- Reference them in `.astro` files using `<img src="/images/your-image.jpg" alt="Description" />`

### Text Content
- Main content files are in the `/src/pages/` directory
- Layout templates are in the `/src/layouts/` directory
- Components are in the `/src/components/` directory

```sh
npm create astro@latest -- --template minimal
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/minimal)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/minimal)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/minimal/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
