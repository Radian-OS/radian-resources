# Brand Logos

<p align="center">
  <strong>Ready-to-use brand icons and wordmarks for light and dark interfaces.</strong>
</p>

This package contains **20 brands** in two themes, two variants, and both SVG and PNG formats—a total of **160 assets**. Every filename and directory is lowercase and URL-safe for predictable CDN use.

---

## Available Variants

| Option | Values |
| --- | --- |
| Theme | `light`, `dark` |
| Variant | `icon`, `wordmark` |
| Format | SVG, transparent PNG |
| PNG size | Icons: `48×48`; wordmarks: `48px` high |

Use `light` assets on light surfaces and `dark` assets on dark surfaces.

### Brands

`adobe`, `angular`, `anthropic`, `bitbucket`, `canva`, `claude`, `figma`, `framer`, `gemini`, `github`, `gitlab`, `google-deepmind`, `miro`, `nextjs`, `npm`, `openai`, `react`, `stack-overflow`, `tailwind-css`, `vue`

---

## File Structure

SVG assets follow this pattern:

```text
src/{theme}/svg/{variant}/{brand}.svg
```

PNG assets follow this pattern:

```text
src/{theme}/png/48px/{variant}/{brand}.png
```

Examples:

```text
src/light/svg/icon/github.svg
src/dark/svg/wordmark/openai.svg
src/light/png/48px/icon/tailwind-css.png
```

---

## CDN Usage (Zero Install)

No installation is required. Load an asset directly through the jsDelivr CDN:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/{theme}/svg/{variant}/{brand}.svg
```

For PNG:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/{theme}/png/48px/{variant}/{brand}.png
```

For immutable production URLs, replace `@main` with a release tag after the assets are included in a release.

### HTML Example

```html
<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/dark/svg/wordmark/github.svg"
  />
  <img
    src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/light/svg/wordmark/github.svg"
    alt="GitHub"
    width="180"
    height="48"
  />
</picture>
```

### React / Next.js Example

```tsx
import Image from 'next/image';

export default function BrandLogo() {
  return (
    <Image
      src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/light/svg/icon/github.svg"
      alt="GitHub"
      width={48}
      height={48}
    />
  );
}
```

When using the Next.js image optimizer, allow `cdn.jsdelivr.net` in your `next.config.js` or `next.config.mjs` remote image configuration.

---

Brand names and logos are trademarks of their respective owners. Inclusion here does not imply endorsement or affiliation.
