# Architecture Overview

AlgoArena uses a React single-page application backed by a Node.js and Express API. Persistent application data is stored in MongoDB, while Redis supports short-lived authentication and session-related state.

## Main components

```mermaid
flowchart TB
    Client[React client]
    API[Express API]
    Auth[Authentication and authorization]
    Problems[Problems and submissions]
    Contests[Contests and leaderboards]
    Content[Video editorials]
    Billing[Premium membership]
    Assistant[AI doubt assistant]

    Client --> API
    API --> Auth
    API --> Problems
    API --> Contests
    API --> Content
    API --> Billing
    API --> Assistant

    Auth --> Mongo[(MongoDB)]
    Auth --> Redis[(Redis)]
    Problems --> Mongo
    Problems --> Judge0[Judge0]
    Contests --> Mongo
    Content --> Cloudinary[Cloudinary]
    Billing --> Razorpay[Razorpay]
    Assistant --> Gemini[Gemini]
```

## Design notes

- Authentication supports standard credentials and Google OAuth.
- User and administrator permissions are enforced at the API boundary.
- Code execution is delegated to Judge0; application services manage validation and result persistence.
- Contest submissions are separated from normal practice activity for scoring and history.
- Payment verification happens server-side before premium access is granted.
- Video assets are stored outside the application server and linked to problem metadata.

This document intentionally describes the system at a high level and excludes implementation details, private endpoints, credentials, and deployment configuration.

