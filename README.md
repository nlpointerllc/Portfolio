# Tomas Venere — Project Portfolio

**Chief Architect · Senior Software Engineer · Full-Stack Developer**
veneret@gmail.com · [linkedin.com/in/tomas-venere-099165154](https://www.linkedin.com/in/tomas-venere-099165154/) · Dawsonville, GA

> All repositories are private. This document provides a curated overview of the most significant projects across 12+ years of professional engineering. Metrics and details are based on first-hand involvement.

---

## Flagship Projects

---

### Heathos — Multi-Tenant Healthcare Platform
**Role:** Independent Chief Architect & Head of Engineering
**Year:** 2025 – Present
**Stack:** .NET Core 8, C#, React, Blazor, Azure (AKS, Key Vault, Cosmos DB, Service Bus), SQL Server, Redis, RabbitMQ, Docker, Kubernetes, OAuth 2.0, SAML, Terraform, GitHub Actions

**What it is:**
A suite of four healthcare products built from the ground up, serving 4,000+ provider partners and designed to scale to 2.5 million patients. I was brought in as the sole architecture decision-maker and head of engineering.

**What I built:**
- Designed the entire cloud-native, multi-tenant platform on Azure with per-tenant compute and data isolation to meet 99.9% SLA from day one
- Architected the microservices split aligned to team ownership boundaries — not just technical convenience
- Built the security model from scratch: OAuth 2.0 + SAML for partner SSO, RBAC at the data row level, secrets rotation via Azure Key Vault, private endpoint network isolation
- Set up CI/CD with GitHub Actions + Docker + Kubernetes (AKS); cut deployment time from ~3 hours to under 20 minutes within the first 6 weeks
- Implemented SQL Server + Cosmos DB + Redis data layer; Redis caching dropped average API response times from ~380ms to ~90ms on the highest-traffic endpoints
- Chose RabbitMQ over Service Bus after evaluating cost/latency tradeoffs for the async messaging backbone
- Managing 3 parallel engineering squads (15 engineers total) across front-end, back-end, and infrastructure

---

### Envestnet — Enterprise Financial Platform Modernization
**Role:** Chief Architect & Head of Engineering
**Year:** 2025 – Present
**Stack:** .NET Core, C#, Blazor, AWS (Bedrock, EKS, Secrets Manager), Azure OpenAI, Kafka, RabbitMQ, MassTransit, Redis, Docker, Kubernetes, ArgoCD, GitLab CI, Okta, Auth0, OAuth 2.0, SAML

**What it is:**
Enterprise wealth management and financial advisory platform serving 200,000+ advisor accounts. Led the full technical modernization of a 600,000-line C# monolith.

**What I built:**
- Decomposed a 600k-line monolith into 12 bounded-context microservices over 8 months; release cycle dropped from 3 weeks to 2 days, hotfix time from 4 hours to under 30 minutes
- Designed a MassTransit + RabbitMQ/Kafka messaging layer processing 180,000+ financial events per day with saga orchestration, automatic retries, and dead-letter alerting — zero message loss in production since launch
- Integrated AWS Bedrock and Azure OpenAI for an AI-assisted financial advisory feature; prototype to production in 11 weeks, now surfacing personalized insights for 200K+ advisor accounts
- CI/CD transformation using GitLab CI + ArgoCD (GitOps) + Octopus Deploy across EKS clusters; teams went from 4 deploys/month to 40+ deploys/month with zero unplanned outages in the last quarter
- Enterprise IAM via Okta + Auth0 across 15 partner integrations; passed SOC 2 review with no findings in the engineering domain
- Redis caching strategy cut p95 API latency from 620ms to 95ms on portfolio analytics endpoints — the biggest user-facing win of the year per product team feedback
- Coordinating 4 concurrent squads (~18 engineers) across wealth management tooling, reporting infrastructure, partner integrations, and platform security

---

### Alaska Airlines — Mileage Plan Award Modernization
**Role:** Lead Engineer / Senior Software Engineer
**Year:** 2021 – 2024
**Stack:** .NET / C#, React, Azure, Redis, SQL Server, GraphQL, JWT / OAuth 2.0, Azure Functions, Power BI, Serilog, Sumo Logic, GitHub Copilot

**What it is:**
Complete redesign of Alaska Airlines' Mileage Plan award redemption system. The algorithm I wrote has generated **over $100M in incremental Mileage Plan revenue every year since launch**.

**What I built:**
- Wrote the core award redemption algorithm end-to-end; led a team of 5 engineers through design, delivery, and stakeholder coordination with actuarial and finance
- Built and maintained the BFF (Backend for Frontend) layer handling 4M+ API calls per month with JWT + OAuth 2.0, structured Serilog logging, and Sumo Logic alerting
- Delivered the Siebel-to-LMS partner migration for 8 airline partners — designed API contracts, built the transformation layer, wrote integration tests, managed partner comms; zero incidents post-cutover
- Built GraphQL + Redis caching layer for the Mileage Plan member portal; cache hit rate stabilized at 87% on the most common queries, meaningfully reducing DB load during peak booking windows
- Built Power BI dashboards consumed by 200+ internal stakeholders across revenue management, loyalty ops, and executive leadership — replaced 6 manual Excel reports that were being emailed weekly
- Led a GitHub Copilot-assisted refactoring sprint across 4 legacy microservices; cleaned ~38,000 lines of C#, improved test coverage from 22% to 61%, cut average PR review time in half

---

### Tri-State Memorial Hospital — Digital Platform (tristatehospital.org)
**Role:** Software Engineer & Systems Integration Specialist
**Year:** 2019 – 2021
**Stack:** ASP.NET Core, SQL Server, React, HL7 v2, WordPress, Windows Server 2016/2019, IIS, Logical Ink, Medex, Create!Forms

**What it is:**
Complete greenfield hospital digital platform built as a one-person team, plus HL7 healthcare messaging middleware for clinical system integration.

**What I built:**
- Built the entire tristatehospital.org platform from scratch: provisioned Windows Server, configured IIS, designed the SQL Server schema, and delivered 150+ pages including patient portals, staff directories, service listings, and 3 integrated sub-projects
- Built HL7 v2 messaging middleware in .NET handling ADT, ORM, and ORU message types between the EMR, lab, and radiology systems; resolved a backlog of ~200 stuck messages in the first two weeks that had been failing silently for months
- Integrated Logical Ink, Medex, and Create!Forms for digital clinical data capture, eliminating paper-based intake for 3 departments
- Administered 4 Windows Server environments (2016/2019) — patching, SQL Server tuning, IIS config — maintaining 99.6% uptime over a full calendar year with no major incident

---

### Vastian — .NET Modernization & Microservices Migration
**Role:** Senior Software Engineer & Technical Lead
**Year:** Jun 2024 – Dec 2024
**Stack:** .NET Core 8, Razor Pages, Blazor, Azure, Docker, Azure Functions, Azure Service Bus, Syncfusion, SQL Server, TDD, Clean Architecture, SOLID

**What I built:**
- Migrated 3 legacy .NET Framework 4.7 applications to .NET Core 8; startup time dropped ~55%, memory footprint reduced ~40%
- Built the Razor Pages + Blazor UI platform from scratch integrating Syncfusion's enterprise component suite; feature delivery time went from ~2 weeks per feature to ~2 days
- Stood up a Docker-based microservices architecture on Azure with Azure Functions + Service Bus for async workflows; went from a single IIS monolith to 8 independently deployable services
- Refactored the core domain layer with SOLID and Clean Architecture; cyclomatic complexity on the most-touched classes dropped from avg 34 to avg 8
- Raised unit test coverage from 11% to 73% in 4 months; production incidents dropped measurably in the final weeks of the engagement
- Fixed 4 reporting SQL queries that were timing out in production; the slowest went from 47 seconds to under 2 seconds

---

### Envestnet Pulse — Internal Healthcare Analytics Platform
**Role:** Chief Architect & Lead Engineer
**Year:** 2025 – Present
**Stack:** .NET Core, React, Azure, SQL Server, Redis, Docker, Kubernetes, REST APIs, CI/CD

**What it is:**
Internal multi-module web application spanning healthcare analytics, reporting dashboards, partner management, and operational tooling. Built alongside the broader Envestnet modernization work as a dedicated internal product.

**Key highlights:**
- Multi-tab SPA architecture with live data sync across modules
- Role-based access control scoped to individual data records
- CI/CD pipeline from commit to production in under 20 minutes
- Integrated with the same microservices backbone as the enterprise platform

---

### Tomiwebsites.com Personal Portfolio & Tools
**Role:** Founder & Developer
**Year:** 2024 – Present
**Stack:** ASP.NET Core 9, Razor Pages, Alpine.js, Tailwind CSS, highlight.js, Roslyn C# Scripting, Azure

**What it is:**
Personal site with live demos and interactive tools — deployed and publicly accessible.

**What's in it:**
- **Resume page** — interactive career timeline, animated stat counters, project cards with live status
- **LeetyCode** — browser-based C# coding playground; runs real C# code server-side via Roslyn scripting, syntax-highlighted editor, 20+ algorithm problems with automated test cases and solutions
- **Study Guide** — reference for .NET advanced topics, algorithm patterns (Big O analysis, code examples), and SQL mastery
- **Maeve's Treatment Tracker** — real-time treatment tracker for a pediatric leukemia patient, with phase timeline, drug reference, interactive calendar, and medical glossary
- **Warrior Path / ZeroToHero** — personal growth and habit tracking dashboard with XP system and life stat visualization
- **Growth OS** — goals, habit logs, daily quotes, and personal analytics

---

### MediaLab VR — NASA-Affiliated VR Research
**Role:** VR Developer & Research Contributor
**Year:** 2016 – 2017 (Washington State University)
**Stack:** Unity, C#, Python, 2D/3D Image Analysis

**What I built:**
- Designed and built interactive VR simulations and educational environments in Unity (C#), including 3D physics, dynamic lighting, and immersive interaction systems
- Contributed to a NASA-affiliated research initiative involving advanced 2D/3D image analysis with Python for aerospace and scientific datasets

---

### QwickCharge — EV Charging Platform UI
**Role:** Front-End Developer
**Year:** 2017 – 2018
**Stack:** React.js, .NET, Azure, WordPress

**What I built:**
- Developed responsive React.js UI components integrated with a custom .NET backend
- Supported Azure-hosted deployment pipelines and environment configuration across dev, staging, and production

---

### Independent Consulting — Tomiwebsites.com & HottCode.com
**Role:** Founder & Full-Stack Developer
**Year:** 2015 – 2021

**What I built:**
- Delivered 100+ custom websites for independent clients using React, WordPress, Angular, and Svelte — full UI/UX design, backend integration, and hosting setup
- Built and deployed 6+ mobile applications in React Native, Kotlin (Android), and Swift (iOS)

---

## Core Competencies

| Area | Details |
|---|---|
| **Architecture** | Microservices, Clean Architecture, DDD, CQRS, Event Sourcing, BFF, API Gateway |
| **Languages** | C#, JavaScript/TypeScript, Python, Java, Swift, Kotlin, SQL |
| **Frameworks** | .NET Core, React, Blazor, Razor Pages, Angular, React Native |
| **Cloud** | Azure (AKS, Functions, Service Bus, Key Vault, Cosmos DB), AWS (EKS, Bedrock, Lambda, Fargate, Secrets Manager), GCP |
| **Messaging** | RabbitMQ, Kafka, MassTransit, Azure Service Bus |
| **Data** | SQL Server, PostgreSQL, Cosmos DB, Redis, Power BI |
| **Security** | OAuth 2.0, SAML, JWT, Okta, Auth0, RBAC, SOC 2, SC-100 Certified |
| **DevOps** | Docker, Kubernetes, Terraform, GitHub Actions, GitLab CI, ArgoCD, Octopus Deploy |
| **AI** | AWS Bedrock, Azure OpenAI, Roslyn scripting, GitHub Copilot |
| **Leadership** | 3–4 parallel Agile squads, 14–20 engineers, ADRs, architecture reviews, mentoring |

---

## By the Numbers

- **$100M+** in annual revenue generated by a single algorithm (Alaska Airlines Mileage Plan)
- **4M+** API calls per month on systems I built
- **180,000+** financial events per day processed with zero message loss
- **200,000+** advisor accounts served on AI-enhanced platform
- **4,000+** provider partners on the Heathos healthcare platform
- **600,000** lines of legacy code decomposed into clean microservices
- **100+** websites delivered for independent clients
- **150+** engineers mentored over 12 years
- **12+** years of professional software engineering

---

## Certifications

- Microsoft Certified: Cybersecurity Architect Expert (SC-100)
- AWS & Azure cloud practitioner experience across production workloads

---

*References, architecture diagrams, and deeper technical walkthroughs available upon request.*
*Contact: veneret@gmail.com*
