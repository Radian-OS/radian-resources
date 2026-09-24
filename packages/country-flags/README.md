# Country Flags

<p align="center">
  <strong>Ready-to-use PNG and SVG flags for selectors, profiles, tables, and other interfaces.</strong>
</p>

This package contains **258 flag designs**, including countries, territories, regions, and organizations. Every design is available as a PNG in **7 sizes** and **3 shapes**, for a total of **5,418 PNG assets**. The package also includes **257 scalable SVG flags**.

---

## Available Variants

| Option | Values |
| --- | --- |
| Sizes | `16px`, `24px`, `32px`, `64px`, `128px`, `256px`, `512px` |
| Shapes | `flat`, `circle`, `squircle` |
| PNG | Transparent PNG in 7 sizes and 3 shapes |
| SVG | Scalable SVG in the `flags` directory |

PNG assets use the following directory and filename structure. The directory identifies the size and shape, so filenames contain only the flag name:

```text
src/{size}px/{shape}/{name}.png
```

For example:

```text
src/32px/circle/Japan.png
src/64px/flat/United States.png
src/128px/squircle/Nepal.png
```

SVG assets use lowercase, kebab-case filenames:

```text
src/flags/{slug}.svg
```

For example:

```text
src/flags/japan.svg
src/flags/united-states.svg
src/flags/nepal.svg
```

File names are case-sensitive. For PNG files, use the exact asset name from the relevant shape directory and URL-encode spaces as `%20`. For SVG files, use the lowercase, kebab-case slug.

---

## CDN Usage (Zero Install)

No installation is required. Load any flag directly through jsDelivr.

### PNG

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/{size}px/{shape}/{name}.png
```

Example:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/32px/circle/Japan.png
```

### SVG

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
  name: string;
  size?: 16 | 24 | 32 | 64 | 128 | 256 | 512;
  shape?: 'flat' | 'circle' | 'squircle';
}

export default function CountryFlag({
  name,
  size = 32,
  shape = 'circle',
}: CountryFlagProps) {
  const fileName = `${name}.png`;
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
  src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/country-flags/src/flags/japan.svg"
  alt="Japan flag"
  width="32"
  height="32"
/>
```
