# Deployment Handoff for Devin

## Purpose of this deployment

Deploy or publish the Markdown civic-research deliverable so reviewers and
downstream agents can use it as the master task definition for mapping North
Carolina elected-office authority and affected constituencies.

The current deliverable focuses on the North Carolina Council of State and
creates a reusable schema for later expansion to federal, state legislative,
judicial, county, municipal, school board, sheriff, and special district offices.

Primary artifact:

- `docs/nc-council-of-state-office-impact-map.md`

## Current repository state

- Branch: `cursor/nc-council-state-md-d3d5`
- Base branch: `main`
- Current change surface versus `origin/main`: one added Markdown file
- No application code was changed
- No package manager manifest is present
- No repository-defined install command is present
- No repository-defined build command is present
- No repository-defined deploy command is present

## Deployment requirements

### Required

1. Preserve the Markdown file path:
   `docs/nc-council-of-state-office-impact-map.md`.
2. Ensure the published environment can render or expose Markdown files.
3. Keep the official source URLs intact because they are part of the research
   handoff and verification chain.
4. Publish from the pushed branch or merge the branch into the deployment branch
   after normal review.
5. If a static-site generator is introduced, confirm it does not rewrite
   headings, tables, or source URLs in the Markdown document.

### Not required

1. No dependency installation is required for the current deliverable.
2. No frontend build is required for the current deliverable.
3. No database migration is required.
4. No environment variables are required.
5. No server process is required.

## Recommended deployment options

Because this repository currently behaves as a static HTML repository with no
install/build/deploy configuration, use one of these paths:

1. **Documentation-only review path**
   - Treat the Markdown file as the deployment artifact.
   - Review it directly in GitHub or any Markdown renderer.

2. **Static hosting path**
   - Configure a static host such as GitHub Pages, Netlify, Vercel static
     hosting, S3/static website hosting, or an existing web server.
   - Publish the repository root or a documentation directory.
   - Confirm the Markdown file is reachable or rendered.

3. **Future app integration path**
   - Convert the Markdown content into a page in the existing static HTML
     dashboard.
   - Add navigation from the existing dashboard only after deciding where civic
     research documents should live in the product.

## Predicted collisions and risks

| Collision or risk | Likelihood | Impact | Why it matters | Mitigation |
| --- | --- | --- | --- | --- |
| Another branch also creates `docs/` | Medium | Low to medium | This branch creates the first `docs/` directory. A parallel documentation branch could create the same path or competing structure. | Rebase before merge and keep this file path stable. |
| A deployment expects only `.html` files at repo root | Medium | Medium | The current repo is mostly static HTML; Markdown may not be rendered by a plain static host. | Either expose the raw Markdown, configure Markdown rendering, or convert to HTML later. |
| A static-site generator is added later | Low to medium | Medium | Some generators require front matter or may ignore files outside configured content directories. | Add generator-specific metadata only after choosing the generator. |
| Source URLs become stale | Medium | Medium | The document is source-backed and government pages can move. | Preserve `last_verified_date` fields when converting to structured data and schedule periodic link checks. |
| Legal authority is treated as final legal advice | Medium | High | The document is a research/task map, not a legal opinion. | Keep the document framed as a source-backed research specification and verify statutes before operational use. |
| Office authority changes after statutory reorganization | Medium | High | NC agencies and boards can be reorganized by statute or budget bills. | Add a current-law verification step before production use. |
| PR or branch conflict with edits to the same Markdown file | Low | Medium | Only one file carries most of the deliverable. | Coordinate edits or split future work by office-specific files. |
| Deployment branch is protected | Unknown | Medium | Direct deployment may require review, status checks, or merge permissions. | Use the normal repository review and merge process. |
| Devin expects executable deploy instructions | Medium | Low | There is no executable deploy pipeline in this repo. | Tell Devin the deployable artifact is documentation-only unless a hosting target is selected. |

## Suggested message to Devin

Use this summary if handing the work to Devin:

> Purpose: publish the Markdown research/task specification for mapping North
> Carolina Council of State offices and affected voter constituencies. The
> deployable artifact is `docs/nc-council-of-state-office-impact-map.md`.
> This branch has no install/build/deploy pipeline and changes only
> documentation. Treat deployment as documentation publication unless a static
> hosting target is selected. Main collision risks are Markdown rendering on a
> static HTML-only host, future branches also creating `docs/`, and current-law
> changes in North Carolina office authority.

## Verification already performed

- `git fetch origin main`
- `git diff --name-status origin/main...HEAD`
- Branch delta showed one added file before this handoff:
  `docs/nc-council-of-state-office-impact-map.md`
- `git status --short --branch`

## Next decision required

Choose the deployment target:

1. Keep as GitHub-rendered Markdown documentation.
2. Publish via static hosting.
3. Convert into an HTML dashboard page.
4. Convert into structured data for an application or database.
