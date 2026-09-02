# UI Avatars

<p align="center">
  <strong>High-quality, pre-optimized transparent PNG avatars for your UI designs.</strong>
</p>

This package contains **200 diverse, high-quality user avatars** tailored for developers and UI/UX designers to use in mockups, default profiles, test suites, and live apps.

---

## 🚀 CDN Usage (Zero Install)

You do not need to install this package to use the avatars. You can hotlink them directly in your app via the jsDelivr global CDN using the following URL structure:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/avatars/src/{id}.png
```

*Replace `{id}` with a number from `1` through `200` (e.g., `1.png`, `42.png`, `180.png`).*

---

## 🛠️ Code Example (Next.js)

To display these avatars efficiently in a React/Next.js environment, use the Next.js `<Image />` component:

```tsx
import Image from 'next/image';

export default function RadianAvatar() {
  return (
    <Image 
      src="[https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/avatars/src/1.png](https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/avatars/src/1.png)"
      alt="Radian UI Avatar"
      width={48}
      height={48}
      className="rounded-full object-cover"
    />
  );
}
```

### Next.js Image Optimization Configuration
To permit Next.js to fetch and optimize these images from the CDN, add the following configuration to your `next.config.js` or `next.config.mjs`:

```javascript
/** @type {import('next').NextConfig} */
const nextConfig = {
  images: {
    remotePatterns: [
      {
        protocol: 'https',
        hostname: 'cdn.jsdelivr.net',
        port: '',
        pathname: '/gh/Radian-os/radian-resources/**',
      },
    ],
  },
};

module.exports = nextConfig;
```

