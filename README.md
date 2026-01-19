# Data Observability & Reliability Framework

## Overview
This project implements a data observability framework designed to detect
data quality issues, pipeline failures, and anomalies before they impact
downstream consumers.

## Architecture
"C:\Users\balas\OneDrive\Desktop\Github projects\data-observability-reliability-framework\architecture.png"

## Tech Stack
- Great Expectations
- Apache Airflow
- Python
- Prometheus
- Grafana
- Slack API

## Data Flow
1. Data pipelines execute ingestion and transformation jobs.
2. Post-load data quality checks are triggered automatically.
3. Metrics are emitted for monitoring.
4. Dashboards visualize pipeline health.
5. Alerts notify stakeholders when issues occur.

## Challenges & Debugging

### Silent Data Corruption
- Issue: Pipelines succeeded but data was incorrect.
- Debugging: Compared historical row counts and freshness metrics.
- Fix: Added row-count and freshness validation checks.

### Alert Fatigue
- Issue: Too many false-positive alerts.
- Debugging: Reviewed alert frequency patterns.
- Fix: Tuned alert thresholds dynamically.

## Data Quality & Reliability
- Schema and freshness validation
- Anomaly detection
- Root-cause analysis support

## Learnings
- Pipeline success does not guarantee data correctness.
- Observability is critical for reliable data systems.
