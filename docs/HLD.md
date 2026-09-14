# High-Level Design (HLD)
**hackbca-example-frontend**

**Last Updated:** 2026-09-14  
**Doc Owner:** Architecture Team  
**Repository:** https://github.com/AryanBhanushali/hackbca-example-frontend

---

## Executive Overview

**hackbca-example-frontend** is a React-based web application that serves as the primary user-facing interface for hackBCA, an educational hackathon event. The application enables event participants to authenticate, browse project proposals, create new projects, collaborate with other participants, and manage project metadata.

The frontend is a single-page application (SPA) that communicates exclusively with a backend API server (via configurable `REACT_APP_API_URL`). All authentication is delegated to the backend via Google OAuth 2.0 flow. The UI is styled using Tailwind CSS with a custom brand theme, and navigation is handled by React Router v6.

**Key characteristics:**
- **Scope:** Frontend only; all business logic and data persistence handled by backend
- **Technology:** React 17, Node.js ecosystem (npm)
- **Authentication:** Google OAuth (backend-delegated)
- **Deployment:** Static build artifact suitable for CDN or static hosting
- **User Base:** hackBCA event participants (students and organizers)

## Objective

This frontend application exists to:

1. **Reduce barriers to participation** — Provide an intuitive, branded interface for hackBCA attendees to discover and propose projects
2. **Enable collaboration** — Allow multiple participants to co-own and co-develop project proposals
3. **Centralize visibility** — Aggregate project information in one place, accessible to all attendees
4. **Facilitate authentication** — Leverage Google OAuth for frictionless sign-in without managing credentials
5. **Support event management** — Enable organizers (authenticated users) to view, edit, and manage projects

**Out of scope:**
- Backend API logic, database design, or server infrastructure
- User management or role definitions (delegated to backend)
- Scheduling or calendar functionality beyond date/time selection in forms
- Real-time collaboration or live updates (polling or WebSocket not implemented)
