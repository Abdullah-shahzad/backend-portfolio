# Muhammad Abdullah — Developer Portfolio

Static React + TypeScript portfolio built with Vite, Tailwind CSS, Lucide icons and locally bundled Manrope. Four sections: About, Resume, Projects and Contact. All content is local; no backend, tracking, contact-form service or runtime API is required.

## Local development

Use Node.js 22.12+ (tested with Node 24) and npm.

```sh
npm ci
npm run dev
```

Open the URL printed by Vite (normally http://127.0.0.1:5173).

```sh
npm run typecheck
npm run lint
npm run build
npm run preview
```

The production output is `dist/`. Never publish the whole workspace: it contains the original reference files.

## Edit content

- `src/data/profile.ts`: identity, contact links, introduction, services and grouped skills.
- `src/data/experience.ts`: employment and education with original resume dates.
- `src/data/projects.ts`: categories, descriptions, verified links and detailed source caveats.
- `src/components/`: sidebar and section components.
- `src/styles.css`: responsive layout, semantic surface colors and interaction states.
- `public/images/`: original SVG concept illustrations, not screenshots of the actual applications.
- `public/resume/Muhammad-Abdullah-Resume.docx`: byte-for-byte copy of the supplied resume. Original input is untouched.

Navigation uses URL hashes and supports back/forward and direct links (for example `/#projects`). Project filters expose selected state to assistive technology. Contacts collapse below desktop widths. The site has visible keyboard focus, a skip link and reduced-motion support. Legacy `/#portfolio` links redirect to `/#projects`; `/#blog` links redirect to About.

## Content verification and outstanding inputs

The supplied resume is the source for identity, contact details, professional history, dates, projects and education. LinkedIn's URL matches the resume but automated profile access returned HTTP 999; its contents were not verified. Postman is included because it was explicitly specified in the user brief.

Public GitHub API verification on 16 October 2026 confirmed these repositories:

- https://github.com/Abdullah-shahzad/Stock_Exchange
- https://github.com/Abdullah-shahzad/Stock_exchange_FastAPI
- https://github.com/Abdullah-shahzad/Stock_exchange_Golang_project
- https://github.com/Abdullah-shahzad/spotify-hit-song-predictor

The Django stock README lists authentication as pending, while the resume describes JWT integration across services. Project details preserve this distinction. The FastAPI README is minimal and the Golang repository has no root README; no extra implementation claims were inferred. The song-predictor README describes PostgreSQL and notes that trained model weights and data are excluded; the resume also lists SQLite. No working live demo is claimed.

SmartStudy and AirSenseAI were not found in the account's public repositories. SmartStudy's features come from the resume. AirSenseAI's title and intended SHAP / LangGraph / forecasting direction come from the brief and are explicitly marked as unverified. Supply their exact repositories before adding implementation claims or links. No photo was provided, so an original initials monogram is used.

## Deploy to Vercel

1. Push the source to your Git repository, excluding node_modules and dist. You may also exclude the supplied reference HTML/assets and original source resume from the repository; the download copy in public/resume must remain.
2. Import that repository into Vercel and select the Vite framework preset.
3. Set install command to `npm ci`, build command to `npm run build`, and output directory to `dist`.
4. Deploy. No environment variables or SPA rewrite rules are needed for hash navigation.
5. Once a real domain is assigned, add an absolute canonical URL and `og:url` to index.html. Add a domain-specific sitemap.xml and its URL to robots.txt. No invented production domain is embedded.

This delivery is local and has not been deployed. The current Open Graph title and description are ready; add an absolute social-preview image URL after hosting is configured.

See IMPLEMENTATION.md for reference analysis and component requirements.

## Validation completed

- TypeScript and ESLint passed; Vite production build passed.
- Visually inspected desktop (1265px), tablet (768px), and mobile (390px) layouts and compared the desktop composition with the live reference.
- Exercised all four navigation sections, mobile contact expansion, all project category filters, and project-detail disclosure in the browser.
- Resume endpoint returned HTTP 200; downloaded bytes match the untouched original.
- Production text/assets checked for original reference identity; none found.
- LinkedIn profile contents and live project deployments remain unverified. No full automated WCAG audit was performed.
