# Client Bob Academy — Editing Guide

## Current design decisions

**Primary audience:** Customer engineers who are beginning to use IBM Bob.

**Website ownership:** A client-specific Bob Academy. Replace the generic name `Client Bob Academy` with the client or program name when ready.

**Learning outcomes:**
1. Understand Bob
2. Begin using Bob
3. Become productive in daily engineering work
4. Standardize team usage
5. Prepare for enterprise rollout

**Primary curriculum:** Beginner → advanced.

**Secondary ways to explore:** SDLC phase, role, use case, and product feature.

## Fastest edits

Open `index.html` in a text or code editor and search for `EDITABLE:`. These comments identify the main content blocks:

- Client academy name, audience, and hero positioning
- Primary academy outcomes
- Curriculum organization
- Role routes and recommendations
- Client-priority tutorial use cases
- Resource catalogue and metadata

## Rename the academy

Search for:

```text
Client Bob Academy
```

Replace it with a name such as:

```text
[Client Name] Bob Academy
```

Also update the page `<title>` and the footer language if needed.

## Content metadata model

Every main learning item should contain these four fields:

- **Source:** Content owner or origin, such as Official IBM Bob docs, IBM Developer, IBM/bob-demo GitHub, or an approved internal source.
- **Difficulty:** Beginner, Intermediate, Advanced, or a range.
- **Duration:** Expected learning time, not only the media runtime.
- **Prerequisites:** Required access, prior modules, tools, environments, or technical knowledge.

For client-owned content, also consider adding:

- Internal content owner
- Last-reviewed date
- Version
- Approval status

## Add a tutorial use case

Copy one `<article class="lab-card">...</article>` block inside the section with `id="tutorials"` and edit:

- Category label
- Tutorial title
- Description
- Source
- Difficulty
- Duration
- Prerequisites
- Role tags
- Link

Example:

```html
<article class="lab-card">
  <span class="lab-duration">Modernization</span>
  <h3>Your tutorial title</h3>
  <p>Describe the outcome the learner will produce.</p>
  <dl class="content-meta compact">
    <div><dt>Source</dt><dd>Approved source</dd></div>
    <div><dt>Difficulty</dt><dd>Intermediate</dd></div>
    <div><dt>Duration</dt><dd>30 min</dd></div>
    <div><dt>Prerequisites</dt><dd>Bob installed and sample repository</dd></div>
  </dl>
  <div class="tag-row">
    <span class="tag">Software Engineer</span>
    <span class="tag">Modernization</span>
  </div>
  <a href="YOUR_LINK" target="_blank" rel="noopener">Open tutorial →</a>
</article>
```

## Add a resource-library item

Copy one `<article class="resource-card">...</article>` block inside `id="resource-grid"`.

Use one of these `data-category` values so filtering continues to work:

- `start`
- `workflow`
- `customize`
- `enterprise`
- `demo`

Add meaningful keywords to `data-search`, including applicable role, SDLC phase, use case, and feature names.

## Role structure

The current routes are:

- Software Engineer
- IBM Z / Legacy Engineer
- Business Analyst / Product / Design
- Architect / DevOps / Platform
- Engineering Leader / Enablement

The role tabs are recommendations only. The beginner-to-advanced path remains the primary curriculum.

## Client-specific content to add later

Recommended additions for a production client academy:

- Bob access and installation instructions for the client environment
- Approved repositories and sandbox guidance
- Client coding and architecture standards
- Client-specific AGENTS.md examples
- Approved modes, rules, skills, and MCP servers
- Support contacts and escalation process
- Security and data-handling requirements
- Learning completion criteria
- Internal demos and recordings
- Adoption and business-value measurement

## Publishing

The website is a single static HTML page and can be hosted on an internal portal, GitHub Pages, or static object storage. Test all external and internal links before publishing.
