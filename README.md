# Luke M. Hebert — personal academic website

A responsive, dependency-free HTML/CSS portfolio. No build step, JavaScript, tracking, or external fonts. Native expandable project details work without JavaScript. All bracketed biography, education, skills, and project text is placeholder content, not a claim about Luke.

## Preview

Open `index.html` in your browser. All asset paths are relative, so the site works at either a GitHub Pages repository path or a custom domain. Project details expand when selected; navigation links jump to each section.

## Customize before publishing

1. Edit the bracketed text in `index.html`, including the introduction, profile, resume, project cards, and personal interests. Remove unused entries.
2. Replace `your-email@example.com`, `YOUR-LINKEDIN-USERNAME`, and `YOUR-GITHUB-USERNAME` with your real contact details. Placeholder profile URLs are not live personal profiles.
3. Your original PDF is included at `assets/Luke-M-Hebert-Resume.pdf`. The Resume section embeds this PDF directly and provides open/download links. No HTML resume is generated or required. Replace this file with a newer PDF using the same filename to update the viewer and download.
4. For each project, replace the sample topics and details, then add actual links inside its `<details>`, for example `<a href="https://github.com/YOUR-USERNAME/YOUR-REPO">View source code</a>`. Duplicate an entire `<article class="project-card">` to add a card.
5. Edit the page title and meta description. Adjust the CSS variables at the top of `styles.css` to customize colors. Change the initials in `assets/favicon.svg` and the header if desired.
6. Replace `www.example.com` in `CNAME` with a domain you own, or **delete CNAME if you are using only the default github.io address**. The supplied CNAME is a placeholder, not a configured domain.

## Publish on GitHub Pages

1. Create a GitHub repository. For a main personal site, name it `YOUR-USERNAME.github.io`; another repository name also works, at `https://YOUR-USERNAME.github.io/REPOSITORY/`.
2. Upload the **contents of this folder** to the root of your repository's `main` branch. Include `.nojekyll` and, only after replacement, `CNAME`. Do not upload the enclosing folder or ZIP as the site itself.
3. Open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**. No Actions workflow or Jekyll configuration is needed for this setup.
4. Wait for the Pages deployment to finish and open the URL shown in Pages settings.

## Custom domain

Recommended example: use `www.yourdomain.com` as the primary address.

1. Verify ownership in your GitHub account’s **Settings → Pages** using GitHub’s supplied TXT record. Keep that TXT record in DNS.
2. Set `CNAME` to exactly `www.yourdomain.com` on one line, without `https://`, paths, or comments. In the repository’s **Settings → Pages → Custom domain**, enter the same hostname and save it. Configure the domain in GitHub before pointing DNS at GitHub Pages.
3. At your DNS provider, add a **CNAME** record with host `www` and target `YOUR-USERNAME.github.io` (no protocol or repository path).
4. To support the root domain and redirect it to `www`, set these **A** records for host `@`:

   | Type | Host | Value |
   | --- | --- | --- |
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |

   For an apex-primary site instead, put `yourdomain.com` in CNAME and GitHub settings; retain the apex A records and `www` CNAME. GitHub handles the alternate-host redirect when both are configured correctly. Your provider may offer ALIAS/ANAME as an alternative; use the official guide below for that setup and optional IPv6 records.
5. Remove conflicting records for the same web hostname; preserve unrelated mail and verification records. Avoid wildcard DNS records. DNS changes can take up to 24 hours.
6. After GitHub’s DNS check and certificate provisioning succeed, enable **Enforce HTTPS** in Pages settings. Check both the apex and `www` addresses.

## Accessibility and checks

Semantic landmarks, heading hierarchy, a keyboard skip link, visible focus indicators, native disclosure controls, responsive layouts, and reduced-motion support are included. Navigation remains visible on small screens. Gold is used as an accent or against navy, rather than small gold text on white.

Before sharing, check phone and desktop layouts, 200% zoom, keyboard navigation, all contact/project links, and the resume download. Search for `[` and `YOUR-` to locate unfinished content. No browser-based accessibility audit is implied.

## Design references

The university palette uses Notre Dame Blue `#0c2340`, Gold `#ae9142`, Medium Blue `#143865`, and Light Sky Blue `#edf2f9`, from [Notre Dame’s official university color guide](https://onmessage.nd.edu/university-branding/colors/). Typography uses locally available Georgia and system sans-serif. The LMH initials are personal branding; no university logo or seal is included. This is an independent personal site.

Deployment references (checked September 2026):
- [Managing a GitHub Pages custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
- [Verifying your custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages)
- [Securing GitHub Pages with HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)



