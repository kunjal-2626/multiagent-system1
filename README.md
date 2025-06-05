# 🧠 Multi-Format Autonomous AI System with Contextual Decisioning & Chained Actions

This project demonstrates a FastAPI-based AI system that processes input files (Email, JSON, PDF), classifies their format and business intent, routes them to specialized agents, and triggers intelligent chained follow-up actions like alerts, escalation, or summarization.

## 🚀 Features

- Detects input file format: Email, JSON, PDF
- Classifies intent: RFQ, Complaint, Invoice, Regulation, Fraud Risk
- Specialized agent routing (email tone, JSON anomaly, PDF parser)
- SQLite-based memory for storing metadata and results
- Triggers follow-up actions like alerts or summaries
- REST API interface for file upload and task lookup

## 🧱 Architecture

![Architecture](architecture_diagram.png)

## 🗂 Sample Inputs

See `/sample_inputs/`:
- `email_sample.txt` - Customer complaint
- `invoice_sample.json` - JSON invoice
- `complaint_sample.pdf` - PDF with regulatory complaint

## 📥 Upload API

```bash
curl -X POST http://127.0.0.1:8000/upload/ \
  -F "file=@sample_inputs/email_sample.txt"
  # 🧠 Multi-Format Autonomous AI System with Contextual Decisioning & Chained Actions

This project demonstrates a FastAPI-based AI system that processes input files (Email, JSON, PDF), classifies their format and business intent, routes them to specialized agents, and triggers intelligent chained follow-up actions like alerts, escalation, or summarization.

## 🚀 Features

- Detects input file format: Email, JSON, PDF
- Classifies intent: RFQ, Complaint, Invoice, Regulation, Fraud Risk
- Specialized agent routing (email tone, JSON anomaly, PDF parser)
- SQLite-based memory for storing metadata and results
- Triggers follow-up actions like alerts or summaries
- REST API interface for file upload and task lookup

## 🧱 Architecture

![Architecture](architecture_diagram.png)

## 🗂 Sample Inputs

See `/sample_inputs/`:
- `email_sample.txt` - Customer complaint
- `invoice_sample.json` - JSON invoice
- `complaint_sample.pdf` - PDF with regulatory complaint

## 📥 Upload API

```bash
curl -X POST http://127.0.0.1:8000/upload/ \
  -F "file=@sample_inputs/email_sample.txt"
🔍 Task Lookup API
curl http://127.0.0.1:8000/tasks/<task_id>
🧠 Agent Logic Summary
Agent
Responsibilities
Classifier
Detects file type and business intent
Email Agent
Extracts sender, subject, tone, issues
JSON Agent
Validates schema, checks anomalies
PDF Agent
Extracts text, detects invoice or fraud
Router
Triggers alerts, summaries, escalations
💾 Memory
Data is stored in memory_store.db using aiosqlite.
📽 Demo Video
