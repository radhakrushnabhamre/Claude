# RADHAKRUSHNA BHAMRE

**Backend Engineer | Java · Spring Boot · PHP/Laravel · SQL Server | Core Banking & Regulatory Reporting**
Pune, Maharashtra · [phone] · [email] · github.com/radhe1115 · [linkedin.com/in/...]

---

## Summary

Backend engineer with ~2 years of experience building core-banking software for cooperative banks. Primary author of a metadata-driven reporting engine now **live in production at a bank**, and recipient of the company's **Report Maestro Award (2026)**. Hands-on with Java/Spring Boot REST services, SQL Server stored procedures, Liquibase migrations, CI/CD, and regulatory/MIS reporting (NPA provisioning, deposit insurance, SFT, balance sheet).

---

## Skills

- **Languages:** Java, PHP, SQL (T-SQL), JavaScript, TypeScript
- **Backend:** Spring Boot, Spring MVC, Spring Data JPA / Hibernate, REST APIs, Laravel
- **Database:** Microsoft SQL Server (stored procedures, query tuning), Liquibase, MySQL
- **Frontend:** Angular, Bootstrap, Blade
- **Tools & DevOps:** Git, GitLab CI/CD & Runners, Maven, PowerShell, Docker (working knowledge), Postman, Jira, Confluence, Apache Solr
- **Reporting:** Eclipse BIRT, headless Chromium / Puppeteer PDF generation, Excel export
- **Domain:** Core banking, maker-checker authorization, audit trails, regulatory & statutory reporting

---

## Experience

### [Software Developer / Associate Software Developer] — Novillex Technologies, Pune
*Dec 2024 – Present · FinWiz Core Banking Solution for cooperative banks*

**FinDrishti Reporting Engine — primary author (200+ commits), live in production**
- Took the BIRT-replacement framework from POC to production: designed a **metadata-driven reporting engine** (Laravel, SQL Server) where a report is defined as database configuration instead of a hand-built BIRT design, using a service pipeline (context → layout/section resolvers → parameter binding → query execution → rendering → export) with pluggable resolvers; [X] reports migrated off BIRT so far.
- Built **PDF/Excel export on a persistent headless Chromium** instance (Browsershot/Puppeteer), producing PDFs identical to on-screen output and removing per-request browser start-up; PDF generation time reduced from [X]s to [Y]s.
- **Integrated core-banking printing-charge APIs** through a backend proxy with double-submit protection, enabling automatic charge calculation and voucher posting for printed reports.
- Built a **read-through metadata cache** with invalidation on admin save; replaced ORM models with lightweight row objects so 7,000+ cached filter rows fit within PHP's 128 MB memory limit. Added an admin UI to configure reports that exports Liquibase SQL.
- Fixed **silent data loss** when report queries returned duplicate column names by switching to positional row fetching and renaming duplicates.

**Core Banking Backend — Java / Spring Boot**
- Developed REST APIs for the **Daily Deposit Agent Master** module with **maker-checker authorization**, field-level modification audit log, duplicate detection and login-ID generation (Spring Boot, JPA, Liquibase); released in product v2.2.x.
- Resolved [103]+ production defects through root-cause analysis, including loan/deposit authorization, insurance handling for unsecured loan accounts, and inward-clearing cheque validation.
- Implemented Solr-based CASA statement retrieval for large account sets.

**Reporting, Database & Release Engineering**
- Built and maintained [N]+ BIRT statutory and operational reports (deposit insurance, NPA provisioning, balance sheet, loan/FD statements, SFT, any-day balance); optimized stored procedures and report queries through index, join and filter tuning, reducing report execution time by [30]%.
- Migrated the report repository from SVN to Git and automated deployment with a **PowerShell script run on GitLab CI runners** (changed-files-only, automatic backups, deployment history), supporting weekly releases to [N] client banks and saving ~30 minutes per release.
- Packaged first-release Liquibase changelogs: schema delta, 25 report seeds, `runOnChange` stored-procedure changelog, parameterized bank codes.
- Reconciled report metadata across 4 repositories: resolved 18 of 19 ambiguous menu groups, synced 98 drifted report titles, removed orphaned and duplicate entries.

---

## Projects

<!-- Add ONLY after it is built and on GitHub (plan: Month 2) -->
**Maker-Checker Approval Service** — Spring Boot 3, JPA, JUnit 5, Mockito, Testcontainers, Docker · [GitHub link]
- [One line: what it does]
- [One line: testing / deployment detail]

---

## Education & Certifications

- **B.E. in Information Technology** — [College], [University] · 2019–2023 · CGPA 8.2/10
- Java Spring Framework, Spring Boot & Spring AI — Udemy, 2026
- Java Development — Cyber Success Institute, Pune, 2023

---

## Achievements

- **Report Maestro Award** — Novillex Technologies Foundation Day, Jan 2026, for excellence in financial report development.
- Cleared written exams for CDSE, AFCAT, SSC-Tech and Indian Coast Guard; called for SSB interview 7 times (2023–2024).
- Student of the Year 2023; NSS Secretary (grew volunteer base from 35 to 100+, led a 500+ tree plantation drive); runner-up, district-level elocution competition.
