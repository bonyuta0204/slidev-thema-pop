# Theme Screenshots

This directory contains automatically generated screenshots of the slidev-theme-horizon theme.

The screenshots are generated using the GitHub Actions workflow defined in `.github/workflows/screenshots.yml` and are updated whenever changes are made to the theme components, layouts, styles, or example presentation.

These screenshots are used in the theme documentation and on npm to showcase the theme's appearance and features.

## How Screenshots are Generated

1. The GitHub Actions workflow runs the `pnpm screenshot` command
2. This command uses Slidev's export functionality to generate PNG images of each slide
3. The images are moved to this directory
4. Changes are committed back to the repository

## Manual Screenshot Generation

To generate screenshots manually:

```bash
pnpm screenshot
```

This will create PNG files in the project root, which you can then move to this directory.
