SPECIFIC AIMS

Proprietary clinical registries—whether vendor-hosted oncology platforms, hospital-built dashboards, or direct-to-patient “digital binders”—have become the dominant mechanism for aggregating longitudinal cancer data, yet they remain technological silos. Most store records in idiosyncratic schemas, export flat files only once or twice per year, and require expensive licenses that safety-net and rural practices cannot afford. Even registries marketed as “FHIR-enabled” typically bolt a thin API onto a legacy database and still depend on brittle extract–transform–load (ETL) scripts that fracture provenance and delay discovery. The result is stalled reproducibility in multi-site studies, sluggish accrual to pragmatic trials, and biased training corpora for AI models. A truly native-FHIR, FAIR-compliant registry—capable of ingesting domain guides such as the minimal Common Oncology Data Elements (mCODE), free of license fees, and simple enough for small practices to deploy—is urgently needed

I propose to develop FHIR-Native Open Registry & Knowledge Repository (FHIR-ORKR)—an Apache-licensed, cloud-hosted toolkit that ingests patient-level data as canonical FHIR R5 resources (including mCODE-conformant oncology records), exposes them through modern REST and Bulk-Data APIs, and layers computable knowledge objects (phenotypes, outcome rules, AI feature stores) with machine-actionable provenance. FHIR-ORKR directly addresses RFA-OD-24-010, “Building Sustainable Software Tools for Open Science,” and operationalizes Goals 3 (FAIR, sustainable software) and 4 (federated infrastructure) of the NIH Strategic Plan for Data Science 2025-2030. Where specialized expertise is required (e.g., DevOps hardening or usability testing), I will engage short-term contractors under my direction.

Central hypothesis. A rigorously engineered, standards-native, open-source registry will (i) cut the cost and time needed to establish interoperable data infrastructure, (ii) broaden research participation among under-resourced sites, and (iii) accelerate AI/ML model development through first-class provenance and computable metadata. I will test this hypothesis through three aims:

Aim 1 – Architect and implement the FHIR-native data & terminology layer
• Profile core FHIR R5 resources—Patient, Encounter, Observation, Condition, Medication, Procedure—and explicitly incorporate the oncology-specific mCODE FHIR profiles; bind standard terminologies (SNOMED CT, LOINC, RxNorm).
• Release schema, JSON-Schema validations, and conformance tests in a public GitHub repository.
• Outcome: ≥ 95 % pass rate on Inferno+/FHIR test harness (including mCODE test bundles); openly citable schema (Zenodo DOI).

Aim 2 – Build and harden the cloud-hosted, open-source registry & knowledge repository
• Containerize micro-services (Docker/Helm), automate CI/CD, and publish a software bill-of-materials (SBOM) for supply-chain security.
• Implement a knowledge layer storing computable phenotypes (CQL), outcome rules, and AI-ready feature vectors—with RO-Crate metadata and native support for mCODE-based oncology phenotypes.
• Outcome: end-to-end ingest → query latency < 2 s for a 1 M-record synthetic cohort; OpenSSF Scorecard “passing” badge.

Aim 3 – Demonstrate value, generalizability, and sustainability across one external pilot site
• Deploy FHIR-ORKR on NIH STRIDES-eligible clouds at one partner institution; load ≥ 5K real-world records, including mCODE-conformant oncology subsets.
• Establish governance, contributor guidelines, and a community roadmap; disseminate via JOSS and webinars.
• Outcome: ≥ 1 000 unique external API calls /month, two merged community pull-requests, and a CoreTrustSeal-ready operations manual.

Expected impact. FHIR-ORKR will be the first production-grade, FHIR-native, FAIR4RS-compliant registry—fully accommodating key guides such as mCODE—that any institution can deploy or query freely. By lowering infrastructural barriers and embodying NIH best practices for sustainable open-science software, the project will accelerate equitable data sharing, catalyze multi-site studies, and provide a trusted substrate for transparent, reproducible AI in health research.