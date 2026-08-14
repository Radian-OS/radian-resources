# UI Shadows

<p align="center">
  <strong>High-quality, pre-optimized PNG shadow overlays for UI elements and layouts.</strong>
</p>

This package contains **10 pre-rendered, high-quality shadow PNG assets** (in Center, Left, and Right alignments with various intensities) tailored for developers and UI/UX designers to add realistic shadow depth to elements, containers, and card layers.

---

## 🚀 CDN Usage (Zero Install)

You do not need to install this package. You can hotlink and embed the shadows directly into your applications using the jsDelivr global CDN:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/shadow/src/{filename}
```

*Replace `{filename}` with the shadow filename (e.g., `CenterA.png`, `LeftB.png`, `RightC.png`).*

---

## 🛠️ Code Example (React / Next.js)

To display these shadow overlays directly in your web applications, you can use standard image tags or remote HTML loading:

```tsx
import Image from 'next/image';

export default function UIShadow() {
  return (
    <Image 
      src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/shadow/src/CenterA.png"
      alt="Radian UI Shadow Overlay"
      width={600}
      height={200}
      className="w-full object-cover"
    />
  );
}
```

### HTML Example
```html
<img src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/shadow/src/CenterA.png" alt="Radian UI Shadow Overlay" width="600" height="200" />
```


