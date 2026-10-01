# Brand Logos

<p align="center">
  <strong>Ready-to-use scalable brand icons and wordmarks for light and dark interfaces.</strong>
</p>

This package contains **244 brands** across **12 categories**. Every brand provides scalable SVG icons and wordmarks for both light and dark interfaces, across colored and neutral colorways, for a total of **1,952 SVG assets**.

SVGs serve as the single source of truth—infinitely scalable, razor-sharp on all display densities, and lightweight. All canonical directory names and filenames are lowercase, kebab-case, and URL-safe. The machine-readable [manifest](./manifest.json) is the source of truth for categories, brand slugs, coverage, and the path template.

---

## Available Variants

| Option | Values |
| --- | --- |
| Theme | `light`, `dark` |
| Colorway | `colored`, `neutral` |
| Variant | `icon`, `wordmark` |
| Format | `SVG` (100% coverage across all 244 brands) |
| Native Canvas | Icons are designed on a `24×24` grid; wordmarks are designed on a `180×48` canvas |

`light` and `dark` describe the interface surface the artwork is optimized for.

`colored` describes the official full-color brand artwork.

`neutral` provides monochrome brand artwork adapted for the interface (`#26282C` dark slate for light surfaces, `#F7F7F8` crisp off-white for dark surfaces).

Because SVG assets are scalable vector graphics, consumers can freely scale them with CSS or HTML dimensions (such as `width`, `height`, `max-width`, and `object-fit: contain`).

---

## File Structure

Canonical assets follow this pattern:

```text
src/{theme}/{colorway}/{category}/{variant}/{brand}.svg
```

Examples:

```text
src/light/colored/development/icon/github.svg
src/dark/colored/ai/wordmark/openai.svg
src/light/neutral/frameworks/icon/tailwind-css.svg
src/dark/neutral/design-creative/wordmark/figma.svg
```

The category is part of the URL. Use the manifest or the catalog below to resolve it.

---

## Brand Catalog

| Category | Count | Brand slugs |
| --- | ---: | --- |
| AI (`ai`) | 22 | `anthropic`, `chatgpt`, `claude`, `cohere`, `copilot`, `cursor`, `elevenlabs`, `gemini`, `github-copilot`, `google-deepmind`, `grok`, `groq`, `hugging-face`, `langchain`, `meta-ai`, `midjourney`, `mistral-ai`, `ollama`, `openai`, `perplexity`, `stability-ai`, `windsurf` |
| Business & Marketing (`business-marketing`) | 23 | `algolia`, `amplitude`, `auth0`, `brevo`, `clerk`, `hotjar`, `hubspot`, `intercom`, `klaviyo`, `mailchimp`, `mixpanel`, `okta`, `optimizely`, `resend`, `salesforce`, `sendgrid`, `shopify`, `strapi`, `twilio`, `webflow`, `wordpress`, `zapier`, `zendesk` |
| Cloud & DevOps (`cloud-devops`) | 22 | `ansible`, `aws`, `aws-lambda`, `circleci`, `cloudflare`, `datadog`, `digital-ocean`, `docker`, `google-cloud`, `grafana`, `heroku`, `jenkins`, `kubernetes`, `microsoft-azure`, `netlify`, `oracle`, `prometheus`, `railway`, `sentry`, `terraform`, `travis-ci`, `vercel` |
| Database & Data (`database-data`) | 19 | `aws-dynamodb`, `cassandra`, `cockroachdb`, `databricks`, `drizzle`, `elasticsearch`, `firebase`, `google-bigquery`, `mariadb`, `mongodb`, `mysql`, `planetscale`, `postgresql`, `prisma`, `redis`, `sequelize`, `snowflake`, `sqlite`, `supabase` |
| Design & Creative (`design-creative`) | 13 | `adobe`, `affinity`, `autodesk`, `behance`, `blender`, `canva`, `dribbble`, `figma`, `framer`, `invision`, `miro`, `sketch`, `zeplin` |
| Development (`development`) | 32 | `bitbucket`, `bun`, `codepen`, `codesandbox`, `cpp`, `dart`, `deno`, `elixir`, `github`, `gitlab`, `go`, `insomnia`, `java`, `javascript`, `kotlin`, `lua`, `npm`, `php`, `postman`, `postmarketos`, `python`, `r`, `replit`, `ruby`, `rust`, `scala`, `stack-overflow`, `stackblitz`, `swagger`, `swift`, `typescript`, `yarn` |
| Entertainment & Gaming (`entertainment-gaming`) | 7 | `disney`, `netflix`, `nintendo`, `playstation`, `spotify`, `unity`, `unreal-engine` |
| Finance & Payments (`finance-payments`) | 23 | `airwallex`, `alipay`, `amazon-pay`, `american-express`, `apple-pay`, `cash-app`, `discover`, `google-pay`, `jcb`, `mastercard`, `paypal`, `paystack`, `payu`, `razorpay`, `revolut`, `samsung-pay`, `square`, `stripe`, `unionpay`, `venmo`, `visa`, `wechat-pay`, `wise` |
| Frameworks (`frameworks`) | 27 | `angular`, `astro`, `bootstrap`, `django`, `dotnet`, `express`, `fastapi`, `fastify`, `flutter`, `gatsby`, `graphql`, `laravel`, `nestjs`, `nextjs`, `nuxtjs`, `react`, `redux`, `remix`, `ruby-on-rails`, `spring`, `storybook`, `svelte`, `sveltekit`, `tailwind-css`, `vite`, `vue`, `webpack` |
| Productivity & Work (`productivity-work`) | 20 | `airtable`, `asana`, `calendly`, `clickup`, `confluence`, `dropbox`, `evernote`, `google-drive`, `google-workspace`, `jira`, `linear`, `loom`, `microsoft-365`, `monday`, `notion`, `slack`, `teams`, `todoist`, `trello`, `zoom` |
| Social & Content (`social-content`) | 15 | `discord`, `facebook`, `instagram`, `linkedin`, `medium`, `pinterest`, `product-hunt`, `reddit`, `substack`, `telegram`, `tiktok`, `twitch`, `whatsapp`, `x`, `youtube` |
| Technology (`technology`) | 21 | `acer`, `amazon`, `amd`, `android-studio`, `apple`, `asus`, `dell`, `google`, `hp`, `intel`, `jetbrains`, `lenovo`, `lg`, `meta`, `microsoft`, `nvidia`, `samsung`, `sony`, `vs-code`, `xcode`, `xiaomi` |

---

## CDN Usage (Zero Install)

No installation is required. Load an asset directly through jsDelivr:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/{theme}/{colorway}/{category}/{variant}/{brand}.svg
```

For immutable production URLs, replace `@main` with a release tag or commit hash.

### HTML Example

```html
<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/dark/colored/development/wordmark/github.svg"
  />
  <img
    src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/light/colored/development/wordmark/github.svg"
    alt="GitHub"
    width="180"
    height="48"
  />
</picture>
```

### React / Next.js Example

```tsx
import Image from 'next/image';

interface BrandLogoProps {
  brand: string;
  category: string;
  variant?: 'icon' | 'wordmark';
  theme?: 'light' | 'dark';
  colorway?: 'colored' | 'neutral';
  width?: number;
  height?: number;
}

export default function BrandLogo({
  brand,
  category,
  variant = 'icon',
  theme = 'light',
  colorway = 'colored',
  width = 24,
  height = 24,
}: BrandLogoProps) {
  const src = `https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/${theme}/${colorway}/${category}/${variant}/${brand}.svg`;

  return (
    <Image
      src={src}
      alt={`${brand} logo`}
      width={width}
      height={height}
      unoptimized
    />
  );
}
```

When using the Next.js image optimizer, allow `cdn.jsdelivr.net` in your `next.config.js` or `next.config.mjs` remote image configuration.

---

Brand names and logos are trademarks of their respective owners. Inclusion here does not imply endorsement or affiliation.
