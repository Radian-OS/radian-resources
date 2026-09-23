# Brand Logos

<p align="center">
  <strong>Ready-to-use brand icons and wordmarks for light and dark interfaces.</strong>
</p>

This package contains **244 brands** across **12 categories**. Every brand has a colored PNG icon and wordmark for both light and dark interfaces, for a total of **976 PNG assets**. A curated set of 20 brands is also available as SVG.

All canonical directory names and filenames are lowercase, kebab-case, and URL-safe. The machine-readable [manifest](./manifest.json) is the source of truth for categories, brand slugs, coverage, and the path template.

---

## Available Variants

| Option | Values |
| --- | --- |
| Theme | `light`, `dark` |
| Colorway | `colored` |
| Variant | `icon`, `wordmark` |
| Format | PNG for all 244 brands; SVG for 20 brands |
| PNG canvas | Most icons are `64×64`; most wordmarks are `240×64` |

`light` and `dark` describe the interface surface the artwork is optimized for. `colored` describes the logo treatment.

The colorway is an independent path segment so future monochrome assets can be added as `black` and `white` under both themes:

```text
src/light/black/...
src/dark/black/...
src/light/white/...
src/dark/white/...
```

Those colorways are reserved in the manifest but do not contain assets yet.

The original canvas dimensions are preserved. A small number of logos use a wider or taller native canvas, so consumers should constrain artwork with CSS such as `max-width`, `max-height`, and `object-fit: contain` rather than assuming every file has identical dimensions.

---

## File Structure

Canonical assets follow this pattern:

```text
src/{theme}/{colorway}/{format}/{category}/{variant}/{brand}.{format}
```

Examples:

```text
src/light/colored/png/development/icon/github.png
src/dark/colored/png/ai/wordmark/openai.png
src/light/colored/png/frameworks/icon/tailwind-css.png
src/dark/colored/svg/design-creative/wordmark/figma.svg
```

The category is part of the URL. Use the manifest or the catalog below to resolve it.

---

## Brand Catalog

| Category | Count | Brand slugs |
| --- | ---: | --- |
| AI (`ai`) | 22 | `anthropic`, `apple-intelligence`, `claude`, `cohere`, `copilot`, `cursor`, `elevenlabs`, `gemini`, `github-copilot`, `google-deepmind`, `grok`, `groq`, `hugging-face`, `langchain`, `meta-ai`, `midjourney`, `mistral-ai`, `ollama`, `openai`, `perplexity`, `stability-ai`, `windsurf` |
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

## CDN Usage

No installation is required. Load an asset directly through jsDelivr:

```text
https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/{theme}/{colorway}/{format}/{category}/{variant}/{brand}.{format}
```

For immutable production URLs, replace `@main` with a release tag after the assets are included in a release.

### HTML Example

```html
<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/dark/colored/png/development/wordmark/github.png"
  />
  <img
    src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/light/colored/png/development/wordmark/github.png"
    alt="GitHub"
    width="240"
    height="64"
  />
</picture>
```

### React / Next.js Example

```tsx
import Image from 'next/image';

export default function BrandLogo() {
  return (
    <Image
      src="https://cdn.jsdelivr.net/gh/Radian-os/radian-resources@main/packages/brand-logos/src/light/colored/png/development/icon/github.png"
      alt="GitHub"
      width={64}
      height={64}
    />
  );
}
```

When using the Next.js image optimizer, allow `cdn.jsdelivr.net` in your `next.config.js` or `next.config.mjs` remote image configuration.

---

## SVG Coverage

The following 20 brands also provide categorized SVG icon and wordmark files for both themes:

`adobe`, `angular`, `anthropic`, `bitbucket`, `canva`, `claude`, `figma`, `framer`, `gemini`, `github`, `gitlab`, `google-deepmind`, `miro`, `nextjs`, `npm`, `openai`, `react`, `stack-overflow`, `tailwind-css`, `vue`

Use the same canonical path template with `svg` as the format and extension.

---

## Legacy URLs

The original uncategorized 48px PNG and SVG URLs remain available for the initial 20-brand collection:

```text
src/{theme}/png/48px/{variant}/{brand}.png
src/{theme}/svg/{variant}/{brand}.svg
```

These paths are retained for backward compatibility. New integrations should use the categorized canonical structure.

---

Brand names and logos are trademarks of their respective owners. Inclusion here does not imply endorsement or affiliation.
