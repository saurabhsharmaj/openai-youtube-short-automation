# 🎥 Automated YouTube Shorts Creation & Publishing System

An end-to-end **agent-based automation system** that generates, creates, uploads, and audits a **daily YouTube Short** at a scheduled time using **n8n + AI agents**.

This project is designed for **content creators** who want a fully automated, auditable, and scalable content pipeline.

---

## 🚀 Problem Statement

As a content creator:
- I want to **publish one YouTube Short every day at 9:00 AM**
- Content should be **AI-generated**
- Video and voice should be **automatically created**
- Upload should happen **without manual intervention**
- Every run should be **logged for audit**
- I should receive a **success/failure email notification**

---

## 🧠 Solution Overview

This system uses:
- **Multiple AI agents** for content, metadata, voice, and video
- **n8n** as the central workflow orchestrator
- **YouTube Data API** for publishing
- **Excel / Google Sheets** for audit logging
- **Email notifications** for observability

---

## 🏗️ High-Level Architecture

### Content Creation Workflow

![Content Creation Workflow](./docs/content-creation-workflow.png)

**Key Concept:**  
n8n acts as the **orchestrator**, coordinating multiple specialized agents in a deterministic sequence.

---

## 🔄 Automated Execution Timeline

### Automated Video Creation & Upload Workflow

![Automated Workflow Timeline](./docs/automated-workflow-timeline.png)

This diagram shows the **linear execution flow** from scheduling to notification.

---

## 🧩 System Components

### 1. Scheduler (n8n Cron)
- Triggers workflow **daily at 9:00 AM**
- Acts as the entry point

---

### 2. Prompt Agent
**Responsibility**
- Generates:
  - Daily content idea
  - Short-form script (30–60 seconds)

**Output**
```json
{
  "topic": "AI productivity hack",
  "script": "Did you know this AI tool can save you 5 hours a week?"
}
