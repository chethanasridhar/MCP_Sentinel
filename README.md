# MCP Sentinel

A voice-approved safety gateway for AI agents.

Built for wHACKiest 2026 (CodeRIT, Ramaiah Institute of Technology), Track 1: Make MCP Matter.

> Status: Round 1 blueprint. This repository holds the design only. Code will be added in the 24-hour offline round.

## The problem

AI agents now pay, send messages and delete files for us through MCP tools. An agent cannot reliably tell data from instructions, so hidden text in a document, a message or a tool description can make it act against its owner. Security gateways for MCP exist, but they are built for engineers. A shopkeeper cannot read a JSON approval pop-up.

## What MCP Sentinel does

Sentinel sits between any AI agent and its MCP servers.

- Safe tool calls pass through.
- Risky calls are paused, and the owner is asked by voice in Hindi, Kannada or English: "Your assistant wants to send ₹5,000 to a new payee. Say four-seven to approve."
- Dangerous calls are blocked.
- Every action is logged, and data changes can be undone with one tap.

## How it works

```
AI agent  <-->  MCP Sentinel  <-->  MCP servers (files, messaging, calendar, sandbox UPI)
                 1. scope check
                 2. injection scan
                 3. chain risk score
                     |         |
          voice approval     audit log + undo snapshots
       (ElevenLabs, phone)   (AWS: API Gateway, Lambda, DynamoDB, S3)
```

## Documents

| File | Contents |
|---|---|
| [architecture.md](architecture.md) | Components, request flow, permission scopes, risk scoring, voice approval, rollback, audit log |
| [threat-model.md](threat-model.md) | The four threats we handle, how, and what we do not cover |

## Planned stack

| Layer | Tools |
|---|---|
| Gateway | Python, official MCP SDK, FastAPI |
| Detection | Rule patterns, LLM judge on Amazon Bedrock |
| Voice | ElevenLabs text-to-speech and Scribe speech-to-text |
| Cloud | AWS API Gateway, Lambda, DynamoDB, S3 |
| Phone app | React web app |


