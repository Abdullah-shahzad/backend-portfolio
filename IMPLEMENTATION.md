# Design analysis and implementation plan

The supplied reference is a personal portfolio, despite the extracted documentation-site classification. Its desktop composition uses a centered 1200px layout, 275px sticky profile panel, 25px gutter, 30px content padding, 20px panel corners, Manrope typography and a compact top-right navigation. Charcoal surfaces sit on a black background; gold is reserved for active navigation, icons and heading rules. Services form a two-column grid with 14px corners and subtle shadows. Mobile stacks the profile and content, with collapsible contacts.

Components: Sidebar, Skills, About, Resume, Projects, Contact, plus data modules. Navigation uses real hash links with browser history support. Project categories use pressed-state buttons. Native details elements expose project notes accessibly. No scraped JavaScript, portrait or personal branding is reused.

All interactions must support keyboard focus and 44px touch targets. Navigation must expose its active state; filters must expose selection. Cards without actions are static. Unverified project states must be explicit. Loading/error states are unnecessary for static content; font loading uses swap. Reduced-motion preference must disable animation. Long email addresses must wrap without clipping. At tablet widths the sidebar must stack; at mobile widths service/project grids must become one column.

Content: resume is the source of employment, dates and education. User brief supplies AirSenseAI's proposed direction only. Public repository verification is recorded in README. No proficiency scores or invented credentials.

QA: typecheck, lint, build, desktop/mobile inspection, navigation, filters, resume checksum, valid local assets, no original owner's content in production output.
