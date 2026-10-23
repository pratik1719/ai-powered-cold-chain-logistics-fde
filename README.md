# AI powered Cold-Chain Logistics

An AI assistant for cold-chain logistics teams. It brings shipment telemetry and operational procedures together so teams can investigate risks and make decisions using natural-language questions.

The project follows the data from GPS, temperature, route, and truck telemetry into a SQL Server system, then adds an AI agent that can use operational tools and standard operating procedures (SOPs).

## Problem

Logistics teams often need to check several dashboards, query databases, and search procedure documents to understand whether a shipment needs attention. This project explores how an AI assistant can make that investigation more direct while keeping operational data and actions controlled.

## Features

- Ingests and organizes logistics SOP documents.
- Connects an agent to operational data through dedicated tools.
- Uses LangGraph to manage the agent’s workflow and state.
- Provides a Streamlit interface for interacting with the system.
- Records activity through an audit logging pipeline.
- Uses database roles and permissions to control access.
- Automates deployment to AWS EC2 through GitHub Actions.

## Architecture

```text
GPS, temperature, route, and truck telemetry
                    ↓
             SQL Server
                    ↓
       Agent tools and data queries
                    ↔
      LangGraph agent + SOP knowledge
                    ↓
             Streamlit UI
                    ↓
        Secure audit logging

       GitHub Actions → AWS EC2
