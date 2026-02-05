# Harmonic API Documentation — Agent Instructions

## Project overview

This is the Harmonic API documentation site, built with Mintlify. It documents the REST API and GraphQL endpoint for Harmonic's startup intelligence platform.

- **Base URL:** `https://api.harmonic.ai/`
- **GraphQL:** `https://api.harmonic.ai/graphql`
- **Auth:** API key via `apikey` header or query parameter
- **Console:** `https://console.harmonic.ai`

## Mintlify basics

- Configuration lives in `docs.json` — check it before making structural changes
- Use MDX format for documentation pages
- Run `mint dev` locally to preview changes before committing
- Run `mint broken-links` to check for broken links

## Style and formatting

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- When referencing UI elements, use bold: Click **Settings**
- Use code formatting for: file names, commands, paths, endpoints, parameters, and code references
- Always show both `curl` examples with query parameter auth and header auth where relevant

## API documentation conventions

- Every endpoint page should include: HTTP method, path, description, parameters, and example request/response
- Use `<ParamField>` components for parameter documentation
- Use `<CodeGroup>` for showing multiple code examples (e.g., curl, Python, JavaScript)
- Mark deprecated endpoints clearly with a `<Warning>` callout
- Mark GraphQL-only endpoints with an `<Info>` callout
- Mark paid add-on features with a `<Note>` callout

## Content structure

- Add frontmatter (title, description) to every page
- Use `sidebarTitle` in frontmatter if the nav title should differ from the page title
- Include introductory context before diving into endpoint details
- Group related endpoints on the same page (e.g., all Company Lists endpoints together)

## What to avoid

- Don't edit `docs.json` without understanding the navigation structure
- Don't remove existing pages without checking for inbound links
- Don't use HTML when an MDX component exists for the same purpose
- Don't add pages to navigation that don't exist yet
- Don't expose internal/private API details (Firebase auth, internal endpoints)
