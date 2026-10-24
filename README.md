# Mashal Olympics Sports Wear — Vercel-ready

TanStack Start + React + Tailwind site. Build target is already set to **Vercel** (`vite.config.ts` -> `nitro: { preset: "vercel" }`).

## Deploy on Vercel
1. Push this folder to a GitHub repo (or use `vercel` CLI).
2. Vercel -> **Add New Project** -> import the repo. Framework preset: **Other**. `vercel.json` already sets install/build commands.
3. Deploy. No environment variables needed.

Local: `npm install --legacy-peer-deps` then `npm run dev` (build: `npm run build`).

## Before going live — EDIT THESE
- **Photos**: the files in `src/assets/` (`hero.jpg`, `shorts.jpg`, `shirts.jpg`, `gym-wear.jpg`, `tracksuit.jpg`, `football-kit.jpg`, `taekwondo.jpg`, `wushu.jpg`, `karate.jpg`) and `mashal-logo.jpg` are **placeholders**. Replace them with your real photos/logo using the **same file names**.
- **Contact details**: `src/lib/site.ts` (WhatsApp number, email, Instagram). The Custom Order form opens WhatsApp with the filled inquiry.

## What changed
- Home hero is now a 3-slide banner (auto-play, Ken Burns zoom, typing headline, right-side rail with counter, slide bars, arrows and scroll hint). Everything else on the page is unchanged.
- Logo no longer depends on Lovable-only URLs.
- Contact form and footer social links now work.

## Troubleshooting: "Could not resolve entry for router entry: router"
This means `src/router.tsx` (or another file in `src/`) did not reach Vercel — usually an incomplete GitHub upload.
- Check on GitHub that `src/router.tsx`, `src/routeTree.gen.ts`, `src/start.ts` and `src/server.ts` exist.
- Upload with GitHub Desktop or `git push` (the web uploader has a 100-file limit). This zip has ~50 files, so a web upload also works if you drag the *contents* of the folder.
- In Vercel, Root Directory must be the folder that directly contains `package.json` and `src/`.
- Alternative without GitHub: run `npx vercel --prod` inside this folder.
