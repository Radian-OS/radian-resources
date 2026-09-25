# Country Flags

<p align="center">
  <strong>Ready-to-use scalable SVG flags for selectors, profiles, tables, and other interfaces.</strong>
</p>

This package contains **257 SVG flags**, including countries, territories, regions, and organizations. The contents of [`src/flags`](./src/flags) are the source of truth for all available flags and filenames.

---

## Available Assets

| Option | Values |
| --- | --- |
| Format | SVG |
| Directory | `src/flags` |
| Naming | Lowercase, kebab-case slugs |

Assets use the following directory and filename structure:

```text
src/flags/{slug}.svg
```

For example:

```text
src/flags/japan.svg
src/flags/united-states.svg
src/flags/nepal.svg
```

File names are case-sensitive. Use the exact lowercase, kebab-case slug found in `src/flags`.

---

## CDN Usage (Zero Install)

No installation is required. Load any flag directly through jsDelivr:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/flags/{slug}.svg
```

Example:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/flags/japan.svg
```

---

## React / Next.js Example

```tsx
import Image from 'next/image';

interface CountryFlagProps {
  slug: string;
  label: string;
  size?: number;
}

export default function CountryFlag({
  slug,
  label,
  size = 32,
}: CountryFlagProps) {
  const src = `https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/flags/${encodeURIComponent(slug)}.svg`;

  return (
    <Image
      src={src}
      alt={`${label} flag`}
      width={size}
      height={size}
      unoptimized
    />
  );
}
```

When using the Next.js image optimizer, allow `cdn.jsdelivr.net` in your `next.config.js` or `next.config.mjs` remote image configuration.

### HTML Example

```html
<img
  src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/flags/japan.svg"
  alt="Japan flag"
  width="32"
  height="32"
/>
```
