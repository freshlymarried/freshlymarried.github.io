# Contributing

## Portable Content

The content is designed to be portable. It is just standard markdown in [`content/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/content) and images in [`static/images/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/static/images).

The file names in `/content/posts/some-name.md` become permalinks at `https://freshlymarried.com/some-name`.

The only exceptions are the `_index.md` files and front matter at the top of each markdown file which are used by tools for programmatic pieces:

```yaml
---
title: "Some Title"
date: "YYYY-MM-DD"
tags:
  - "some-tag"
  - "another-tag"
featured_image: "/images/some-file.png"
---
```

## Production Dependencies

The repository strives to be self-contained without production dependencies at runtime.

The only exceptions are some external links. Including:

- Newsletter service (Mailchimp)
- Analytics service (Google Analytics)
- Affiliates service (Amazon Associates)
- Social media accounts (Facebook and Instagram)

## Development Dependencies

The rest is minimal development dependencies that could be easily swapped out. Including:

- Version control (Git)
- Remote repository (GitHub)
- CI/CD (GitHub Actions)
- Hosting (GitHub Pages)
- Static site generator (Hugo)

### Development Branches

- The `main` branch is used as the source.
- The branch `gh-pages` and the repository name `freshlymarried.github.io` are used by GitHub pages.

### Development Files

- `.git/` and [`.gitignore`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/.gitignore) hold version control history used by Git and GitHub.
- [`README.md`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/README.md) and [`CONTRIBUTING.md`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/CONTRIBUTING.md) hold documentation used by GitHub.
- [`config.toml`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/config.toml) holds configuration values used by Hugo.
- [`.gitmodules`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/.gitmodules) and [`themes/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/themes) hold the theme used by Hugo. It is [a fork](https://github.com/freshlymarried/gohugo-theme-ananke) so that the version is pinned without automatic breaking changes.
- [`layouts/partials/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/layouts/partials) holds theme overrides used by Hugo. These are avoided where possible.
- [`.github/workflows/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/.github/workflows) holds CI/CD configuration used by GitHub Actions. This uses pinned versions without automatic breaking changes.
