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
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global cloud data integration and ETL market is estimated at **$14B–$17B in 2025–2026** (projected to surpass $21B by 2028–2030 with ~10–13% CAGR), driven by enterprise cloud migrations and AI readiness demands. The sector is **moderately fragmented with a barbell concentration structure**: cloud hyperscalers (Microsoft, AWS, Google) and legacy enterprise suites (Informatica, Qlik) anchor core large-enterprise spend, while a highly competitive and fragmented tier of specialized SaaS startups and open-core innovators (Fivetran, Airbyte, Matillion, Hevo) capture dynamic modern data stack (MDS) workloads.

## SaaS/Hosted Platforms

| Product | Company Scale (Valuation / Revenue) | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------------------------------|-------------|-------------------|--------------------------|
| **[Azure Data Factory](https://azure.microsoft.com/en-us/products/data-factory/)** | Microsoft: **$3.1T+ Market Cap** (~$245B+ Annual Rev) | Cloud ETL/ELT orchestration service integrating data across hybrid storage. Consumption-metered by pipeline runs, DIU copy hours, and Spark vCores. | **$0.25/DIU-hour** (data movement) + **$0.274/vCore-hour** (data flows) + **$1.00/1,000 cloud activity runs** | **Always-free tier**: 5 low-frequency activity runs/month; **30-day free trial**: $200 Azure cloud credits |
| **[AWS DMS](https://aws.amazon.com/dms/)** | Amazon / AWS: **$2.0T+ Market Cap** (~$105B+ AWS Annual Rev) | Managed database migration and replication service supporting continuous CDC replication to AWS data lakes and warehouses. | **$0.065/hour** (~$47/month for `dms.t3.medium`) or **$0.0384/hour** (for `dms.t3.small`) + $0.115/GB-month storage | **AWS Free Tier (12 months)**: 750 hours/month of Single-AZ replication instance (`dms.t3.micro`/`dms.t3.small`) + 50GB storage |
| **[Zoho DataPrep](https://www.zoho.com/dataprep/)** | Zoho Corp: **~$12B–$15B Est. Valuation** (~$1.5B FY25 Revenue) | Self-service data preparation, cleaning, and pipeline integration platform with 250+ transforms and reverse-ETL connectors. | **$40/month** (billed annually) for Standard plan (2M rows/month, 3 users) | **Free plan**: 20,000 rows/month, 1 user, 1-month audit log retention; **15-day free trial** of paid plans |
| **[Stitch Data](https://www.stitchdata.com/)** | Qlik / Thoma Bravo: **~$10B Valuation** (~$1B+ Revenue) | Simple, developer-focused cloud ELT platform extracting data from SaaS applications and databases into warehouses. | **$100/month** for Standard plan (5M rows/month, 1 destination, up to 10 sources) | **14-day free trial**: unlimited rows and connections, no credit card required |
| **[Talend (Qlik Talend Cloud)](https://www.talend.com/)** | Qlik / Thoma Bravo: **~$10B Valuation** (~$1B+ Revenue) | Enterprise data integration, quality governance, and pipeline transformation suite across multi-cloud environments. | **$6,000/year** (~$500/month) for Starter plan (up to 50GB/month data volume) | **14-day free trial**: full cloud platform features, no credit card required |
| **[Informatica Cloud Data Integration](https://www.informatica.com/)** | Informatica: **~$7.6B–$8.0B Valuation** (~$1.6B+ Revenue) | Enterprise-grade iPaaS and ETL platform featuring extensive governance, enterprise connectors, and automated mapping pipelines. | **$1,098/IPU-year** (~$91.50/IPU-month; standard AWS Marketplace entry at $131,760/year for 120 IPUs/month) | **CDI-Free plan**: 20M rows/month, 10 compute hours/month, 25 IPUs/month (requires corporate work email); **30-day free trial** |
| **[Fivetran](https://www.fivetran.com/)** | Fivetran: **$5.6B Valuation** (~$300M+ ARR; merged with dbt Labs) | Fully managed automated ELT platform featuring 700+ connectors with automated schema drift detection and in-warehouse transformation. | **$5/month base charge** per connection (generating 1–1M MAR) on Standard pay-as-you-go | **Free plan**: 500,000 MAR/month for connectors, 3,500 MAR/month for reverse ETL activations, 5,000 monthly model runs for dbt transformations; **14-day free trial** |
| **[Airbyte](https://airbyte.com/)** | Airbyte: **$1.5B Valuation** (Series B Unicorn) | Open-core ELT engine with managed cloud hosting, credit-based volume scaling, and 300+ community and native connectors. | **$20/month** for Standard plan (includes 5 credits, $5/additional credit) | **Free plan (Airbyte Cloud)**: 1,000 Action Operations (AOs)/month, single user; **30-day free trial** with $500 free credits |
| **[Matillion](https://www.matillion.com/)** | Matillion: **$1.5B Valuation** (Series E Unicorn) | Warehouse push-down ELT and transformation engine designed natively for Snowflake, Databricks, Redshift, and BigQuery. | **~$2.00–$2.50/credit** via credit packages (Teams tier typically starts around ~$20,000/year; 1 credit/task-hour for orchestration, 3 credits/task-hour for transform) | **14-day free trial**: 500 free credits included, full platform capabilities |
| **[Hevo Data](https://hevodata.com/)** | Hevo Data: **~$300M–$400M Est. Valuation** (~$35M–$45M ARR, $43M funded) | Real-time, no-code data pipeline and replication platform offering fault-tolerant ELT ingestion from 150+ sources. | **$265/month** (billed annually, or $299/month monthly) for Starter plan (5M events/month, 10 users) | **Free plan**: 1,000,000 events/month, unlimited free sources, up to 5 users; **14-day free trial** of paid features |

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
