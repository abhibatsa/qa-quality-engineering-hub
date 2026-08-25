# QA, Quality Engineering & Quality Management Hub

The practitioner reference for Quality Assurance, Quality Engineering, and
Quality Management — process, tooling, automation, and AI-QA — end to end.
Not a career-prep repo (see the SDET and AI Test Engineer career-ladder
repos for that); this is the knowledge base you keep coming back to.

**Out of scope, by design:** SRE, SLOs, incident response, and
observability/monitoring dashboards live in the
[Observability & Monitoring repo](https://github.com/abhibatsa/architecting-software) —
kept separate because reliability engineering is its own discipline, not
a QA sub-topic.

## 🏁 Start Here
- [What This Repo Covers (and What It Doesn't)](./start-here/scope.md)
- [The QA/QE Career Landscape](./start-here/qa-qe-career-landscape.md) — how QA, QE, SDET, and AI Test Engineer relate; cross-links to the dedicated career-prep repos

## 🧪 QA & Testing Fundamentals
- [STLC (Software Testing Life Cycle)](./qa-fundamentals/stlc.md)
- [Test Planning](./qa-fundamentals/test-planning.md)
- [Test Estimation Techniques](./qa-fundamentals/test-estimation.md)
- [Resource Estimation & Capacity Planning](./qa-fundamentals/resource-and-capacity-planning.md)
- [Requirements Traceability Matrix](./qa-fundamentals/traceability-matrix.md)
- [Test Case Design Techniques](./qa-fundamentals/test-case-design-techniques.md) — equivalence partitioning, boundary value analysis, decision tables
- [Test Data Generation Strategies](./qa-fundamentals/test-data-generation.md)
- [Priority vs Severity](./qa-fundamentals/priority-vs-severity.md) — the distinction most new QAs get backwards
- [Test Execution & Status Reporting](./qa-fundamentals/test-execution-and-status-reporting.md)

## 🐞 Defect & Test Management
- [Defect Life Cycle & Reporting](./defect-management/defect-life-cycle-and-reporting.md)
- [Defect Mapping to Requirements](./defect-management/defect-mapping.md)
- [Incident Reporting for QA](./defect-management/incident-reporting.md)
- [Jira for QA Teams](./defect-management/jira-for-qa.md)
- [Asana for QA Teams](./defect-management/asana-for-qa.md)
- [QA Project Management Fundamentals](./defect-management/qa-project-management.md)
- [Daily/Weekly/Monthly Status Reporting](./defect-management/status-reporting-cadences.md)
- [Stakeholder Management for QA Leads](./defect-management/stakeholder-management.md)

## 🧰 Framework Development & Design Patterns
- [Test Automation Framework Design Principles](./framework-development/framework-design-principles.md)
- [Design Patterns in Test Automation](./framework-development/design-patterns-in-automation.md) — Page Object, Factory, Singleton, Strategy, applied to test code specifically
- [Python Scripts to Automate the Boring Stuff](./framework-development/python-scripts-for-boring-automation.md) — file handling, report parsing, environment setup, CI helper scripts
- Deeper language-specific automation tracks (Selenium, Playwright, Karate, RestAssured, Cypress):
  [SDET / Automation Career Prep repo](https://github.com/abhibatsa/sdet-automation-career-prep) — cross-linked, not duplicated

## 🌐 Web, Mobile & API Testing
- [Web Automation, Testing & Debugging](./web-mobile-api/web-automation-testing-debugging.md) — browser dev tools, network tab, console debugging as a testing skill
- [Mobile App Automation & Testing](./web-mobile-api/mobile-app-automation-and-testing.md) — Appium fundamentals
- [Debugging with Android Studio](./web-mobile-api/debugging-with-android-studio.md) — Logcat, layout inspector
- [Debugging with Xcode](./web-mobile-api/debugging-with-xcode.md) — device logs, Instruments
- [API Testing, Automation & Debugging](./web-mobile-api/api-testing-automation-debugging.md)
- [Building a REST API for Test/Mock Purposes](./web-mobile-api/building-a-rest-api-for-testing.md) — when and how QA teams build their own mock/stub APIs

## 📊 Report Generation & Dashboards
- [Allure Reporting](./reporting/allure-reporting.md)
- [ReportPortal.io](./reporting/reportportal-io.md)
- [TestNG HTML Reports](./reporting/testng-html-reports.md)
- [JUnit Reporting](./reporting/junit-reporting.md)
- [Building Custom HTML Reports](./reporting/custom-html-reports.md)

## 📈 Log Monitoring & Assessment
- [Reading Server Logs Effectively](./log-monitoring/reading-server-logs.md)
- [Kibana Fundamentals for QA](./log-monitoring/kibana-fundamentals.md)
- [Splunk Fundamentals for QA](./log-monitoring/splunk-fundamentals.md)
- [ELK Stack Overview](./log-monitoring/elk-stack-overview.md)
- [Elasticsearch & KQL for Log Search](./log-monitoring/elasticsearch-and-kql.md)
- [Log Storage Patterns with S3](./log-monitoring/log-storage-with-s3.md)
- [Browser Dev Tools for Web Log Assessment](./log-monitoring/browser-dev-tools-for-logs.md)
- *(Deep SRE-style log-driven alerting and on-call practices live in the [Observability & Monitoring repo](https://github.com/abhibatsa/architecting-software) — this section covers log reading as a QA/debugging skill, not incident response)*

## 🗄️ Database & DSA for QA
- [Database Fundamentals for QA](https://github.com/abhibatsa/sdet-automation-career-prep/tree/main/07-database-fundamentals-for-sdets) — shared with the SDET repo
- [DSA Fundamentals for QA/SDET](https://github.com/abhibatsa/sdet-automation-career-prep/tree/main/08-data-structures-and-algorithms-for-sdets) — shared with the SDET repo

## 🤖 AI in QA / AI Test Engineering
- [AI QA Fundamentals](./ai-in-qa/ai-qa-fundamentals.md) — what changes when the system under test isn't deterministic
- [AI Automation](./ai-in-qa/ai-automation.md) — where AI genuinely speeds up test creation/maintenance vs hype
- [AI Testing](./ai-in-qa/ai-testing.md) — hallucination testing, RAG validation, guardrails, at reference depth
- [Integrating AI into Existing Test Frameworks](./ai-in-qa/ai-integration-into-existing-frameworks.md)
- [Choosing AI Models/LLMs for Test Engineering Tasks](./ai-in-qa/choosing-ai-models-for-test-engineering.md)
- [LLMs for Test Case Generation](./ai-in-qa/llms-for-test-case-generation.md)
- Deeper career-prep angle on all of this:
  [AI Test Engineering Career Prep repo](https://github.com/abhibatsa/ai-test-engineering-career-prep) *(private)* — cross-linked, not duplicated

## ✅ Interview Prep
- Full interview-prep track (level calibration, common questions, framework-design interviews):
  [SDET / Automation Career Prep repo](https://github.com/abhibatsa/sdet-automation-career-prep) — cross-linked, not duplicated
- [QA/QE-Specific Interview Questions](./interview-prep/qa-qe-specific-questions.md) — process/management questions (STLC, estimation, defect triage) that the SDET repo doesn't cover

## 📇 Related repos in this family
- [System Design & Architecture](https://github.com/abhibatsa/architecting-software) — includes Observability & Monitoring (SRE content lives there)
- [SDET / Automation Career Prep](https://github.com/abhibatsa/sdet-automation-career-prep) — automation framework depth, DSA, DB, coding-round prep
- [AI Test Engineering Career Prep](https://github.com/abhibatsa/ai-test-engineering-career-prep) *(private)* — AI-QA career-transition depth
- [LLD & OOD Interview Prep](https://github.com/abhibatsa/lld-and-ood-interview-prep) — design patterns referenced in the framework-development section above

## 📚 Books

- [Foundations of Software Testing: ISTQB Certification](https://link.amazon/B06ebBC0f)
- [Data Structures And Algorithms Made Easy -  Narasimha Karumanchi](https://amzn.to/45OnH5L)
- [Cracking The Coding Interview: 189 Programming Questions and Solutions-Paperback [Paperback] Gayle Laakmann McDowell](https://amzn.to/4xWQocB)
- [Head First Design Patterns: Building Extensible and Maintainable Object-Oriented Software, Second Edition (Grayscale Indian Edition) -  Eric Freeman](https://amzn.to/4qzMFPM)
- [Clean Code : Import Edition :Multi colour book: A Handbook of Agile Software Craftsmanship (Robert C. Martin Series)](https://amzn.to/45IWf9D)
- [Head First Java: A Brain-Friendly Guide, Third Edition (Grayscale Indian Edition)](https://link.amazon/B061FY2Qn)
- [Automate the Boring Stuff with Python, 3rd Edition: Practical Programming for Total Beginners](https://link.amazon/B0fbWI6Ot)

## 🤝 Contributing
See [CONTRIBUTING.md](./CONTRIBUTING.md).

## 📄 License
MIT
