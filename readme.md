# Jenny Chen — Personal Website

A lightweight, responsive English-language personal website for Jenny Chen (Fangting Chen), focused on cross-border logistics, 3PL fulfilment, order management, customer/carrier coordination and Auckland-based New Zealand / global remote opportunities.

## Live website

- https://jennyc.pages.dev/
- Cloudflare account: 719919153@qq.com
- Cloudflare Pages project: `jennyc`, production branch: `main`
- Repository: https://github.com/yaohuangguan/jenny-website
- Local source on Windows: `E:\Coding\jenny-website`
- Stack: plain HTML, CSS and minimal vanilla JS; no runtime dependencies or paid services.

## Pages and assets

- `public/index.html` — landing page: About, Expertise, Experience, Contact.
- `public/resume.html?track=nz` — NZ-focused, print-friendly résumé.
- `public/resume.html?track=global` — global/remote-focused résumé.
- `public/Jenny_Chen_CV_NZ.pdf` and `public/Jenny_Chen_CV_Global.pdf` — downloadable CV files.
- `public/og.png` — social sharing preview; source art: `public/og.svg`.
- `public/_headers`, `robots.txt`, `sitemap.xml` — security headers and discoverability.

## Deployment

This Cloudflare Pages project uses **direct upload**, not Git integration. Pushing to GitHub does not automatically redeploy the website.

With Wrangler already logged into the Cloudflare account in WSL, from `E:\Coding` run:

```sh
wsl.exe -d Ubuntu -e bash -lc "npx --yes wrangler pages deploy jenny-website/public --project-name jennyc --branch main"
```

Verify `https://jennyc.pages.dev/` after publishing.

## Content maintenance

The content is based on Jenny's NZ and global logistics CVs. Do not invent metrics, employers, or certifications. The site is light-mode by default and designed for mobile.

After modifying `public/resume.html` or `public/resume.css`, re-export both PDF versions using Chrome's print-to-PDF or headless Chrome. After changing `public/og.svg`, regenerate `public/og.png`. Keep canonical URL, social preview, robots, sitemap and résumé links consistent.

**Privacy:** The downloadable CVs show Jenny's phone number and email address. The repository is public; please confirm with Jenny before sharing widely.
