# Elastic Cloud Log Analytics Dashboard

This repository documents a software-service-construction proof of concept for
moving an operational ELK workload from an on-premises environment to Elastic
Cloud on AWS. The project included configuring a hosted deployment and building
a Kibana dashboard to summarize log activity.

## Business problem

The scenario involved a ten-person team maintaining an on-premises ELK stack.
Routine patching, vulnerability remediation, availability, and infrastructure
administration consumed time that could otherwise support product and service
work.

## Proof-of-concept scope

- Configure an Elastic Cloud deployment in AWS `us-east-1`.
- Access Kibana through the managed deployment.
- Ingest representative log data.
- Build a dashboard that summarizes operational activity.
- Compare a managed SaaS approach with continued on-premises maintenance.

## Architecture

```mermaid
flowchart LR
    A[Application logs] --> B[Elastic Cloud]
    B --> C[Elasticsearch]
    C --> D[Kibana dashboard]
    D --> E[Operational review]
```

## Findings

The proof of concept demonstrated how a managed Elastic deployment can reduce
direct responsibility for infrastructure patching and platform maintenance.
It also provides a centralized Kibana interface for exploring logs and sharing
operational views. A production decision would additionally require analysis of
data volume, retention, security controls, migration effort, and total cost.

## Repository contents

- [`docs/implementation-notes.md`](docs/implementation-notes.md): deployment and
  dashboard workflow
- [`docs/evaluation.md`](docs/evaluation.md): benefits, tradeoffs, and production
  considerations

Cloud credentials, account identifiers, deployment endpoints, and customer log
data are intentionally excluded.

## Tools

Elastic Cloud, Elasticsearch, Kibana, and AWS.

## Author

[Justin Spratt](https://github.com/justinspratt07)
