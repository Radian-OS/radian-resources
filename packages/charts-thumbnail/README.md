# Chart Thumbnails

<p align="center">
  <strong>Pre-rendered, high-quality chart thumbnail previews in light and dark modes for dashboard pickers and UI builders.</strong>
</p>

This package contains **12 pre-rendered, high-quality chart thumbnail PNG assets** representing popular chart types in both **light** and **dark** theme variants. These are ideal for chart type selectors, dashboard configuration modals, template previews, analytics builders, and UI mockups.

---

## 📊 Available Chart Thumbnails

| Chart Type | Light Mode Asset | Dark Mode Asset |
| :--- | :--- | :--- |
| **Area Chart** | `area-chart.png` | `area-chart-dark.png` |
| **Bar Chart** | `bar-chart.png` | `bar-chart-dark.png` |
| **Donut Chart** | `donut-chart.png` | `donut-chart-dark.png` |
| **Line Chart** | `line-chart.png` | `line-chart-dark.png` |
| **Pie Chart** | `pie-chart.png` | `pie-chart-dark.png` |
| **Radar Chart** | `radar-chart.png` | `radar-chart-dark.png` |

---

## 🚀 CDN Usage (Zero Install)

You do not need to install this package. You can hotlink and embed the chart thumbnails directly into your applications using the jsDelivr global CDN:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/charts-thumbnail/src/{filename}
```

*Replace `{filename}` with the chart asset name (e.g., `area-chart.png`, `bar-chart-dark.png`, `line-chart.png`).*

---

## 🛠️ Code Example (React / Next.js)

To display these chart thumbnails dynamically based on chart type and current theme (light/dark):

```tsx
import Image from 'next/image';

interface ChartThumbnailProps {
  type: 'area' | 'bar' | 'donut' | 'line' | 'pie' | 'radar';
  isDark?: boolean;
}

export default function ChartThumbnail({ type, isDark = false }: ChartThumbnailProps) {
  const fileName = isDark ? `${type}-chart-dark.png` : `${type}-chart.png`;
  const src = `https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/charts-thumbnail/src/${fileName}`;

  return (
    <div className="overflow-hidden rounded-lg border border-slate-200 dark:border-slate-800">
      <Image 
        src={src}
        alt={`${type} chart preview`}
        width={320}
        height={200}
        className="w-full h-auto object-cover"
      />
    </div>
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
        pathname: '/gh/Radian-os/radian-resources/**',
      },
    ],
  },
};

module.exports = nextConfig;
```

### HTML Example

```html
<!-- Light Mode -->
<img 
  src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/charts-thumbnail/src/bar-chart.png" 
  alt="Bar Chart Preview" 
  width="320" 
  height="200" 
/>

<!-- Dark Mode -->
<img 
  src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/charts-thumbnail/src/bar-chart-dark.png" 
  alt="Bar Chart Dark Preview" 
  width="320" 
  height="200" 
/>
```
