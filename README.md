# AES Partner Connect — Portfolio Collaboration Portal

A responsive, **unofficial fictional demonstration** of a cross-portfolio partner portal for engineered-solutions programs, suitable for GitHub Pages. This is a separate public-facing prototype complementary to an internal project-controls dashboard.

## Included

- Home dashboard with featured projects, milestones, and portfolio overview.
- Searchable portfolio directory and detailed project views.
- Collaboration and support request intake with locally generated reference numbers.
- Request lookup for locally created browser drafts and **fictional** project status lookup.
- Searchable knowledge hub with six project controls guides.
- Collaboration working-group descriptions and locally saved personal notes.
- Rule-based AES assistant: sample project lookup, request status, intake help, EVM FAQs, and navigation guidance.
- Local request JSON export and a browser reset option.
- Responsive interface and GitHub Actions workflow for Pages deployment.

## Quick start

Open `index.html` in a modern browser. No build tools, dependencies, keys, or server required.

## GitHub Pages deployment

1. Create a repository, e.g. `aes-partner-connect`.
2. Upload **all** files, including `.github/workflows/deploy.yml`, and push to `main`.
3. In repository **Settings → Pages → Build and deployment**, select **GitHub Actions**.
4. Wait for the `Deploy GitHub Pages` workflow to complete.
5. Visit `https://YOUR-USERNAME.github.io/aes-partner-connect/` (adjust name as needed).

## Critical limitations / data handling

- **Not affiliated with, sponsored by, or connected to Westinghouse.** All names and project figures are fabricated for demonstration.
- **No backend.** Intake does *not* send requests anywhere; the status lifecycle is *not* shared or updated by a team.
- New requests and collaboration notes are stored via browser `localStorage` on the current device only. Clearing browser data removes them. JSON export downloads a local file. Shared/team-visible intake is not provided.
- **No real AI model.** The assistant uses local deterministic JavaScript logic, not an LLM. It cannot access internal tools, P6, SAP, email, or external knowledge.
- **No login or permissions.** GitHub Pages is public by default. Do not enter passwords, customer data, sensitive internal information, controlled technical data, or confidential project details.
- No third-party dependencies, API calls, or tracking are used.
- Do not treat fictional project status, schedule, budgets, owners, or milestones as actual records.

## Production architecture next steps

For operational use, put an authenticated gateway and API behind the portal (e.g. Azure Static Web Apps + Microsoft Entra ID + Azure Functions/.NET), add a managed database and workflow routing, provision role-based access and audit logs, and connect approved portfolio data sources (P6, SAP, project management systems, knowledge repository). Introduce a server-side agent with retrieval from approved documents, explicit per-user authorization, prompt-injection defenses, safety review, and action approval. Host sensitive environments using approved enterprise infrastructure, not a public Pages repo.

## File map

- `index.html` — screens and markup
- `styles.css` — responsive layout
- `app.js` — demo data, local forms/status/knowledge and assistant
- `.github/workflows/deploy.yml` — Pages deployment

## Customization

Modify `projects`, `guides`, and `groups` at the top of `app.js` to replace demo content with content approved for public distribution. Keep proper security controls for any operational data.
