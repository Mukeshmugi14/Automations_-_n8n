# MoodMetrics – Sentiment Analysis Automation

Workflow that takes text data (reviews, comments, etc.), classifies sentiment, and outputs simple bar chart-ready counts.

## Features

- Batch sentiment detection via LLM or classifier API
- Aggregates counts: positive, neutral, negative
- Output usable by dashboards (e.g. Metabase, Grafana, Google Sheets)

## Input Example

```json
{
  "items": [
    "The product is amazing!",
    "Service was okay.",
    "This is terrible, I want a refund."
  ]
}
