<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=32&duration=3000&pause=1000&color=512BD4&center=true&vCenter=true&width=600&lines=MD.+Sikhul+Islam+Shihab;Backend+Engineer;.NET+%7C+Microservices+%7C+Cloud" alt="Typing SVG" />
</h1>

<h3 align="center">Building Enterprise-Grade Distributed Systems with .NET 10</h3>

<p align="center">
  <img src="https://img.shields.io/badge/.NET%2010-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/Microservices-FF6C37?style=for-the-badge&logo=serverfault&logoColor=white" />
  <img src="https://img.shields.io/badge/Event--Driven-000000?style=for-the-badge&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Clean%20Architecture-1E5945?style=for-the-badge&logo=archlinux&logoColor=white" />
</p>

<p align="center">
  <em>Architecting scalable, resilient, and event-driven backend systems with modern .NET ecosystem</em>
</p>

---

## 🏗️ Architecture & Design Philosophy
### Core Principles
- **SOLID** — Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion
- **Vertical Slice Architecture (VSA)** — Features as slices, each containing Controller → Command/Query → Handler → Validator
- **Clean Architecture** — Domain-centric with inward dependencies only
- **Event-Driven** — Async communication via Domain Events & Integration Events
- **CQRS & Event Sourcing** — Command Query Responsibility Segregation for optimized read/write paths

---

## 🛠 Tech Stack

### Backend & Framework
<p>
  <img src="https://skillicons.dev/icons?i=dotnet,cs" />
  <img src="https://img.shields.io/badge/.NET%2010-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/Minimal%20APIs-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
</p>

- **.NET 10** | ASP.NET Core Web API | Minimal APIs | gRPC
- **Vertical Slice Architecture** with MediatR & Carter
- **CQRS** — Command & Query separation with FluentValidation
- **MediatR** — In-process messaging & behavior pipelines
- **FluentValidation** — Request validation pipelines
- **AutoMapper** — Object-to-object mapping
- **Scrutor** — Assembly scanning & decoration
- **Polly** — Resilience & transient-fault handling
- **Serilog** | Seq — Structured logging & observability
- **HealthChecks** — Deep health monitoring (DB, MessageBus, Cache)

### Message Brokers & Event Streaming
<p>
  <img src="https://skillicons.dev/icons?i=rabbitmq" />
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
  <img src="https://img.shields.io/badge/MassTransit-2E7D32?style=flat-square&logo=bus&logoColor=white" />
  <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
</p>

- **RabbitMQ** — Reliable message queuing with topic exchanges
- **MassTransit** — Distributed application framework for RabbitMQ/Azure Service Bus
- **Outbox Pattern** — Guaranteed message delivery
- **Saga Pattern** — Distributed transaction coordination
- **Event Sourcing** — EventStoreDB / Marten for audit trails

### Databases & Persistence
<p>
  <img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb" />
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/EF%20Core-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/Dapper-2E7D32?style=flat-square&logo=dotnet&logoColor=white" />
</p>

| Database | Use Case | Provider |
|----------|----------|----------|
| **PostgreSQL** | Primary transactional DB | Npgsql.EntityFrameworkCore.PostgreSQL |
| **SQL Server** | Enterprise OLTP workloads | Microsoft.EntityFrameworkCore.SqlServer |
| **MySQL** | LAMP-compatible microservices | Pomelo.EntityFrameworkCore.MySql |
| **MongoDB** | Document store / Event store | MongoDB.Driver |
| **Redis** | Distributed caching & session store | StackExchange.Redis |
| **Elasticsearch** | Full-text search & log aggregation | NEST |

### DevOps & Cloud
<p>
  <img src="https://skillicons.dev/icons?i=docker,kubernetes,azure,git,github,githubactions" />
</p>

- **Docker** — Multi-stage builds, containerized microservices
- **Kubernetes** — Container orchestration with Helm charts
- **Azure** — AKS, Azure Service Bus, Azure SQL, App Insights
- **CI/CD** — GitHub Actions with automated testing & deployment
- **Terraform** — Infrastructure as Code
- **Prometheus + Grafana** — Metrics & monitoring

### Testing & Quality
- **xUnit** | NUnit — Unit testing frameworks
- **Moq** | NSubstitute — Mocking frameworks
- **FluentAssertions** — Expressive test assertions
- **Integration Testing** — TestContainers for DB/MQ isolation
- **ArchUnitNET** — Architecture testing & dependency validation

---

## 💼 Enterprise Projects

### 🏪 E-Commerce Microservices Platform
> **.NET 10 | Vertical Slice Architecture | Event-Driven | RabbitMQ | PostgreSQL | Redis | Docker**

A distributed e-commerce system built with 6 autonomous microservices:

- **Catalog Service** — Product management with MongoDB & Elasticsearch
- **Basket Service** — Redis-backed shopping cart with discount integration
- **Ordering Service** — Domain-driven design with EF Core & PostgreSQL
- **Identity Service** — IdentityServer4 with JWT & role-based authorization
- **Payment Service** — Stripe integration with webhook handling
- **Notification Service** — Email/SMS via MassTransit consumers

**Patterns:** Outbox, Saga (Choreography), API Gateway (YARP), Sidecar Logging

---

### 📊 Enterprise Document Management System
> **Clean Architecture | CQRS | Event Sourcing | SQL Server | Azure Blob | SignalR**

- **Vertical Slices** per feature (Upload, Version, Audit, Share)
- **Event Sourcing** with Marten for complete audit trails
- **Real-time collaboration** via SignalR hubs
- **RBAC** with custom authorization handlers & resource-based policies
- **Azure Blob Storage** with SAS token generation
- **Background Jobs** — Hangfire for document processing pipelines

---

### 🏨 Hotel Reservation Distributed System
> **Microservices | gRPC | RabbitMQ | PostgreSQL | Redis | Docker Compose**

- **Booking Service** — Saga pattern for room reservation flow
- **Payment Service** — Idempotent payment processing
- **Notification Service** — Event-driven email confirmations
- **Search Service** — Elasticsearch for room availability
- **gRPC** — High-performance inter-service communication
- **Distributed Caching** — Redis with Cache-Aside pattern

---

## 📈 GitHub Analytics

<p align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=sikhul007&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sikhul007&layout=compact&langs_count=8&theme=tokyonight&hide_border=true"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=sikhul007&theme=tokyonight&hide_border=true"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=sikhul007&theme=tokyo-night&hide_border=true&area=true"/>
</p>

---

## 🎓 Certifications & Learning

- 🏅 **AZ-204** — Azure Developer Associate *(In Progress)*
- 🏅 **AWS Certified Developer** — Associate *(Planned)*
- 📚 **System Design** — Designing Data-Intensive Applications
- 📚 **Domain-Driven Design** — Eric Evans / Vaughn Vernon

---

## 🌐 Connect & Collaborate

<p align="left">
  <a href="https://www.linkedin.com/in/md-sikhul-islam-shihab/">
    <img src="https://skillicons.dev/icons?i=linkedin" width="45" alt="LinkedIn"/>
  </a>
  &nbsp;
  <a href="mailto:sikhulshihab@gmail.com">
    <img src="https://skillicons.dev/icons?i=gmail" width="45" alt="Email"/>
  </a>
  &nbsp;
  <a href="https://codeforces.com/profile/Sikhul2001">
    <img src="https://cdn.simpleicons.org/codeforces/1F8ACB" width="40" alt="Codeforces"/>
  </a>
  &nbsp;
  <a href="https://leetcode.com/Shihab2001">
    <img src="https://cdn.simpleicons.org/leetcode/FFA116" width="40" alt="LeetCode"/>
  </a>
</p>

---

## ⚡ Current Focus

```csharp
var currentStack = new[]
{
    ".NET 10 & ASP.NET Core 10",
    "Vertical Slice Architecture (VSA)",
    "Event-Driven Architecture with RabbitMQ",
    "Domain-Driven Design (DDD)",
    "Event Sourcing & CQRS",
    "Kubernetes & Service Mesh",
    "Observability (OpenTelemetry, Jaeger)",
    "Performance Optimization & Benchmarking"
};
