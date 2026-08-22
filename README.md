# AlgoArena

AlgoArena is a full-stack coding practice platform for solving programming problems, participating in contests, reviewing submissions, and learning through editorials and AI-assisted doubt solving.

> **Showcase repository:** The production source code is intentionally kept private. This repository contains product documentation and a high-level architecture overview only.

## Preview

![AlgoArena AI-powered DSA learning platform landing page](assets/screenshots/landing-page.png)

## Highlights

- Problem solving with run and submit flows powered by Judge0
- Visible and hidden test cases with submission history
- Live, upcoming, and completed coding contests
- Score-based leaderboards with tie-time ranking
- Email/password and Google authentication
- Role-based admin tools for problems, contests, and video editorials
- Premium membership flow with verified Razorpay payments
- Cloudinary-hosted video editorials
- AI-assisted doubt solving with Gemini
- Personal dashboard with progress and activity insights

## Product Tour

<table>
  <tr>
    <td width="50%">
      <img src="assets/screenshots/practice-problems.png" alt="AlgoArena practice problem library" />
      <p align="center"><strong>Practice problem library</strong></p>
    </td>
    <td width="50%">
      <img src="assets/screenshots/code-editor.png" alt="AlgoArena problem workspace and code editor" />
      <p align="center"><strong>Problem workspace and code editor</strong></p>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <img src="assets/screenshots/contest-arena.png" alt="AlgoArena coding contest arena" />
      <p align="center"><strong>Coding contest arena</strong></p>
    </td>
    <td width="50%">
      <img src="assets/screenshots/dashboard.png" alt="AlgoArena user progress dashboard" />
      <p align="center"><strong>Progress dashboard</strong></p>
    </td>
  </tr>
</table>

## Technology

| Area | Technologies |
| --- | --- |
| Frontend | React, Vite, Redux Toolkit, Tailwind CSS, DaisyUI, Monaco Editor |
| Backend | Node.js, Express, MongoDB, Mongoose |
| Authentication | JWT, bcrypt, Google OAuth |
| Execution | Judge0 via RapidAPI |
| Infrastructure | Redis, Cloudinary |
| Integrations | Razorpay, Gemini |

## How the platform works

```mermaid
flowchart LR
    U[User] --> W[React web app]
    W --> A[Express API]
    A --> D[(MongoDB)]
    A --> R[(Redis)]
    A --> J[Judge0]
    A --> C[Cloudinary]
    A --> P[Razorpay]
    A --> G[Gemini]
```

More detail is available in [Architecture](docs/ARCHITECTURE.md) and [Product Features](docs/FEATURES.md).

## Repository policy

This public repository is intended for portfolio and product demonstration purposes. It does **not** contain:

- frontend or backend source code
- environment variables, credentials, or deployment configuration
- GitHub Actions workflows
- database schemas or production infrastructure details

The application source and deployment pipeline are maintained in a separate private repository.

## Ownership

Copyright © 2026 Raghav Maheshwari. All rights reserved.

No license is granted to copy, modify, redistribute, sublicense, or use the private AlgoArena implementation. See [COPYRIGHT.md](COPYRIGHT.md).
