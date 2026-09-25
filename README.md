# Radian UI Resources

<p align="center">
  <strong>The official static marketing and UI asset hub for the Radian Design System.</strong><br />
  High-quality, optimized, free design assets served directly via a global CDN.
</p>

<p align="center">
  <a href="https://github.com/Radian-os/radian-resources/blob/main/LICENSE"><img src="https://img.shields.io/github/license/Radian-os/radian-resources?style=flat-square" alt="License" /></a>
  <a href="https://radianui.com"><img src="https://img.shields.io/badge/design_system-Radian-blue?style=flat-square" alt="Radian Design System" /></a>
  <a href="https://www.jsdelivr.com/"><img src="https://img.shields.io/badge/cdn-jsDelivr-orange?style=flat-square" alt="jsDelivr CDN" /></a>
</p>

---

## ⚡ Overview

[Radian](https://radianui.com) is an open-source React component library built on Radix UI and Tailwind CSS.

**Radian Resources** (`radian-resources`) is a dedicated public repository for hosting and serving Radian's static design assets—such as user avatars, brand logos, country flags, and file-type icons. 

By leveraging the free, global **jsDelivr CDN**, developers can hotlink these assets directly in their production applications with zero bandwidth costs and ultra-low latency.

---

## 🚀 How It Works (CDN Hotlinking)

You do **not** need to clone this repository or install npm packages to use these assets. All assets are hotlinkable directly from your application using the following base CDN URL format:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/{package-name}/src/{file}
```

- **`{package-name}`**: The subfolder name under `packages/` (e.g., `avatars`, `brand-logos`).
- **`{file}`**: The path to the asset inside that package (e.g., `1.png`, `light/colored/png/development/icon/github.png`).

---

## 📦 Available Assets

This repository contains the following asset collections. Click on a category name to view its detailed documentation, exact asset lists, and integration examples.

| Asset Category | Directory / Documentation | Description |
| :--- | :--- | :--- |
| **Avatars** | [packages/avatars](./packages/avatars/README.md) | 200 transparent, high-quality PNG user avatars for UI mocks. |
| **Avatar Backgrounds** | [packages/avatars-background](./packages/avatars-background/README.md) | 58 solid, gradient, and image backgrounds for UI avatars. |
| **Brand Logos** | [packages/brand-logos](./packages/brand-logos/README.md) | 244 categorized brands with colored PNG icons and wordmarks for light and dark themes, plus SVG coverage for 20 brands. |
| **Chart Thumbnails** | [packages/charts-thumbnail](./packages/charts-thumbnail/README.md) | Pre-rendered light and dark mode chart thumbnail previews. |
| **Country Flags** | [packages/country-flags](./packages/country-flags/README.md) | 257 scalable SVG flags for countries, territories, regions, and organizations. |
| **File Icons** | [packages/file-icons](./packages/file-icons/README.md) | Consistent, modern SVG file-type icons. |
| **Shadow Overlays** | [packages/shadow](./packages/shadow/README.md) | Pre-rendered shadow overlays for UI layout depth. |

---

## 📄 License

All assets in this repository are licensed under the MIT License unless otherwise specified. Feel free to use them in both commercial and personal projects.
