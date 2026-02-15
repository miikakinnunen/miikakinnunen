## Introduction

Projects I have developed are currently hosted on a private Gitea instance. I am in the process of migrating and streamlining these for GitHub to ensure they are in a suitable form for public showcase.

Below are nutshell versions of my work that are already migrated. While source code repositories are currently private for privacy reasons, i am happy to provide access upon request.

## Technical Skills

- **Languages:** Python, JavaScript (ES6+), TypeScript, Go, SQL
- **Backend:** Django, Node.js (Express), RESTful API Design, WebSockets, Celery
- **Frontend:** Vue.js, React,  SPAs, State Management, HTML5, CSS3, Tailwind CSS
- **Databases & Messaging:** PostgreSQL, MySQL, SQLite, RabbitMQ, Relational Data Modeling
- **DevOps & Platform:** Docker, CI/CD pipelines, Linux, Kubernetes, Helm, ArgoCD, Vagrant, Ansible
- **Quality & Metrics:** Prometheus, Grafana, ELK, PyTest, Jest, k6, Locust
- **Security & Identity:** JWT (refresh token rotation), TLS, OAuth2, 2FA, RBAC, rate limiting


## Projects

### E-commerce platform

A production-style e-commerce platform designed and implemented from the ground up. It models a production-style commerce system, covering secure authentication, catalog management, transactional checkout, asynchronous payment processing, administrative tooling, and operational considerations such as background task processing and load testing.

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
- Stripe payment integration using Payment Intents (sandbox)
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




