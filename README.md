# 🚀 CargoFL Ops AI Internal Tool Builder

> Transform unstructured customer communications into actionable operational insights in seconds.

![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge\&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge\&logo=typescript)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge\&logo=postgresql)
![Prisma](https://img.shields.io/badge/Prisma-ORM-2D3748?style=for-the-badge\&logo=prisma)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-green?style=for-the-badge\&logo=openai)
![Slack](https://img.shields.io/badge/Slack-Integration-4A154B?style=for-the-badge\&logo=slack)
![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge\&logo=amazonaws)

---

## 📖 Overview

Operations teams often spend valuable time manually reading customer emails, extracting information, updating spreadsheets, and tracking incidents.

**CargoFL Ops AI Internal Tool Builder** automates this process by converting unstructured customer communications into structured operational records using AI.

### Demo Flow

```text
Customer Email
      ↓
Slack Message
      ↓
AI Extraction Engine
      ↓
Structured JSON
      ↓
PostgreSQL Database
      ↓
Real-Time Dashboard Update
```

A customer email can become an operational record visible on the dashboard within **4 seconds**.

---

## ✨ Key Features

### 🤖 AI-Powered Data Extraction

Extracts:

* Customer Name
* Customer Email
* Shipment ID
* Order ID
* Issue Type
* Priority Level
* Status
* Additional Metadata

from plain text emails automatically.

---

### 💬 Slack Integration

* Slack Event API
* Incoming Webhooks
* Slash Commands
* Real-time Message Processing

Paste a customer email into Slack and watch it appear in the dashboard instantly.

---

### 📊 Operations Dashboard

Track:

* Open Incidents
* Critical Issues
* Resolution Status
* Extraction Accuracy
* Processing Metrics

with a modern analytics dashboard.

---

### ⚙️ Prompt Configuration System

Non-technical users can:

* Edit AI prompts
* Add extraction fields
* Remove extraction fields
* Save prompt versions
* Rollback configurations

without writing code.

---

### 🔔 Real-Time Updates

Dashboard updates automatically whenever:

* New incidents are created
* Existing incidents are modified
* AI extraction completes

---

### 🔐 Enterprise Security

* Authentication
* Role-Based Access Control (RBAC)
* Audit Logs
* Input Validation
* Rate Limiting
* Secure API Routes

---

## 🏗️ System Architecture

```text
┌─────────────────────┐
│      Slack App      │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   Next.js Backend   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   OpenAI GPT-4o     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Validation Layer   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ PostgreSQL + Prisma │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Next.js Dashboard   │
└─────────────────────┘
```

---

## 🛠️ Tech Stack

### Frontend

* Next.js 15
* React 19
* TypeScript
* Tailwind CSS
* shadcn/ui
* Zustand
* TanStack Table

### Backend

* Next.js API Routes
* Server Actions

### Database

* PostgreSQL
* Prisma ORM

### AI

* OpenAI GPT-4o

### Authentication

* Clerk

### Realtime

* Pusher

### Cloud

* AWS Amplify
* AWS RDS
* AWS S3

### Monitoring

* Sentry
* CloudWatch

---

## 📂 Project Structure

```bash
CargoFL-Ops-AI/
│
├── app/
│   ├── dashboard/
│   ├── incidents/
│   ├── analytics/
│   ├── prompts/
│   ├── users/
│   ├── settings/
│   └── api/
│
├── components/
│   ├── dashboard/
│   ├── incidents/
│   ├── analytics/
│   ├── prompts/
│   └── shared/
│
├── prisma/
│   ├── schema.prisma
│   └── migrations/
│
├── lib/
│   ├── prisma.ts
│   ├── openai.ts
│   ├── slack.ts
│   └── pusher.ts
│
├── services/
│
├── hooks/
│
├── schemas/
│
├── types/
│
├── public/
│
└── tests/
```

---

## 🗄️ Database Models

### Core Models

* User
* Role
* Organization
* Incident
* Customer
* PromptTemplate
* PromptVersion
* ExtractionHistory
* SlackMessage
* AuditLog
* Notification

---

## 📊 Dashboard Modules

### Overview Dashboard

* Total Incidents
* Open Incidents
* Critical Incidents
* Resolved Incidents
* AI Accuracy
* Processing Time

### Incident Management

* Incident List
* Incident Details
* Status Updates
* Assignment Workflow

### Prompt Management

* Prompt Editor
* Version Control
* Rollback Support

### Analytics

* Incident Trends
* Issue Categories
* Resolution Metrics
* Team Performance

### Audit Logs

* User Activities
* Prompt Changes
* Incident Updates

---

## 🔄 Workflow

### Step 1

Customer email arrives:

```text
Hi Team,

Shipment #7845 has been delayed.

Customer: John Smith

Expected delivery was June 1st.

Regards
```

### Step 2

Message is posted to Slack.

### Step 3

AI extracts:

```json
{
  "customerName": "John Smith",
  "shipmentId": "7845",
  "issueType": "Shipment Delay",
  "priority": "High"
}
```

### Step 4

Data is validated and saved.

### Step 5

Dashboard updates automatically.

---

## 🚀 Getting Started

### Clone Repository

```bash
git clone https://github.com/yourusername/cargofl-ops-ai.git
```

```bash
cd cargofl-ops-ai
```

---

### Install Dependencies

```bash
npm install
```

---

### Configure Environment Variables

Create `.env`:

```env
DATABASE_URL=

OPENAI_API_KEY=

CLERK_SECRET_KEY=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=

SLACK_SIGNING_SECRET=

SLACK_BOT_TOKEN=

PUSHER_APP_ID=

PUSHER_KEY=

PUSHER_SECRET=

AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION=
```

---

### Database Migration

```bash
npx prisma migrate dev
```

---

### Generate Prisma Client

```bash
npx prisma generate
```

---

### Start Development Server

```bash
npm run dev
```

---

## 🧪 Testing

### Unit Tests

```bash
npm run test
```

### Integration Tests

```bash
npm run test:integration
```

### End-to-End Tests

```bash
npm run test:e2e
```

---

## ☁️ Deployment

### Frontend

AWS Amplify

### Database

AWS RDS PostgreSQL

### Storage

AWS S3

### Monitoring

CloudWatch + Sentry

---

## 📈 Future Enhancements

* Multi-Tenant Support
* OCR Document Processing
* Email Inbox Integration
* Automated Ticket Creation
* AI-Powered Incident Categorization
* Predictive Analytics
* Workflow Automation Engine

---

## 🎯 Resume Highlights

Built an AI-powered operations automation platform using Next.js, TypeScript, PostgreSQL, Prisma, Slack APIs, OpenAI GPT-4o, and AWS.

Implemented configurable prompt workflows enabling non-technical users to modify extraction logic without code deployments.

Designed a real-time incident processing pipeline that converts unstructured customer communications into structured operational data within seconds.

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Vaishnav B**

B.Tech CSE | Full-Stack Developer | AI & Cloud Enthusiast

If you found this project useful, give it a ⭐ on GitHub.
