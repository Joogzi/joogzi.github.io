# Portfolio Projects

Two hackathon projects from our team, prepared as static demos for GitHub Pages:

- [NextTerm](https://joogzi.github.io/nextTerm/) — an education-focused course-scheduling concept; 2nd Place overall at the IBM-sponsored OSU AI Hackathon, February 2026.
- [Data I/O 2026](https://joogzi.github.io/dataio2026/) — a 3D campus energy visualizer; 1st Place in the Advanced Track at Data I/O, February 2026.

NextTerm uses a captured OSU course catalog with browser-local demo interactions. It does not call an AI service. The Data I/O visualizer serves its processed datasets and 3D assets directly.

## Deployment

The `Deploy portfolio projects` GitHub Actions workflow publishes the contents of `site/` after a push to `main`. GitHub Pages must use **GitHub Actions** as its source.

The source projects remain in `Joogzi/nextTerm` and `Joogzi/dataio-26`. To update the demos, keep both source checkouts in the same parent directory and run `node deploy/build-portfolio.mjs` from the NextTerm checkout with Bun on your PATH. The helper checks and builds both projects and prints a fresh release directory. Update the corresponding folders in this repository's `site/` directory with the release outputs, commit, and push.

Only compiled website files and display datasets are published here. The backend database and credentials are not included.
