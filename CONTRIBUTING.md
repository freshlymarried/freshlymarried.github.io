# Contributing

## Content

The content is designed to be portable. It is just standard markdown files in [`content/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/content) and image files in [`static/images/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/static/images).

The only exceptions are the `_index.md` files that Hugo uses and front matter at the top of each markdown file which Hugo uses but could be used by other tools for programmatic pieces:

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

## Permalinks

The file names in `/content/posts/some-name.md` become permalinks at `https://freshlymarried.com/some-name`.

## Tooling

The rest is minimal tooling that could be easily swapped out. It is currently using Git, GitHub, and Hugo:

- `.git/` and [`.gitignore`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/.gitignore) hold version control history used by Git and GitHub.
- [`README.md`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/README.md) and [`CONTRIBUTING.md`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/CONTRIBUTING.md) hold documentation used by GitHub.
- [`config.toml`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/config.toml) holds configuration values used by Hugo.
- [`.gitmodules`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/.gitmodules) and [`themes/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/themes) hold the theme used by Hugo. It is [a fork](https://github.com/freshlymarried/gohugo-theme-ananke) so that the version is pinned without automatic breaking changes.
- [`layouts/partials/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/layouts/partials) holds theme overrides used by Hugo. These are avoided where possible.
- [`.github/workflows/`](https://github.com/freshlymarried/freshlymarried.github.io/tree/main/.github/workflows) holds CI/CD configuration used by GitHub Actions. This uses pinned versions without automatic breaking changes.

## Runtime Integrations

The repository is self-contained without runtime dependencies.

The only exceptions are an analytics service (Google Analytics) and some external links - like the newsletter service (Mailchimp), social media, and Amazon Associates.
