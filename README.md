# Awesome-Cloud-Data-Migration-ETL

## Top Cloud Data Migration & ETL Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Data Pipeline Automation, ELT/ETL Orchestration & Cloud Warehouse Ingestion*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Data Migration & ETL**. These tools help organizations move and transform data between sources (databases, SaaS apps, APIs, files) and destinations (data warehouses, lakes, and operational systems)—covering batch ELT, CDC replication, and transformation-in-warehouse workflows.

**Examples** include Fivetran, Stitch Data, Airbyte, Matillion, AWS DMS, Azure Data Factory, Hevo Data, Informatica Cloud Data Integration, Talend, and Zoho Data Migration (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted data integration, open-source ELT engines, and CDC replication frameworks—ideal for data engineers, platform teams, and organizations seeking transparent, vendor-neutral pipelines without per-row or per-credit billing surprises.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Fivetran](https://www.fivetran.com/)** | Managed ELT platform with 700+ connectors for SaaS apps, databases, and files. Usage is measured in Monthly Active Rows (MAR); initial syncs and unchanged rows are excluded. As of January 2026, deletes count toward paid MAR, and a $5 minimum charge applies to standard connections generating between 1 and 1M MAR . | Pay-as-you-go (Standard); $5 minimum base charge per connection generating 1–1M MAR [citation:1][citation:11] | **Free plan**: entirely free, no base charge, includes 5,000 monthly model runs for transformations; no overage available [citation:1] |
| **[Stitch Data (Qlik)](https://www.stitchdata.com/)** | Managed ELT service focused on extracting and loading data into supported warehouses using row-based pricing. Requires downstream transformation tooling. Often paired with Talend for transformation within the Qlik ecosystem . | Advanced: $1,500/month (annual commitment ~$18,000); Premium: $3,000/month (annual ~$36,000) [citation:2] | **14-day free trial**; no permanent free tier listed [citation:2] |
| **[Airbyte](https://airbyte.com/)** | Open-core data integration platform (self-hosted OSS free) with managed cloud offering. Cloud plans use credit-based volume pricing for Standard/Plus and capacity-based Data Workers for Pro/Enterprise Flex . | Standard: $20/month (5 credits included, extra $5/credit); Plus: from $189/month (40 credits)  | **Free plan**: 1,000 AOs/month, single user, API/MCP access, daily context store refresh; **30-day free trial** for Standard [citation:3] |
| **[Matillion (Maia)](https://www.matillion.com/)** | Cloud-native ELT/ETL with transformation pushed down to the target warehouse (Snowflake, Databricks, Redshift, BigQuery). Billed in credits per task hour: 1 for orchestration, 3 for transformation, 1–2 for CDC streams. Third-party listings cite ~$2.00 per credit . | Credit-based; ~$2.00/credit (third-party listing); fixed annual credit packages [citation:4] | No free tier or self-serve trial listed; demo via sales |
| **[AWS DMS](https://aws.amazon.com/dms/)** | Managed database migration and replication service. Supports provisioned replication instances or Serverless (DCU-hours). Billed per instance-hour or DCU-hour plus storage ($0.115/GB-month). Data transfer charges apply separately for cross-region replication . | dms.t3.medium: ~$47/month; dms.r5.large: ~$190/month (us-east-1 list) [citation:5] | No permanent free tier; AWS Free Tier credits may apply for new accounts |
| **[Azure Data Factory](https://azure.microsoft.com/en-us/products/data-factory/)** | Cloud ETL/ELT orchestration service. Consumption-based billing across four meters: orchestration activity runs, data movement (DIU-hours for Copy), Mapping Data Flows (vCore-hours), and SSIS IR runtime. Costs vary significantly by pipeline frequency and parallelism . | Consumption-based; no single flat cost  | No permanent free tier; Azure free account credits may apply |
| **[Hevo Data](https://hevodata.com/)** | Managed ELT platform with 150+ connectors. Pricing based on monthly Events (rows processed). Free Sources included in all paid plans; paid Sources require upgrade . | Starter: includes 5M Events (adjustable); Professional: includes 20M Events [citation:7] | **Free plan**: 1M Events/month, unlimited Free Sources, unlimited Models, no credit card required; **14-day free trial** for paid features [citation:7] |
| **[Informatica Cloud Data Integration](https://www.informatica.com/)** | Enterprise iPaaS with broad connectivity and governance. Priced on IPU (Informatica Processing Unit) consumption with volume tier discounts. MDM is quoted separately per domain record. Complex UI and steep learning curve noted by reviewers . | Quote-only (IPU consumption model) [citation:8] | No free tier; trial via sales |
| **[Talend (Qlik Talend Cloud)](https://www.talend.com/)** | Enterprise data integration and governance platform. Four editions: Starter, Standard, Premium, Enterprise. Starter metered on data volume; Premium+ add job executions and duration. Talend Open Studio free edition retired January 2024 . | Starter: $6,000/year (up to 50GB/month, overage billed separately) [citation:9] | **14-day free trial** (no credit card); no permanent free tier [citation:9] |
| **[Zoho Data Migration](https://www.zoho.com/)** | Data migration services and tools within the Zoho ecosystem. Implementation and migration are typically quoted separately from license pricing, often $1,500–$12,000 depending on data volume and source cleanliness . | Quote-only (migration services priced separately from Zoho licenses) [citation:10] | Contact Zoho for migration trial/evaluation options |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Airbyte (OSS)](https://github.com/airbytehq/airbyte)** | [![Stars](https://img.shields.io/github/stars/airbytehq/airbyte?style=social&color=white)](https://github.com/airbytehq/airbyte/stargazers) | Open-source data integration platform with 300+ connectors. Self-managed deployment is free forever; the same codebase powers Airbyte Cloud. The reference implementation for open-source ELT. |
| **[Apache Airflow](https://github.com/apache/airflow)** | [![Stars](https://img.shields.io/github/stars/apache/airflow?style=social&color=white)](https://github.com/apache/airflow/stargazers) | Programmatic workflow orchestration for data pipelines. DAG-based scheduling with Python; widely used as the orchestration layer above ETL/ELT tools. |
| **[dbt (data build tool)](https://github.com/dbt-labs/dbt-core)** | [![Stars](https://img.shields.io/github/stars/dbt-labs/dbt-core?style=social&color=white)](https://github.com/dbt-labs/dbt-core/stargazers) | SQL-based transformation framework for data warehouses. Handles the "T" in ELT; pairs with Fivetran, Airbyte, and Stitch for the "EL" layer. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Debezium](https://github.com/debezium/debezium)** | [![Stars](https://img.shields.io/github/stars/debezium/debezium?style=social&color=white)](https://github.com/debezium/debezium/stargazers) | Open-source CDC (change data capture) platform for databases (PostgreSQL, MySQL, MongoDB, etc.). Streams row-level changes to Kafka and downstream consumers. |
| **[Kafka Connect](https://github.com/apache/kafka)** | [![Stars](https://img.shields.io/github/stars/apache/kafka?style=social&color=white)](https://github.com/apache/kafka/stargazers) | Framework for streaming data between Kafka and external systems. Source and sink connectors enable scalable, fault-tolerant data pipelines. |
| **[Meltano](https://github.com/meltano/meltano)** | [![Stars](https://img.shields.io/github/stars/meltano/meltano?style=social&color=white)](https://github.com/meltano/meltano/stargazers) | Open-source ELT platform built on Singer taps and targets. Provides a CLI and web UI for managing extraction and loading pipelines. |
| **[Singer](https://github.com/singer-io)** | [![Stars](https://img.shields.io/github/stars/singer-io?style=social&color=white)](https://github.com/singer-io/stargazers) | Open-source standard for writing data extraction (taps) and loading (targets) scripts. The foundation for Meltano and many custom ELT pipelines. |

**Frameworks for building custom systems**: Combine **Airbyte OSS** for managed connectors, **Debezium** for CDC replication, **dbt Core** for warehouse transformations, and **Apache Airflow** or **Meltano** for orchestration—creating a fully self-hosted ELT stack with no per-row or per-credit billing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Data migration and ETL tools handle sensitive business data; enforce encryption in transit, least-privilege source credentials, and audit logging for pipeline changes.
- Pricing models (MAR, credits, DCU-hours, Events, IPU) vary dramatically and can produce unpredictable bills at scale; model total cost against actual data volume and change frequency before committing to annual contracts.

---

**Made for data engineers, analytics engineers, platform teams, and developers building data pipelines.**  
Let's make cloud data migration and ETL more open, observable, and cost-predictable.
