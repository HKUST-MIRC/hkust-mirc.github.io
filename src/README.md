# Note of using this template

- `config.yaml` is the main configuration file for the site. You can set site-wide settings like title, description, and theme here.
- `src/` directory contains the main source code for the website, including pages, components, styles
  - `src/components/` directory contains reusable UI components that can be used across different pages.
    - `src/components/logo.astro` is the logo component used in the header.
    - Check `src/components/widgets` for reusable widgets and compose them to make a page. Add new widges if necessary and do check this won's break the existing pages.
  - `src/pages/` directory contains the individual pages of the website. Each .astro file corresponds to a route on the site. Markdown files (.md) can also be used for content pages. - `src/pages/index.astro` is the homepage of the site.
  - Markdown can be parsing by `src/layouts/MarkdownLayout.astro` and `src/layouts/MarkdownLayoutWithToggle.astro`. If any new layout is needed, create a new layout file in `src/layouts/` and use it in the frontmatter of the markdown file.
  - Use `src/navigation.ts` to configure the header and footer links. `src/navigation.ts` contains the navigation structure for the site, including **header links**, **footer links**, and social media links.
    ~~- `ToggleMenu` is mannually removed to disable the mobile menu toggle button. It can be re-enabled by uncommenting the relevant lines in `src/components/widgets/Header.astro`.~~
- `showRssFeed` is mannually removed to disable the RSS feed icon in the header. It can be re-enabled by uncommenting the relevant lines in `src/layouts/PageLayout.astro`.

# Note for deployment

- Modify `.github/workflows/deploy.yml` for automated deployment settings.
  - Remember to set the `base` in `config.yaml` to `/` when doing local testing.
  - Set the `base` in `config.yaml` to `/Media-Intelligence-Center-Webpage/` when deploying to GitHub Pages.
