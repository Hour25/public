<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/f3496a33-46dc-4481-9169-027892e31724" />


# Mind Guard

## Architecture & Security Overview

### Runtime & Frameworks

* TypeScript; Bun/Node.js runtime
* Fastify APIs (CORS, Helmet, cookies, form parsing)
* React + React Router
* Storybook (UI component library & docs)

### Data

* PostgreSQL (primary on AWS RDS; managed Postgres where appropriate, e.g., Supabase)
* Knex for migrations/query builder

### Infrastructure & Hosting

* **Primary:** AWS (EC2 for compute, RDS for Postgres)
* **Frontend delivery:** Vercel (global edge)
* **Staging/experiments:** Render

### CI/CD & Quality

* GitHub Actions pipelines (build, test, deploy)
* Testing: Jest, React Testing Library, Cypress
* Tooling: ESLint, Prettier, TypeScript compiler

### Security

* OAuth 2.0, JWT-based auth
* Passwords salted & hashed (bcrypt)
* Encryption in transit (TLS 1.2+) and at rest (AWS-managed keys)
* CSP and security headers via Helmet
* XSS/CSRF protections as applicable
