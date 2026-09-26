# [YOUR NAME]

**Backend Engineer | Java · Spring Boot · PHP/Laravel · SQL Server | Core Banking & Regulatory Reporting**
Pune, India · [phone] · [email] · [linkedin.com/in/...] · [github.com/...]

---

## Summary

Software Developer with ~2 years of experience building core-banking software for cooperative banks. Primary author of a metadata-driven reporting engine now **live in production at a bank**. Hands-on with Java/Spring Boot REST services, SQL Server stored procedures, Liquibase migrations, and regulatory/MIS reporting (NPA provisioning, deposit insurance, SFT, balance sheet).

---

## Skills

- **Languages:** Java, PHP, SQL (T-SQL), JavaScript, TypeScript
- **Backend:** Spring Boot, Spring Data JPA / Hibernate, REST APIs, Laravel
- **Database:** Microsoft SQL Server (stored procedures, query tuning), Liquibase, MySQL
- **Frontend:** Angular, Bootstrap, Blade
- **Tools & DevOps:** Git, GitLab CI, Maven, PowerShell, Docker (working knowledge), Postman, Jira, Apache Solr
- **Reporting:** Eclipse BIRT, headless Chromium / Puppeteer PDF generation, Excel export
- **Domain:** Core banking, maker-checker authorization, audit trails, regulatory & MIS reporting

---

## Experience

### Software Developer — [Company], [City]
*Dec 2024 – Present · Core-banking software provider for cooperative banks*

**Reporting Engine — primary author (200+ commits), live in production**
- Designed and built a **metadata-driven reporting engine** (Laravel, SQL Server) where a report is defined as database configuration instead of a hand-built BIRT design, using a service pipeline (context → layout/section resolvers → parameter binding → query execution → rendering → export) with pluggable resolvers; [X] reports migrated off BIRT so far.
- Built **PDF/Excel export on a persistent headless Chromium** instance (Browsershot/Puppeteer), producing PDFs identical to on-screen output and removing per-request browser start-up; PDF generation time reduced from [X]s to [Y]s.
- **Integrated core-banking printing-charge APIs** through a backend proxy with double-submit protection, enabling automatic charge calculation and voucher posting for printed reports.
- Built a **read-through metadata cache** with invalidation on admin save; replaced ORM models with lightweight row objects so 7,000+ cached filter rows fit within PHP's 128 MB memory limit. Added an admin UI to configure reports that exports Liquibase SQL.
- Fixed **silent data loss** when report queries returned duplicate column names by switching to positional row fetching and renaming duplicates.

**Core Banking Backend — Java / Spring Boot**
- Developed REST APIs for the **Daily Deposit Agent Master** module with **maker-checker authorization**, field-level modification audit log, duplicate detection and login-ID generation (Spring Boot, JPA, Liquibase); released in product v2.2.x.
- Fixed production defects in loan/deposit authorization, insurance handling for unsecured loan accounts, and inward-clearing cheque validation.
- Implemented Solr-based CASA statement retrieval for large account sets.

**Reporting, Database & Release Engineering**
- Developed and maintained [N]+ BIRT regulatory and operational reports: deposit insurance, NPA provisioning, balance sheet, loan/FD statements, SFT, any-day balance.
- Migrated the report repository from SVN to Git and wrote a **PowerShell deployment script** (changed-files-only, automatic backups, deployment history) run through GitLab CI, supporting weekly releases to [N] client banks.
- Packaged first-release Liquibase changelogs: schema delta, 25 report seeds, `runOnChange` stored-procedure changelog, parameterized bank codes.
- Reconciled report metadata across 4 repositories: resolved 18 of 19 ambiguous menu groups, synced 98 drifted report titles, removed orphaned and duplicate entries.

---

## Projects

<!-- Add ONLY after it is built and on GitHub (plan: Month 2) -->
**Maker-Checker Approval Service** — Spring Boot 3, JPA, JUnit 5, Mockito, Testcontainers, Docker · [GitHub link]
- [One line: what it does]
- [One line: testing / deployment detail]

---

## Education

**B.E. in Information Technology** — [College], [University] · 2023 · CGPA: [X]

---

## Achievements

- Cleared written exams for CDSE, AFCAT, SSC-Tech and Indian Coast Guard; called for SSB interview 7 times (2023–2024).
