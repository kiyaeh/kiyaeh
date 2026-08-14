# Design — GitHub Profile README Upgrade

## Structure Overview

The upgraded README follows this top-to-bottom layout:

```
1. Hero Banner (capsule-render waving, larger, richer gradient)
2. Typing SVG (more lines, personality)
3. Social Badges Row (Email, LinkedIn, Portfolio, Twitter-placeholder, Views)
4. "Currently Building" Spotlight card
5. About Me (two-column emoji table)
6. The Arc — Architecture Timeline (enhanced Mermaid + narrative)
7. Tech Stack (tiered: Expert / Proficient / Exploring)
8. Flagship Projects (styled HTML table cards)
9. GitHub Stats Grid (2×2 layout)
10. Activity Graph
11. Contribution Snake
12. What I'm Exploring (progress-style badges)
13. Let's Collaborate (styled block + badges)
14. Beyond the Code
15. Footer (capsule-render + quote)
```

## Section Designs

### 1. Hero Banner
```
capsule-render:
  type: waving
  color: 0:0d1117,50:1e3c72,100:0f9b8e
  height: 250
  text: Ewnetu Tesfaye
  fontSize: 60
  desc: Kiyaeh • Full-Stack Engineer • Addis Ababa, Ethiopia
  animation: twinkling
```

### 2. Typing SVG
- Font: Fira Code
- Color: #2DD4BF
- Lines: 8 descriptive lines covering stack, current work, ambitions
- Width: 700

### 3. Social Badges
- style: for-the-badge
- Badges: Gmail, LinkedIn, Portfolio (netlify), GitHub, Profile Views (komarev)

### 4. Currently Building Spotlight
HTML table with teal left-border effect using a colored emoji bar:
```html
<table>
  <tr>
    <td>🟢 LIVE BUILD</td>
    <td><b>Learnova</b> — AI-powered EUEE prep platform...</td>
    <td>stack badges</td>
  </tr>
</table>
```

### 5. About Me Table
Two-column HTML table:
| Field | Value |
|---|---|
| 👤 Name | Ewnetu Tesfaye ("Kiyaeh") |
| 📍 Location | Addis Ababa, Ethiopia |
... etc

### 6. The Arc (Mermaid)
Enhanced flowchart LR with subgraphs per phase, status labels, and tech stacks inline. Styled with fill colors matching palette.

### 7. Tech Stack — Tiered Layout
Three tiers shown with section headers:

**🔴 Expert**
skillicons: ts, nestjs, react, nextjs, postgres, docker

**🟡 Proficient**  
skillicons: java, spring, mongodb, redis, rabbitmq, aws

**🟢 Exploring**
skillicons: py, elasticsearch, graphql, githubactions

### 8. Project Cards
HTML table with 3-column layout per card:
- Col 1: emoji + project name + status badge
- Col 2: description
- Col 3: stack badges (shields.io)

Status badges:
- 🟢 Active: `https://img.shields.io/badge/status-active-2DD4BF`
- 🧪 Experimental: `https://img.shields.io/badge/status-experimental-yellow`
- ✅ Shipped: `https://img.shields.io/badge/status-shipped-0f9b8e`

### 9. GitHub Stats — 2×2 Grid
```
[readme-stats card]     [top-langs card]
[streak-stats card]     [activity-graph]
```
All using tokyonight theme, hide_border=true, consistent height=180.

### 10. Activity Graph
`github-readme-activity-graph` with theme=tokyo-night, area=true, hide_border=true.

### 11. Snake
Framed in its own `<div align="center">` with a `### 🐍 Contribution Snake` header.

### 12. What I'm Exploring
Shields.io badges styled as progress indicators:
- `AI/ML Engineering` — 35%
- `Spring Cloud Depth` — 60%  
- `Elasticsearch Internals` — 55%
- `System Design Patterns` — 70%

### 13. Collaboration Block
capsule-render `rect` type divider above the section, then bullet list with shields.io topic badges.

### 14. Footer
capsule-render waving footer (reversed gradient from header) + italic quote.

## Color Palette Reference
| Token | Hex |
|---|---|
| Primary Teal | `#2DD4BF` |
| Dark Navy | `#1e3c72` |
| Mid Teal | `#0f9b8e` |
| Dark Green | `#134e4a` |
| Background | `#0d1117` |

## Widget URLs

| Widget | Base URL |
|---|---|
| capsule-render | `https://capsule-render.vercel.app/api` |
| readme-typing-svg | `https://readme-typing-svg.demolab.com/` |
| github-readme-stats | `https://github-readme-stats.vercel.app/api` |
| streak-stats | `https://streak-stats.demolab.com/` |
| activity-graph | `https://github-readme-activity-graph.vercel.app/graph` |
| trophies | `https://github-profile-trophy.vercel.app/` |
| skillicons | `https://skillicons.dev/icons` |
| shields.io | `https://img.shields.io/badge/` |
| komarev views | `https://komarev.com/ghpvc/` |
| snake | `https://raw.githubusercontent.com/kiyaeh/kiyaeh/output/github-contribution-grid-snake-dark.svg` |
