# Contributing to OpenAPI.Tools

## 🛠 Adding New Tools

To add a new tool to the project, you need to create a new markdown file in the `src/content/tools/` directory. Each tool should have its own file.

1. Navigate to the `src/content/tools/` directory.
2. Create a new markdown file. The file name should be the name of the tool, with spaces replaced by hyphens (e.g., `my-new-tool.md`).
3. In the new markdown file, add the necessary information about the tool. Here's a basic template you can use:

  ```markdown
  ---
  name: 'Tool Name'
  description: 'A brief description of the tool.'
  categories:
    - docs
    - sdk-generators
    - code-validators
    - servers
    - mocking-tools
  languages: { 'Language1': true, 'Language2': false }
  link: 'https://toolwebsite.com'
  repo: 'https://github.com/tool'
  openApiVersions:
    v2: false
    v3: true
    v3_1: true
    v4: true
  ---

  ## Overview

  Provide an overview of the tool here.

  ## Features

  List the main features of the tool here.

  ## Usage

  Explain how to use the tool here.
  ```

  See `/src/content/categories/` for the list of available categories. If the tool fits into multiple categories, you can add them to the `categories` list. Make the categories you list match the file name of existing categories from the `/src/content/categories/` directory.

  If you think we're missing a category, feel free create an issue or open a pull request to add a new category and we'll review it!

1. Fill in the information for the tool. Make sure to replace `'Tool Name'`, `'A brief description of the tool.'`, `'https://toolwebsite.com'`, `'The category of the tool'`, and the content of the sections with the appropriate information.

2. Save the file.

3. Open a pull request with your changes to have the new tool added to the project.

---

## Openapi.tools is built with Astro

[Astro](https://astro.build/) is the web content framework for content-driven websites. Our configuration of Astro uses React, TypeScript, and Tailwind CSS.

### 🚀 Project Structure

Inside of the repo, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── content/
│   │   ├── categories/
│   │   └── tools/
│   ├── components/
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put React components.

Any static assets, like images, can be placed in the `public/` directory.

### 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                       |
| :--------------------- | :------------------------------------------- |
| `pnpm install`         | Installs dependencies                        |
| `pnpm dev`             | Starts local dev server at `localhost:4321`  |
| `pnpm build`           | Build your production site to `./dist/`      |
| `pnpm preview`         | Preview your build locally, before deploying |
| `pnpm astro ...`       | CLI commands like `astro add`, `astro check` |
| `pnpm astro -- --help` | Get help using the Astro CLI                 |
| `pnpm prettier-fix`    | Format your code with Prettier               |
| `pnpm lint`            | Lint your code with ESLint                   |

## 👀 Want to learn more about Astro?

Feel free to check out [Astro documentation](https://docs.astro.build).
