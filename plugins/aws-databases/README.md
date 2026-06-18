# aws-databases

## Overview

This plugin brings AWS database expertise directly into your coding assistant, covering relational, key-value, and wide-column workloads across the [AWS database portfolio](https://aws.amazon.com/products/databases/). Currently, skills are provided to assist with the following capability areas:

- **Relational (Aurora)** — Provision and manage Amazon Aurora PostgreSQL and MySQL clusters: ACU sizing, I/O-Optimized storage, commitment pricing, express configuration, pgvector, Babelfish, and upgrade planning.
- **In-memory (ElastiCache)** — Model data for Amazon ElastiCache (Valkey/Redis), build vector search and semantic caching for GenAI, monitor clusters, and migrate from self-managed Redis.
- **Wide-column (Keyspaces)** — Compatibility checks, pricing, connection troubleshooting, pre-warming, and SQL-to-CQL / Cassandra-to-Keyspaces migration for Amazon Keyspaces.
- **Data movement** — Export Amazon RDS and Aurora snapshots to Amazon S3 for analytics and archival.

> Looking for Amazon OpenSearch Service (search, log analytics, trace analytics)? It ships in the [aws-data-analytics](../aws-data-analytics/) plugin.

## Agent Skills

| # | Skill | Description | Documentation |
| -- | --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------- |
| 1 | `amazon-aurora-postgresql` | Provision and advise on Amazon Aurora PostgreSQL clusters — express configuration, ACU sizing, pgvector, Babelfish, upgrades | [SKILL.md](skills/amazon-aurora-postgresql/SKILL.md) |
| 2 | `amazon-aurora-mysql` | Provision and advise on Amazon Aurora MySQL clusters — ACU sizing, I/O-Optimized storage, parallel query, upgrades | [SKILL.md](skills/amazon-aurora-mysql/SKILL.md) |
| 3 | `creating-amazon-aurora-db-cluster-with-instances` | Create an Amazon Aurora DB cluster with instances following AWS-recommended procedures | [SKILL.md](skills/creating-amazon-aurora-db-cluster-with-instances/SKILL.md) |
| 4 | `amazon-elasticache` | Cache lifecycle for Amazon ElastiCache — data modeling, vector search, semantic caching, monitoring, migration | [SKILL.md](skills/amazon-elasticache/SKILL.md) |
| 5 | `amazon-keyspaces` | Compatibility, pricing, connection troubleshooting, pre-warming, and SQL-to-CQL migration for Amazon Keyspaces | [SKILL.md](skills/amazon-keyspaces/SKILL.md) |
| 6 | `exporting-rds-to-s3` | Export Amazon RDS and Aurora snapshots to Amazon S3 | [SKILL.md](skills/exporting-rds-to-s3/SKILL.md) |

## Install

### Claude Code

```
/plugin install aws-databases@claude-plugins-official
/reload-plugins
```

### Codex

In your terminal:

```
codex plugin marketplace add aws/agent-toolkit-for-aws
```

Then launch Codex and run `/plugins` to browse and install the **aws-databases** plugin.

## What's included

### AWS MCP Server

This plugin configures the [AWS MCP Server](https://docs.aws.amazon.com/agent-toolkit/latest/userguide/understanding-mcp-server-tools.html), which gives your agent real-time AWS documentation search, on-demand skill discovery and retrieval, authenticated access to AWS services through `call_aws`, and sandboxed Python script execution through `run_script`.
