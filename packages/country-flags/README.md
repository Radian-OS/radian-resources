# Country Flags

<p align="center">
  <strong>Ready-to-use PNG flags in multiple sizes and shapes for selectors, profiles, tables, and other interfaces.</strong>
</p>

This package contains **258 flag designs**, including countries, territories, regions, and organizations. Every design is available in **7 sizes** and **3 shapes**, for a total of **5,418 PNG assets**.

---

## Available Variants

| Option | Values |
| --- | --- |
| Sizes | `16px`, `24px`, `32px`, `64px`, `128px`, `256px`, `512px` |
| Shapes | `flat`, `circle`, `squircle` |
| Format | Transparent PNG |

Assets use the following directory and filename structure:

```text
src/{size}px/{shape}/{name}-{shape}-{size}.png
```

For example:

```text
src/32px/circle/Japan-circle-32.png
src/64px/flat/United States-flat-64.png
src/128px/squircle/Nepal-squircle-128.png
```

File names are case-sensitive. Use the exact asset name from the relevant shape directory, and URL-encode spaces as `%20` when constructing a URL.

---

## CDN Usage (Zero Install)

No installation is required. Load any flag directly through jsDelivr using this URL pattern:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/{size}px/{shape}/{name}-{shape}-{size}.png
```

Example:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/32px/circle/Japan-circle-32.png
```

---

## React / Next.js Example

```tsx
import Image from 'next/image';

interface CountryFlagProps {
  name: string;
  size?: 16 | 24 | 32 | 64 | 128 | 256 | 512;
  shape?: 'flat' | 'circle' | 'squircle';
}

export default function CountryFlag({
  name,
  size = 32,
  shape = 'circle',
}: CountryFlagProps) {
  const fileName = `${name}-${shape}-${size}.png`;
  const src = `https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/${size}px/${shape}/${encodeURIComponent(fileName)}`;

  return (
    <Image
      src={src}
      alt={`${name} flag`}
      width={size}
      height={size}
    />
  );
}
```

When using the Next.js image optimizer, allow `cdn.jsdelivr.net` in your `next.config.js` or `next.config.mjs` remote image configuration.

### HTML Example

```html
<img
  src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/32px/circle/Japan-circle-32.png"
  alt="Japan flag"
  width="32"
  height="32"
/>
```
