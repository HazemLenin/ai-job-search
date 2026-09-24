---
framework_version: 1.1.1
---

# Candidate Profile

## Identity
- **Name:** Hazem Lenin
- **Location:** Alexandria, Egypt
- **Phone:** +201002353194
- **Email:** hazemlenin@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/hazem-lenin
- **GitHub:** https://github.com/HazemLenin
- **Portfolio:** https://hazemlenin.github.io
- **Status:** GAMP's Egyptian branch is closing 30 Jul 2026 (business reasons, unrelated to performance); actively seeking new opportunities, available immediately after
- **Constraints:** Based in Alexandria, Egypt; open to remote and on-site; will relocate to Cairo for any onsite role

### Languages
<!-- Every language you can work in professionally, with your honest level. Used by the
Language Gate in 04-job-evaluation.md and by job-scraper/search-queries.md's query-language
generation. Omit any language you don't actually work in - an undeclared language is treated as
a hard no, not a gap to smooth over. -->

| Language | Level | Notes |
|----------|-------|-------|
| Arabic | Native | |
| English | Professional working proficiency | |

## Education

| Degree | Period | Institution | Key Topics |
|--------|--------|-------------|------------|
| BBA, Management Information Systems (GPA 3.69/4.0) | Oct 2021 - Jun 2025 | Alexandria University | Statistics, Accounting, Data Analysis, Business Intelligence, Cloud Computing, Databases, Software Design |
| Nanodegree, Web Development | Sep - Nov 2022 | Udacity | Web development |

## Professional Experience

### Software Engineer - GAMP (Mar 2024 - Jul 2026)
Alexandria, Egypt (IT Services & Software Development; enterprise clients in Poland)
- Software engineer on GapMap, a modular B2B partition management platform for agricultural trade markets, serving enterprise clients in Poland (Renk, ZRRT); digitizes the sale of trading stands, subscriptions, and entry tickets, handles payments, and controls vehicle traffic through integrations with LPR cameras, gate barriers, payment terminals, and fiscal devices; owned the Contractors module end-to-end across .NET Core API and Angular - domain modelling, EF Core schema, API design, and UI components
- Built full-stack features spanning MFA (Identity Server, recovery codes), PayU payments, subscriptions, shipment, a cross-platform feature-toggle system, and raw TCP socket integration with ethernet-connected printers
- Integrated GapMap with external ERP systems used by enterprise clients in Poland, including Subiekt and Symfonia
- Solely owned the mobile project - GapMap and eZRRT (Capacitor + Angular + Trapeze) with FCM push, native config, Fastlane CI/CD, and Google Play/App Store releases; fully automated the release publish step so approved builds reach users without manual intervention
- Responsible for Pay-Station, a kiosk-machine module within GapMap letting on-site customers pay for their parking time - kiosk UI, payment flow, and hardware/printer integration
- Applied Clean Architecture, Repository pattern, CQRS (MediatR), and SignalR across .NET Core services; co-led a 2-month Nx monorepo restructure consolidating two large Angular apps (5 modules) into a shared component library; set up Playwright e2e testing
- Cut calendar load time by ~70% by redesigning the API and optimizing DB queries
- Consolidated 280+ EF Core migration files for the MSSQL database into a single migration, speeding up local builds by ~40%
- Mentored 3 junior developers, conducted technical interviews, delivered a company-wide knowledge-sharing session recognized as the best KS session, and co-authored the company's engineering competency matrix

### Software Engineer - Pixel Academy (Oct 2021 - Mar 2024)
Alexandria, Egypt
- Built a course-center management system with C# ASP.NET Core, Razor Pages, and MSSQL, deployed on IIS, with React and Angular used for select frontend modules
- Built an offline desktop version of the platform with automatic two-way sync to the backend server, plus a data pipeline for converting between Excel files and live system data
- Designed a tailored attendance system tracking attendance history, cross-referencing it against exam attendance and delivered content, and calculating student charges under weekly, monthly, or custom billing plans

### Full Stack Developer - Pixel Stamp (Oct 2020 - Jun 2021)
Alexandria, Egypt
- Architected and built multiple e-learning platforms from the ground up using Django REST Framework - API design, data modelling, and backend architecture decisions
- Designed and delivered a full learning-center management system covering appointments, scheduling, pricing rules, and financial reporting
- Delivered frontend features across React, Vue.js, and Next.js depending on project requirements

## Independent Projects
- **Merge Polisher** (github.com/HazemLenin/merge-polisher, 2024 - Present): AI-powered GitLab/GitHub CI tool that polishes MR/PR descriptions, posts inline code review suggestions, and generates a confidence score based on coverage of critical code paths. Python, layered architecture (adapters, domain, application, core), Gemini API, retry/fallback LLM handling, Docker deployment, GitHub Actions CI.
- **Learn Flow** (github.com/HazemLenin/learn-flow, 2026 - Present): Event-driven mini e-learning platform. Nx monorepo of 3 NestJS microservices (Catalog, Enrollment, Notification) over RabbitMQ, plus React frontend. MongoDB (Mongoose) and PostgreSQL (TypeORM) data models, idempotent event consumers, mock-payment flow, retry/backoff email notification pipeline. Docker Compose, Swagger, Jest/Supertest unit + integration tests, GitHub Actions CI.

## Technical Skills

### Backend
- **.NET Core** (primary): Clean Architecture, Repository pattern, CQRS (MediatR), SignalR, EF Core, Identity Server
- **NestJS**: microservices, event-driven architecture (RabbitMQ), TypeORM, Mongoose
- **Django** (Python): Django REST Framework
- REST APIs, microservices, event-driven architecture

### Frontend
- **Angular** (primary): Signals, standalone components, Nx monorepos
- React, Vue.js, Next.js, Redux, TanStack Query, Vite

### Mobile
- Capacitor + Angular, Trapeze (multi-app native config), FCM push, Fastlane CI/CD, Google Play Console, App Store Connect

### Databases
- MSSQL (EF Core), PostgreSQL (TypeORM), MongoDB (Mongoose), SQL

### DevOps & Tools
- GitLab CI/CD, GitHub Actions, Docker, Fastlane, Git, Playwright (e2e), Jest, Supertest

### Other
- Python, LLM APIs (Gemini), AI-powered developer tooling

## Certifications
- **Software Design and Architecture Specialization** - University of Alberta / Coursera (courses: Design Patterns, Service-Oriented Architecture, Software Architecture, Object-Oriented Design)
- **Web Development Nanodegree** - Udacity (2022)

## Activities
- Coding Instructor (volunteer) - Semicolon

## Publications
None.

## Awards
- Company-wide knowledge-sharing session recognized as best KS session at GAMP

## Deal-breakers
- Rigid, restrictive work environments
- Minimum salary when based in Egypt (including remote roles), location-dependent:
  - Cairo (onsite or remote): 50,000 EGP/month
  - Alexandria onsite: 30,000 EGP/month

## References
- **Dominika Gawara** - COO & Board Member, GAMP. dominika.gawara@gamp.pl, +48 500 000 103, linkedin.com/in/dominika-gawara
  Quote: "This is exactly the profile of a strong fullstack engineer, someone who improves the system he works in, not only the tickets he is given."

More references available upon request.
