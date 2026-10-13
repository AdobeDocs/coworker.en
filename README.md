# CX Enterprise Coworker documentation

Source for the Adobe CX Enterprise Coworker documentation set.

## Publishing configuration

Use the shared article validation and mirroring workflows in `.github/workflows/`.
The validation workflow runs for pull requests and pushes to `main`.
The mirroring workflow runs when you push to `main`.

Use `markdownlint_custom.json` for Markdown rule overrides and `linkcheckexclude.json` for example URL exclusions.
The `pipeline.opts` file follows the link checking configuration in `cx-enterprise-ai.en`.
Add URL redirects to `redirects.csv` using the `source,dest` columns.
