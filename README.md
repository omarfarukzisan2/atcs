# Asraf Tailors & Cloth Store

Production-ready Next.js 16 site (App Router, TypeScript, Tailwind CSS v4). Business copy, phone, address, map embed, pricing hints, and offers live in **`lib/site-config.ts`**—edit that file instead of hunting through components.

- **`tailwind.config.js`** — content paths for Tailwind (used with `@config` in `app/globals.css`).

## Scripts

```bash
npm install
npm run dev      # http://localhost:3000
npm run build
npm run lint
```

## Deploy on Vercel

1. Push this folder to GitHub (or GitLab / Bitbucket).
2. Import the repo in [Vercel](https://vercel.com/new): framework **Next.js**, root directory the project folder, build command `npm run build`, output default.
3. After deploy, set **`siteConfig.siteUrl`** in `lib/site-config.ts` to your real URL (or custom domain) so Open Graph and `metadataBase` stay correct.

## Manual steps after launch

- **Google Maps:** In Google Maps → your place → **Share** → **Embed a map**, copy the iframe `src` and paste it into `mapEmbedUrl` in `lib/site-config.ts`.
- **Images:** Replace placeholders under `public/images/gallery/` and `public/images/cloth/`, then update paths in `app/gallery/page.tsx` and `app/cloth/page.tsx` if filenames change.
- **Pricing & offers:** Adjust `pricing`, `offer`, and `delivery` in `lib/site-config.ts` seasonally.
- **Email:** Replace the placeholder `contact@asraftailors.example` in `lib/site-config.ts` if you use the mailto link on the contact page.

## Out of scope (future)

Order tracking, saved measurements in a database, and SMS notifications are not implemented; add a backend or third-party services when you need them.
