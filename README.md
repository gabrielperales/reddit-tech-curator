# Reddit Tech Curator

A personal, read-only aggregation service designed to fetch and filter technical discussions from specific programming and engineering subreddits.

## Motivation
As a software engineer, I want to keep up with high-signal technical discussions, architectural patterns, and framework updates without getting distracted by the broader Reddit feed. This tool serves as a personal curation engine, polling only the most relevant threads based on specific technical keywords to help me stay updated efficiently.

## Architecture & Tech Stack
This project is built as a lightweight backend processor:
* **Core Language:** Elixir
* **Framework/Tooling:** Phoenix (utilizing background workers for rate-limited, scheduled polling)
* **Deployment:** Containerized via Docker for local execution on a personal Proxmox homelab.

## Scope and Limitations
* **Strictly Read-Only:** This application only consumes data via the Reddit API. It does not post, comment, upvote, send messages, or interact with the platform in any way.
* **Personal Use Only:** There is no commercial aspect, SaaS component, or public-facing frontend. Data is fetched and aggregated locally solely for personal review and reading.
* **Rate Limit Compliant:** Built to strictly adhere to Reddit's API rate limits using controlled background queues.

## Current Status
Currently in the architecture planning and initial setup phase. Awaiting API access approval from Reddit to begin testing the data ingestion workers.
