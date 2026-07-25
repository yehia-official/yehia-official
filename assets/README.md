# assets/

This folder holds local images referenced by the profile `README.md`
(project screenshots, GIF previews, etc.) instead of relying only on
external hosted images.

## Suggested structure

```
assets/
├── quizzy-preview.gif
├── spark-preview.gif
├── gdgc-preview.gif
└── guide-preview.gif
```

## Guidelines

- Keep images reasonably sized (compress GIFs/PNGs before committing —
  large media slows down profile page load times).
- Reference files from `README.md` with a relative path, e.g.:
  ```markdown
  ![Quizzy Preview](./assets/quizzy-preview.gif)
  ```
- Prefer `.webp` or optimized `.png`/`.gif` over raw screenshots.

<!-- TODO: add real screenshots/GIFs once available -->
