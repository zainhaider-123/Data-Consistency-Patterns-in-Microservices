### 3.1 Eligibility criteria

**Inclusion criteria:**

- Peer-reviewed journal articles or peer-reviewed conference papers.
- Published from 1 January 2018 through the final search date in 2026: **[Final search date to be recorded]**.
- Written in English.
- Addresses data consistency across microservices through an identifiable pattern, architectural approach, or coordination mechanism.
- Provides sufficient methodological or technical detail about at least one of the following: the pattern and its consistency guarantees; factors influencing selection; evaluation methods and reported trade-offs; or implementation challenges and research gaps.

Eligibility will not require empirical evaluation if a primary study otherwise meets these criteria. Whether and how a proposed pattern is evaluated will be extracted and considered in the synthesis.

**Exclusion criteria:**

- Surveys, systematic reviews, mapping studies, position papers, and opinion pieces.
- Industry whitepapers, blog posts, technical reports, theses, and non-peer-reviewed preprints.
- Papers addressing data consistency solely within a single service or database, without a connection to consistency across microservices.
- Papers discussing microservices without sufficient detail about data consistency patterns or mechanisms.
- Short papers under four pages, extended abstracts, and posters.
- Papers with insufficient methodological or technical detail to address any research question.

### 3.2 Information sources

Five bibliographic sources will be searched:

1. ACM Digital Library
2. IEEE Xplore
3. Scopus
4. ScienceDirect (Elsevier)
5. SpringerLink

The search date, query, filters, and number of retrieved records will be recorded for each source. The final search date will define the publication cutoff in 2026.

### 3.3 Search strategy

The search strategy will target two concept blocks combined with AND:

- **Block 1:** Microservices terminology.
- **Block 2:** Data consistency terminology and relevant pattern or coordination terminology.

The exact Boolean string and any named-pattern terms remain to be finalized. The canonical string will be stored in `02-searches/search-string-canonical.txt`, with source-specific adaptations in dated files in the same folder. Search fields and supported syntax will be documented for each source.

The search will support identifying patterns broadly so that the most frequently reported ones can be established from the included studies. It will not require selection factors, evaluation outcomes, or research gaps to appear in the search terms for every retrieved paper.

### 3.4 Study records

**Data management:** Records will be exported from each source in BibTeX or RIS format and deduplicated. Source provenance and screening decisions will be retained to support the reporting of study selection.

**Selection process:** Two reviewers (Zain Haider and Ashok Kumar) will independently screen records at the title/abstract and full-text stages. Disagreements will be resolved through discussion. Reasons for exclusion at the full-text stage will be recorded.

**Data collection process:** Two reviewers will independently extract data from all included studies into a shared structured form. Differences will be resolved through discussion. Information that a study does not report will be marked as “not reported.”

### 3.5 Data items

The extraction form will capture:

- **Bibliographic information:** Title, authors, publication year, venue, and DOI or other identifier.
- **Study characteristics:** Study type, objectives, application domain, system context, and evaluation setting, where reported.
- **Patterns and guarantees (RQ1):** Pattern names, definitions, mechanisms, combinations with other patterns, stated consistency guarantees, assumptions, and conditions under which guarantees apply. Stated guarantees will be distinguished from guarantees supported by evaluation or formal analysis.
- **Selection factors (RQ2):** Reported technical, organizational, and economic reasons for selecting or rejecting a pattern, including context and alternatives considered.
- **Evaluation and trade-offs (RQ3):** Evaluation method, implementation or prototype, workload, system scale, comparison baseline, metrics, measurement conditions, and reported results concerning consistency, performance, availability, scalability, and operational complexity.
- **Challenges and gaps (RQ4):** Reported implementation difficulties, limitations, threats to validity, unresolved challenges, and proposed future work.

Pattern names and terminology will be retained as reported. Where different terms are grouped under a common category, the grouping and its justification will be documented. Research gaps explicitly reported by authors will be distinguished from gaps identified through the review synthesis.

### 3.6 Outcomes and prioritization

Primary synthesis outputs, mapped to the research questions, will be:

- A catalogue of data consistency patterns and their reported guarantees, including their frequency across included studies (RQ1).
- A classification of technical, organizational, and economic selection factors (RQ2).
- A synthesis of evaluation methods, metrics, benefits, limitations, and trade-offs (RQ3).
- A synthesis of implementation challenges and research gaps (RQ4).

Frequency will be reported as the number of included studies addressing each pattern. A study addressing multiple patterns may contribute to more than one category. Counts will describe the reviewed evidence base and will not establish that a pattern is superior or more widely adopted in practice.

### 3.7 Quality and risk-of-bias assessment

A quality/risk-of-bias assessment will be applied to each included study by two independent reviewers. Differences will be resolved through discussion. The instrument and its application rules will be described in `06-risk-of-bias/rob-instrument.md`.

**Pending specification:** The assessment questions, scoring rules, and any consequences for study inclusion or synthesis have not yet been specified. These details must be documented before the assessment is applied.

### 3.8 Data synthesis

Narrative synthesis is planned, organized by research question (RQ1–RQ4), with thematic coding for qualitative data on patterns, selection factors, trade-offs, challenges, and research gaps.

Descriptive counts will summarize the frequency of patterns within the included literature. The synthesis will give particular attention to the most frequently reported patterns while retaining other eligible patterns in the evidence catalogue.

Reported guarantees and outcomes will be interpreted alongside study context, assumptions, evaluation design, and quality assessment. Studies proposing an approach without evaluation will be distinguished from studies providing evaluation evidence. Missing organizational or economic evidence will be reported as missing rather than inferred from technical results.

Quantitative synthesis through meta-analysis is not planned because the studies are expected to differ in patterns, consistency guarantees, system scale, workloads, metrics, and evaluation methods. Quantitative results will be summarized with their measurement context.

### 3.9 Meta-bias and certainty

Potential reporting bias will be considered by examining whether studies report negative or null results and limitations, and by comparing stated aims with reported outcomes. Limitations arising from the selected publication types, language, sources, and publication period will be discussed.

Confidence in the synthesis will be discussed narratively, considering study quality, consistency of findings, relevance to the review questions, and the amount and precision of supporting evidence. No formal certainty-grading framework has been specified.

### 3.1 Eligibility criteria (PRISMA-P item 8 / PRISMA 2020 item 5)

**Inclusion criteria:**

- **IC1 — Publication type:** Peer-reviewed primary research published in a journal or conference proceedings, presenting an original data consistency approach, implementation, analysis, or evaluation. Workshop papers qualify when peer reviewed, published in proceedings, and meeting all other criteria.

- **IC2 — Publication period:** First formal publication of the report, including an online-first journal version, falls between 1 January 2018 and the final search date in 2026. The actual cutoff date will be recorded.

- **IC3 — Language and length:** Full text is in English and contains at least four pages of main article content, excluding reference-only pages and supplementary material.

- **IC4 — Microservice context:** Explicitly studies data consistency in microservices or concretely applies the proposed approach to a microservice system. Generic distributed-system or service-oriented approaches qualify only when a worked microservice application is provided. Incidental mentions or claims of potential applicability are insufficient.

- **IC5 — Data consistency focus:** Addresses maintaining, coordinating, restoring, or reasoning about data consistency across microservice boundaries. Relevant concerns include distributed transactions, cross-service data updates, replicated data, and consistency of service-owned read models. The approach must have an explicit connection to data consistency.

- **IC6 — Relevance to the research questions:** Provides extractable information about at least one of the following:
  - A data consistency pattern or mechanism and its intended guarantees or behaviour (RQ1).
  - Technical, organizational, or economic factors influencing pattern selection (RQ2).
  - Evaluation methods, benefits, limitations, or trade-offs concerning consistency, performance, availability, scalability, or operational complexity (RQ3).
  - Implementation or evaluation challenges and research gaps (RQ4).

- **IC7 — Assessable technical detail:** The accessible full text identifies the microservice context, consistency concern, and relevant pattern or mechanism in sufficient detail for extraction. A study need not use the word “pattern” if its mechanism is identifiable. Empirical evaluation, formal proof, industrial deployment, public artifacts, and answers to every RQ are not mandatory.

**Exclusion criteria:**

- **EC1 — Secondary or non-research contributions:** Surveys, systematic reviews, mapping studies, tutorials, and position or opinion papers without an eligible original research contribution. Secondary studies may inform the background but will not enter the primary-study synthesis.

- **EC2 — Ineligible publication type:** Non-peer-reviewed preprints, whitepapers, blogs, technical reports, theses, extended abstracts, posters, and other publications failing IC1.

- **EC3 — Date, language, or length:** Reports outside the specified publication window, non-English full texts, or reports below the minimum main-text length.

- **EC4 — Insufficient microservice context:** Generic database, cloud, distributed-system, or service-oriented studies without the concrete microservice context required by IC4.

- **EC5 — No cross-service consistency concern:** Studies addressing only internal single-service transactions, database internals, deployment, resource allocation, or other concerns without a connection to data consistency across microservices.

- **EC6 — Pattern terminology without relevant substance:** Papers mentioning consistency or named approaches only incidentally. Studies of Saga, CQRS, event sourcing, messaging, or similar approaches are excluded when they provide no substantive connection to data consistency. Naming a pattern alone does not establish eligibility.

- **EC7 — Insufficient extractable detail:** Full texts that do not provide enough technical or methodological information to establish the microservice context, consistency concern, and relevant approach, or to extract evidence for any RQ. Missing benchmarks, numerical results, formal proofs, tool versions, or public artifacts alone are not grounds for exclusion.

**Application rules:**

All inclusion criteria must be met; meeting any exclusion criterion results in exclusion. Studies need to address at least one RQ, rather than all four. Uncertain title/abstract records will proceed to full-text screening.

Eligibility will not depend on a pattern being considered common beforehand. The most commonly reported patterns will be identified from their frequency across included studies; less frequently reported eligible patterns will remain in the evidence catalogue.

Consistency models, such as eventual or strong consistency, will be distinguished from the patterns and mechanisms used to achieve them. Proposed guarantees will be distinguished from guarantees supported by formal analysis or empirical evaluation. Unevaluated proposals may be included but will not be treated as evidence of demonstrated effectiveness.

Duplicate records will be removed before screening. Related reports of one underlying study will be linked, with the most complete report supplying the main evidence and unique information retained from companion reports. Multiple reports of the same study will not be counted as independent studies when determining pattern frequency.

Unretrievable reports will be recorded separately from assessed full-text exclusions. Full-text exclusion reasons and reviewer disagreements will be documented; disagreements will be resolved through discussion.

## 4. Reporting

The completed review will be reported using the applicable PRISMA 2020 checklist items, with a completed checklist and a PRISMA 2020 flow diagram. Non-applicable items will be identified and explained. Findings will be organized around RQ1–RQ4. This review is prepared as a coursework assignment.

## 5. Replication package

A replication package containing search strings, search dates and filters, screening logs, full-text exclusion reasons, extraction data, quality/risk-of-bias assessments, and the completed PRISMA checklist will be compiled in `09-supplementary/`.

Protocol amendments and substantive methodological decisions will be recorded in `00-admin/decision-log.md`. File paths in this protocol identify planned storage locations; they do not indicate that the referenced files or activities already exist.