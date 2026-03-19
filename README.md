# 👋 Introduction

Projects I have developed are currently hosted on a private Gitea instance. I am in the process of migrating and streamlining these for GitHub to ensure they are in a suitable form for public showcase.

Below is a brief overview of selected projects that have already been migrated. While source code repositories are currently private for privacy reasons, i am happy to provide access upon request.

# 🛠️ Technical Skills

- **Languages:** Python, JavaScript (ES6+), TypeScript, Go, SQL
- **Backend:** Django, Node.js (Express), RESTful API Design, WebSockets, Celery, Redis
- **Frontend:** Vue.js, React,  SPAs, State Management, HTML5, CSS3, Tailwind CSS
- **Databases & Messaging:** PostgreSQL, MySQL, SQLite, RabbitMQ, Relational Data Modeling
- **DevOps & Platform:** Docker, Infrastructure as Code (IaC), Terraform, Ansible, Nginx, CI/CD pipelines, Linux, Kubernetes, AWS, Azure, Helm, ArgoCD, Vagrant
- **Quality & Metrics:** Prometheus, Grafana, ELK, PyTest, Jest, k6, Locust
- **Security & Identity:** JWT (refresh token rotation), TLS, OAuth2, 2FA, RBAC, rate limiting


# 🗂️ Projects

## 🛒 E-commerce platform

A full-stack e-commerce platform designed and implemented from the ground up, modeling a production-oriented commerce system with secure authentication, transactional checkout, asynchronous payment processing, and administrative tooling.

<details>
    <summary><strong>🗃️ Project ERD</strong></summary>
    <img src="./media/ERD.png">
</details>
<p>
<details>
    <summary><strong>🌐 Microsoft Azure Architecture</strong></summary>
    <img src="./media/architecture.svg">
</details>
<p>
<details>
    <summary><strong>📸 Click to open a few preview images</strong></summary>
    <img src="./media/entry_page.png" width="300" alt="Thumbnail" />
    <img src="./media/category_and_price_filtering.png" width="300" alt="Thumbnail" />
    <img src="./media/book_details_and_reviews.png" width="300" alt="Thumbnail" />
    <img src="./media/cart+cartcomponent+suggests.png" width="300" alt="Thumbnail" />
    <img src="./media/checkoutview.png" width="300" alt="Thumbnail" />
    <img src="./media/paymentpending.png" width="300" alt="Thumbnail" />
    <img src="./media/myorders.png" width="300" alt="Thumbnail" />
    <img src="./media/adminfeatures.png" width="300" alt="Thumbnail" />
    <img src="./media/admin_order_management.png" width="300" alt="Thumbnail" />
</details>
<p>


**Tech Stack**

* Backend: Python, Django
* Frontend: Vue, TypeScript, Tailwind CSS
* Database: PostgreSQL
* Infrastructure: Docker, RabbitMQ, Celery, Terraform
* Testing: PyTest, k6
<p>

**Architectural Highlights**

- Stateless JWT authentication with access/refresh token rotation
- Optional 2FA and OAuth login
- ACID-compliant checkout flow with inventory reservation logic
- Stripe Payment Intents integration (Sandbox mode)
- Asynchronous webhook handling via RabbitMQ
- Background task processing with Celery
- Role-based access control (RBAC) for admin operations
- Rate limiting and input validation for API protection
<p>

**Testing & Performance**

- Automated test coverage using PyTest
- Load testing using k6
- Transaction and stress testing for checkout consistency
- WCAG 2.1 Level A accessibility compliance
- SEO best practices applied
<p>

**Cloud Deployment — Microsoft Azure**

- Infrastructure provisioned with Terraform (IaC) across 10+ Azure resources
- Application Gateway (Standard_v2) for SSL termination and path-based routing
- Separated frontend VM (Nginx + built Vue) and backend VM (Nginx + Gunicorn + Django)
- Managed PostgreSQL Flexible Server in a private subnet with VNet integration
- Azure Cache for Redis via private endpoint — no public internet exposure
- Azure Blob Storage for media files via django-storages
- Dedicated gateway subnet isolating Application Gateway from VM traffic
- Docker Compose orchestrating five containers on the backend VM
- Multi-stage frontend Dockerfile — Node builds Vue to static files, Nginx serves them



---

## 🗺️ Interest-Based Geospatial Matching Platform

A full-stack recommendation system built with Go and React, connecting users through a custom weighted matching algorithm and geospatial proximity filtering. The platform combines strict access control, prioritized recommendations, and real-time communication.

<details>
    <summary><strong>📸 Click to open a few preview images</strong></summary>
    <img src="./media/gm1.png" width="300" alt="Thumbnail" />
    <img src="./media/gm2.png" width="300" alt="Thumbnail" />
    <img src="./media/gm3.png" width="300" alt="Thumbnail" />
    <img src="./media/gm4.png" width="300" alt="Thumbnail" />
    <img src="./media/gm5.png" width="300" alt="Thumbnail" />
    <img src="./media/gm6.png" width="300" alt="Thumbnail" />
    <img src="./media/gm7.png" width="300" alt="Thumbnail" />
    <img src="./media/gm8.png" width="300" alt="Thumbnail" />
    <img src="./media/gm9.png" width="300" alt="Thumbnail" />
</details>
<p></p>

**Tech Stack**

* Backend: Go, GraphQL
* Frontend: React (JavaScript)
* Database: PostgreSQL with `cube` + `earthdistance` extensions
* Real-time: WebSockets (GraphQL subscriptions + chat channel)
* Security: JWT, brcrypt
* Containerization: Docker + Docker Compose
<p>

**Highlights**

- Hybrid API architecture (REST + GraphQL with subscriptions)
- Custom recommendation engine using 5+ weighted profile attributes
- Radius-based proximity filtering via PostgreSQL `earthdistance`
- WebSocket-powered real-time chat with typing indicators and unread tracking
- Connection-based profile visibility and strict authorization boundaries
- Accessibility practices applied throughout the UI


---

## ⚙️ DevOps Infrastructure Project

This project simulates a real-world DevOps environment built from the ground up — from bare metal virtualization to a fully automated CI/CD pipeline with observability and container orchestration. Rather than focusing on a single application, the core value of this project lies in the **infrastructure, automation, and operational practices** surrounding it.

The project was completed in total of **six phases**, each building on the last.

**Tech Stack Summary** *(see project details below for more detail)*

| Category | Tools |
|----------|-------|
| Provisioning | Vagrant, Ansible |
| Virtualization | VirtualBox |
| OS | Ubuntu (Linux) |
| Containerization | Docker |
| Container Registry | Docker Hub |
| CI/CD | Drone CI, Gitea |
| Package Management | Helm |
| GitOps | ArgoCD, ArgoCD Image Updater, Argo Rollouts |
| Security | UFW, Fail2Ban, Trivy, SSH hardening |
| Performance Testing | Artillery, Locust |
| Monitoring | Prometheus, Grafana, Alertmanager |
| Logging | ELK Stack (Phases 2-3), EFK Stack (Phases 4-5), Loki, Promtail (Phase 6) |
| Orchestration | Kubernetes (Minikube) |
| Cloud Platforms | AWS, GCP (cost analysis) |

--- 

### 📂 Project details

**Click to open** the architecture pictures and full breakdown of phases.
<details>
    <summary><strong>📐 VM Architecture (Phases 1-3)</strong></summary>
    <img src="./media/VM-arch.png"  />
</details>
<p>
<details>
    <summary><strong>☸️ K8s Architecture (Phases 4-5)</strong></summary>
    <img src="./media/k8s-arch.png"  />
</details>
<p>
<details>
    <summary><strong>📋 Phases 1-6 Breakdown</strong></summary>
    
## 🖥️ Phase 1 — Virtual Infrastructure & Linux Hardening

The foundation of the project is a network of virtual machines, each with a specific role:

| VM | Role | Notes |
|----|------|-------|
| `app-server` | Application backend | Higher resource allocation |
| `web-server-1` | Frontend web server | Handles user requests |
| `web-server-2` | Frontend web server | Handles user requests |
| `load-balancer` | Traffic distribution + CI/CD routing | Routes traffic to webservers and redirects Gitea webhooks |
| `ci-server` | CI/CD tooling (Drone CI + runner) | Included into provision configurations in Phase 2 |
| `backup-server` | Scheduled backups | Weekly full backups of application data |

### Automated Provisioning

All VMs were provisioned automatically using **Vagrant** to define and spin up the virtual environment, and **Ansible** to configure them. This meant the entire environment could be reproduced from scratch with a single command — no manual server setup. 

All VMs were configured with **static IP addresses** on a shared subnet to ensure reliable inter-VM communication, while minimizing external exposure.

### Security Hardening

Each machine was hardened following Linux administration best practices:

- **Dedicated `devops` user** — root account left untouched; sudo privileges granted appropriately
- **SSH key-only authentication** — password login disabled; only the `devops` user permitted SSH access
- **UFW firewall** — enabled and configured to allow only necessary traffic
- **Unused network interfaces disabled** — to reduce the attack surface
- **Secure umask** — newly created files are not world-readable or writable by default
- **Automatic security updates** — enabled to keep systems patched against known vulnerabilities
- **Fail2Ban** — installed to protect against SSH brute-force attacks


---

## 🔄 Phase 2 — Application & CI/CD Pipeline

A lightweight diagnostic application was built to collect and display real-time performance metrics from the backend VM. This gave the infrastructure a concrete workload to operate on.

### Backup

A dedicated `backup-server` VM was set up to run weekly full backups of all application-related data. Restores were handled via Ansible playbooks, making recovery a repeatable, automated process rather than a manual one. 

### CI/CD with Drone CI & Gitea

A dedicated `ci_server` VM was created and automated pipeline was implemented using **Drone CI** triggered via **Gitea webhooks** on every push to the `main` branch. The pipeline is path-aware — backend and frontend steps only run when their respective directories have changed.

`ci-server` VM hosted both Drone CI and its runner. Gitea webhooks were routed to this VM through the **Nginx load balancer**, which was configured to forward webhook traffic specifically to the CI server while distributing all other incoming traffic across the two web servers using the `least_conn` algorithm.

During provision, the pipeline is automatically triggered to pull the latest application build.

#### Backend Pipeline Steps

1. **Lint & dependency audit** — `npm ci`, ESLint, `npm audit`
2. **Docker build & push** — image tagged with both `latest` and the short commit SHA
3. **Container security scan** — Trivy scans for `CRITICAL` vulnerabilities
4. **Performance test** — Artillery load test run against the containerized backend in an isolated Docker network
5. **Deploy** — SSH into `app-server`, pull latest image, restart container

#### Frontend Pipeline Steps

1. **Lint & dependency audit**
2. **Docker build & push** — same tagging strategy as backend
3. **Container security scan** — Trivy
4. **Deploy to both web servers** — parallel SSH deployments to `web-server-1` and `web-server-2`

#### Notifications

Email notifications (via Gmail SMTP) are sent on both pipeline success and failure, with a direct link to the build logs.

---

## 📈 Phase 3 — Observability Stack

To gain visibility into the running infrastructure, a full observability stack was deployed:

- **Prometheus** — metrics collection from all VMs and containers
- **Grafana** — dashboards for visualizing system and application performance
- **ELK Stack (Elasticsearch, Logstash, Kibana)** — centralized log aggregation and search across all nodes
- **cAdvisor** - container-level metrics

Custom dashboards were built to monitor CPU, memory, network I/O, and application-level metrics in real time and SMTP alerts were configured for high resource usage both at the VM and container level, repeated container restarts, unreachable VM's or Elastic cluster status changes.

---

## ☸️ Phase 4 — Kubernetes Migration (Minikube)

The entire stack — application, CI/CD tooling, and observability components — was migrated from the VM-based setup into a **Kubernetes environment running on Minikube**.

### Application Deployment

Kubernetes manifests were written for all workloads, replacing the previous raw `docker run` commands with proper Deployment and Service resources:

- **Backend** — single replica Deployment with resource requests/limits, exposed via a ClusterIP Service
- **Frontend** — two-replica Deployment for redundancy, with a Service providing internal load balancing across pods
- **Ingress** — configured to manage external access to the frontend

### Storage & State

PersistentVolumes (PVs) and PersistentVolumeClaims (PVCs) were set up to ensure data from the CI/CD tooling and observability stack survives pod restarts and redeployments.

### Observability in Kubernetes

The Prometheus + Grafana and EFK stack (Logstash switched to Fluentbit) were redeployed as Kubernetes workloads, with dashboards covering cluster health, pod/container performance, and application-level metrics. Alerting rules were configured through Prometheus Alertmanager for node, pod, and cluster-level conditions.

### Horizontal Pod Autoscaling

An HPA was configured for the frontend Deployment to automatically scale replica count based on CPU utilization, demonstrating load-responsive scaling within the cluster.

---

## 🚀 Phase 5 — GitOps with Helm & ArgoCD

With the application running in Kubernetes, the next step was to introduce proper GitOps practices to make deployments declarative, auditable, and automated.

### Helm

A **custom Helm chart** was created for the application, bundling backend and frontend Deployments, Services, and ConfigMaps into a single reusable package. Templating was used to make image versions, resource limits, and environment variables easily configurable.

A production database (PostgreSQL) was also deployed using an **existing Helm chart** from a public registry, with persistent storage configured and a Kubernetes Job used to verify connectivity and functionality post-deployment with credentials managed by **HashiCorp Vault**.

### HashiCorp Vault

**HashiCorp Vault** was deployed into dedicated `vault` namespace, providing a secrets management layer so that sensitive credentials never appear in Git or Kubernetes Secrets in plaintext.

The setup involved several moving parts:

* A **KV secrets engine** was enabled and the PostgreSQL password stored at `kv/data/database/postgresql`

* **Kubernetes authentication** was configured, allowing pods to authenticate with Vault using their ServiceAccount identity

* A scoped **read policy** (`postgres-read-policy`) was created, granting access only to the specific secret path — nothing else

* A **Vault role** (`postgresql-app`) was bound to the PostgreSQL pod's ServiceAccount and namespace

* The **Secrets Store CSI driver** was installed alongside the Vault provider, enabling Vault secrets to be mounted directly into pod filesystems as volumes — no application code changes required

At pod startup, the CSI driver authenticates with Vault using the pod's ServiceAccount, retrieves the password, and mounts it into the container. The secret is never hardcoded, never committed to Git, and encrypted at rest inside Vault, which is itself backed by a PersistentVolume.

### ArgoCD

**ArgoCD** was deployed into the cluster (via Helm) and connected to the Git repository containing the Kubernetes manifests. Key configuration decisions:

- Sync options set to delete stale resources only after new resources are healthy
- Auto-sync enabled to continuously reconcile cluster state with Git
- RBAC configured to give ArgoCD the minimum necessary permissions

### ArgoCD Image Updater

The **ArgoCD Image Updater** was installed and configured to watch Docker Hub for new image versions. When a new tag is detected, it uses the Git write-back method to commit the updated image tag directly to the repository. ArgoCD then detects the drift between Git and the cluster and syncs automatically — meaning Git always reflects exactly what is running, and every deployment is traceable through commit history.

### CI/CD Integration

In the GitOps phase, Drone CI's role was deliberately narrowed. Direct `kubectl apply` calls were removed and the pipeline's only responsibilities became testing, building, and pushing semantically versioned images (`1.0.<build_number>`) to Docker Hub. Everything after that is handled by ArgoCD Image Updater and ArgoCD itself.

### Argo Rollouts & Automated Blue/Green Deployments

Rather than standard Kubernetes `Deployment` resources, the backend was managed using **Argo Rollouts** with a **Blue/Green deployment strategy**. When a new image version is detected and synced by ArgoCD, Argo Rollouts spins up a full preview (green) environment alongside the currently active (blue) one before any traffic is switched.

Promotion from green to active is gated by a pre-promotion **AnalysisTemplate** that runs automated health checks against the preview environment — hitting the `/metrics` endpoint every 5 seconds, twice in total. If even one check fails, the rollout is automatically aborted and the active (blue) version continues serving traffic unchanged.

The full end-to-end deployment flow looks like this:

```
Code pushed to Gitea
        ↓
Drone CI tests, builds, and pushes versioned image to Docker Hub
        ↓
ArgoCD Image Updater detects new tag, commits updated version to Git
        ↓
ArgoCD detects Git drift, syncs cluster
        ↓
Argo Rollouts spins up preview (green) environment
        ↓
AnalysisTemplate runs health checks against preview
        ↓
PASS → green auto-promoted to active, blue scaled down
FAIL → rollout aborted, blue remains active
```

---

## ☁️ Phase 6 — Cloud Cost Analysis

The final phase was a standalone exercise using a provided sample application (React frontend, Go backend, PostgreSQL database). The goal was to produce a realistic, methodology-driven cloud migration cost analysis — not just theoretical estimates, but numbers grounded in actual measured resource usage.

### Performance Baseline

The sample application was deployed locally with a full observability stack: Grafana, Prometheus, Postgres Exporter, Loki, Promtail, and cAdvisor for container-level metrics. Two baselines were established — one at idle to approximate test environment usage, and one under simulated peak load using **Locust** with 1000 simultaneous active users at approximately 200 requests/second.

Key findings from the baseline:
- The **backend pod** was by far the most resource-intensive component under load
- PostgreSQL's default connection limit of 50 creates a bottleneck at scale — raising `max_connections` was accounted for in resource sizing, though connection pooling would be the proper long-term fix
- If load exceeds the 200 RPS estimate, the production main node group CPU is the first thing to saturate, at which point the Cluster Autoscaler would spin up additional nodes

### Cloud Provider Selection

All three major providers were initially evaluated — AWS, GCP, and Azure. Azure was eliminated early due to a structural pricing issue with its load balancing tier. Meeting the requirement for TLS termination at the external load balancer necessitates Azure Application Gateway v2, which uses a reserved-capacity billing model: a fixed gateway-hour fee applies continuously regardless of traffic volume, with variable capacity unit costs layered on top. TLS connections directly consume compute units, meaning data-in-transit protection actively drives up the variable cost component. 

Combined, these two cost layers pushed Azure's load balancing spend significantly above both AWS and GCP before the remaining required resources were accounted for — AWS and GCP both offer TLS termination as part of their standard load balancer pricing with no fixed reservation fee, making their costs idle-friendly and traffic-proportional by comparison. The detailed comparison therefore proceeded between AWS and GCP.

### Dependency & Data Flow Mapping

A visual dependency map was produced covering all service-to-service relationships, shared resources, and data flow directions. Resources were split across three billing accounts — `Production`, `Test`, and `Shared` — matching how a real multi-environment cloud setup would be structured and billed.

### Infrastructure Requirements & Cluster Sizing

Resource requirements were derived from the measured baselines rather than guesswork. Three node groups were defined for each environment — **main** (app workloads), **monitoring** (Prometheus, Loki, Grafana, Promtail, cAdvisor), and **tools** (ArgoCD) — with production sized for HA across multiple availability zones and test scaled to approximately 30–40% of production with no HA requirement.

Production node selection:
- **AWS:** 2× m5.large (main), 2× t3.medium (monitoring), 1× t3.medium (tools)
- **GCP:** Custom-spec n2d and e2 instances sized precisely to measured load — GCP's custom machine types allowed tighter resource matching than AWS's fixed instance sizes

Security and networking requirements were also fully mapped: WireGuard VPN for internal access, ALB/external LB for public traffic, private subnets for all nodes and databases, TLS termination at the load balancer, KMS encryption at rest, and IAM roles with least-privilege service accounts throughout.

### Cost Comparison

| Environment | AWS (USD/mo) | GCP (USD/mo) |
|-------------|-------------|-------------|
| Production  | $499.99     | $524.41     |
| Test        | $190.63     | $187.67     |
| Shared      | $16.79      | $36.08      |
| **Total**   | **$707.41** | **$748.16** |

AWS came out approximately **$40/month cheaper** overall despite providing more raw hardware resources. This was somewhat surprising — GCP's custom machine types allowed more precise resource matching, but AWS still won on compute and shared services pricing. The one notable advantage GCP holds is **free intra-region (AZ-to-AZ) traffic**, which AWS charges for and could shift the comparison if internal traffic volumes turn out higher than estimated.

Accounting for one-time credits across all three billing accounts (AWS $200/account, GCP $300/account with a 90-day usage window), first-year totals estimate to roughly **$7,889 for AWS** and **$8,270 for GCP**.

### Risk Assessment & Cost Controls

A separate risk assessment and management plan was produced covering budget alerting thresholds, right-sizing strategy, storage tiering (hot SSD for Loki and Prometheus, cold object storage for long-term log retention), and cleanup policies aligned to retention requirements — 30 days for metrics, 1 year for application logs. Recommendations included automated start/stop schedules for the test environment outside working hours and the option to run test/shared workloads on spot instances to reduce costs further.

---

## Key Takeaways

This project spans the full arc of a modern DevOps journey — from hand-configuring virtual machines and hardening Linux servers, through containerized CI/CD pipelines, all the way to GitOps-driven deployments and production-grade cloud cost planning. Every phase built directly on the last, and every tooling decision was made deliberately with security, scalability, and operational best practices in mind.
</details>