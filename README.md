## Introduction

Projects I have developed are currently hosted on a private Gitea instance. I am in the process of migrating and streamlining these for GitHub to ensure they are in a suitable form for public showcase.

Below is a brief overview of selected projects that have already been migrated. While source code repositories are currently private for privacy reasons, i am happy to provide access upon request.

## Technical Skills

- **Languages:** Python, JavaScript (ES6+), TypeScript, Go, SQL
- **Backend:** Django, Node.js (Express), RESTful API Design, WebSockets, Celery, Redis
- **Frontend:** Vue.js, React,  SPAs, State Management, HTML5, CSS3, Tailwind CSS
- **Databases & Messaging:** PostgreSQL, MySQL, SQLite, RabbitMQ, Relational Data Modeling
- **DevOps & Platform:** Docker, Infrastructure as Code (IaC), Nginx, CI/CD pipelines, Linux, Kubernetes, Helm, ArgoCD, Vagrant, Ansible
- **Quality & Metrics:** Prometheus, Grafana, ELK, PyTest, Jest, k6, Locust
- **Security & Identity:** JWT (refresh token rotation), TLS, OAuth2, 2FA, RBAC, rate limiting


## Projects

### E-commerce platform

A full-stack e-commerce platform designed and implemented from the ground up, modeling a production-oriented commerce system with secure authentication, transactional checkout, asynchronous payment processing, and administrative tooling.

**Tech Stack**

* Backend: Python, Django
* Frontend: Vue, TypeScript, Tailwind CSS
* Database: PostgreSQL
* Infrastructure: Docker, RabbitMQ, Celery
* Testing: PyTest, k6

**Architectural Highlights**

- Stateless JWT authentication with access/refresh token rotation
- Optional 2FA and OAuth login
- ACID-compliant checkout flow with inventory reservation logic
- Stripe Payment Intents integration (Sandbox mode)
- Asynchronous webhook handling via RabbitMQ
- Background task processing with Celery
- Role-based access control (RBAC) for admin operations
- Rate limiting and input validation for API protection
- Observability stack using ELK

**Testing & Performance**

- Automated test coverage using PyTest
- Load testing using k6
- Transaction and stress testing for checkout consistency
- WCAG 2.1 Level A accessibility compliance
- SEO best practices applied

---

### Next to be migrated... 

### Interest-Based Geospatial Matching Platform

A full-stack recommendation system built with Go and React, connecting users through a custom weighted matching algorithm and geospatial proximity filtering. The platform combines strict access control, prioritized recommendations, and real-time communication.

**Tech Stack**

* Backend: Go, GraphQL (gqlgen), REST
* Frontend: React 18 (JavaScript)
* Database & Geospatial: PostgreSQL (earthdistance)
* Real-time: WebSockets (GraphQL subscriptions + chat channel)
* Security: JWT, brcypt

**Highlights**

- Hybrid API architecture (REST + GraphQL with subscriptions)
- Custom recommendation engine using 5+ weighted profile attributes
- Radius-based proximity filtering via PostgreSQL `earthdistance`
- WebSocket-powered real-time chat with typing indicators and unread tracking
- Connection-based profile visibility and strict authorization boundaries



