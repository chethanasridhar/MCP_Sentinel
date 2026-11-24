# 🛡️ MCP Sentinel
### A Voice-Approved Safety Gateway for AI Agents

**Built for wHACKiest 2026 | CodeRIT – Ramaiah Institute of Technology**  
**Track 1: Make MCP Matter**

---

## 💡 About the Project

AI agents are becoming increasingly capable of performing everyday tasks such as sending messages, processing payments, managing files, and accessing personal information. However, giving AI agents access to these tools also introduces security risks.

**MCP Sentinel** is a safety gateway that sits between AI agents and their MCP servers, monitoring tool calls, identifying potentially harmful actions, and ensuring that users remain in control.

Instead of blindly trusting an AI agent, Sentinel adds an additional layer of protection through risk assessment, permission controls, and voice-based human approval.

Our goal is simple: **Make AI agents safer to use, without taking control away from people.**

## 🚨 The Problem

An AI agent might be asked to summarize a document, but the document could contain hidden malicious instructions telling the agent to send private information to an external server.

Without proper safeguards, the agent may execute these instructions through its connected tools.

This creates risks such as:
- Unauthorized payments and transactions.
- Accidental deletion or modification of important data.
- Exposure of sensitive personal information.
- Malicious instructions hidden inside documents or external content.
- Unsafe sequences of tool calls.

## ⚙️ Our Solution

MCP Sentinel acts as an intermediary between AI agents and their connected tools.

It:
- Inspects incoming tool calls and sequences of actions.
- Detects suspicious instructions and potentially unsafe behaviour.
- Assigns risk scores to requested actions.
- Enforces permission scopes for individual tools.
- Requests human approval through voice for high-risk actions.
- Maintains an audit trail of executed and blocked actions.
- Supports rollback through saved state snapshots.

## 🔄 How It Works

1. **Agent Request:** An AI agent requests access to an MCP tool.
2. **Interception:** Sentinel intercepts the request before execution.
3. **Risk Assessment:** The request is checked for suspicious behaviour, permissions and potential threats.
4. **Decision:** Low-risk actions proceed, while high-risk actions are paused.
5. **Voice Approval:** The user receives a spoken approval request through ElevenLabs.
6. **Execution:** The action proceeds only after the required approval.
7. **Audit & Recovery:** The action is recorded, and supported state changes can be rolled back.

## 🏗️ Tech Stack

| Component | Technology |
|---|---|
| Backend | Python, FastAPI |
| Agent-Tool Communication | Model Context Protocol (MCP), Official MCP SDK |
| Risk Detection | Rule-based checks, LLM |
| LLM Integration | Amazon Bedrock |
| Voice Interaction | ElevenLabs |
| Cloud Infrastructure | AWS |
| Audit Storage | DynamoDB / S3 |
| Frontend | React |

## 🔐 Key Features

**1. Risk-Based Action Monitoring**  
Evaluates tool calls and identifies potentially dangerous actions before execution.

**2. Permission Scopes**  
Provides tool-level permissions to restrict what an AI agent can access or modify.

**3. Voice-Based Human Approval**  
Uses ElevenLabs to communicate high-risk actions and request explicit user confirmation.

**4. Audit Trail**  
Records tool calls, risk assessments, approval decisions and execution outcomes.

**5. Rollback Support**  
Uses state snapshots to support recovery from supported actions.

**6. Prompt Injection Detection**  
Identifies suspicious instructions embedded in external content that could manipulate agent behaviour.

## 🎯 Target Users

MCP Sentinel is designed for everyday users who rely on AI assistants to perform tasks on their behalf.

- **Small Business Owners:** Protect against unauthorized payments, messages and business operations.
- **Caregivers:** Maintain control over AI assistants managing reminders, communication and daily tasks.
- **AI Developers & Companies:** Add a safety layer between AI agents and their connected tools.

## 🌱 Future Scope

- Support for more Indian languages.
- WhatsApp-based approval notifications.
- Integration with additional MCP servers and AI agents.
- More advanced detection of malicious tool chaining.
- Expanded rollback and recovery capabilities.
- Customizable security policies for different users.

## 🚀 Vision

We believe AI should be capable of taking action, but people should always remain in control of those actions.

**MCP Sentinel — Powerful AI. Human Control. Built on Trust.**

---

### 👥 Team
**Hackathon:** wHACKiest 2026  
**Institution:** Ramaiah Institute of Technology  
**Track:** 1 – Make MCP Matter

