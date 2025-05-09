# MilTech v5 — MVP Platform

MilTech is a next-generation military-focused SaaS platform designed to upskill service members across their entire lifecycle: 
before enlistment, during active duty, and after transition.

This platform empowers users with:
- Credentialed bootcamps
- Verifiable skill-tracking
- Benefits education
- Transition planning tools
- AI-powered resume generation
- Direct employer job matching

This is the official production MVP build (miltech-v5).

---

## 🔧 Tech Stack

- Framework: Next.js (App Router, TypeScript)
- Database: Supabase (PostgreSQL + Auth + RLS)
- UI Framework: Tailwind CSS + Shadcn UI
- AI Integration: OpenAI (via GPT-4)
- Hosting: Vercel (frontend), Supabase (backend)
- MCP: Supabase Model Context Protocol (for Cursor)
- Dev Tools: Cursor, GitHub, VSC

---

## 📁 Folder Structure

app/                    # Route segments for users and employers  
components/             # Reusable + scoped UI  
hooks/                  # React hooks per feature/domain  
lib/                    # Service wrappers (Supabase, GPT, etc.)  
layouts/                # Global layout templates  
types/                  # Centralized TS interfaces  
db/                     # schema.sql, policies.sql, seed.sql  
utils/                  # Helper functions  
styles/                 # Tailwind entry  
public/                 # Static assets  
.cursor/                # MCP integration  

---

## ⚙️ Getting Started

### 1. Clone the Repo

git clone https://github.com/Leonard-Val/miltechv5.git  
cd miltechv5

### 2. Install Dependencies

npm install

### 3. Setup Environment Variables

Create `.env.local` and add:

NEXT_PUBLIC_SUPABASE_URL=your-supabase-url  
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key  
SUPABASE_SERVICE_ROLE_KEY=your-service-role-key  
OPENAI_API_KEY=your-openai-api-key

### 4. Start Dev Server

npm run dev

---

## 🚀 Features (MVP Scope)

- ✅ User & employer auth (Google/email)
- ✅ Bootcamp registration w/ seat tracking
- ✅ Benefits walkthrough engine
- ✅ AI resume & tutor (GPT-4)
- ✅ Verifiable profile export
- ✅ Employer dashboards w/ bulk outreach
- ✅ Transition roadmap flow

---

## 🧠 Cursor AI Project Rules

- MCP Supabase context enabled  
- Uses strict vertical slice structure: API route → hook → component → page  
- Design is locked via shared UI components (`/ui/`, `/shared/`)  
- All GPT logic goes through `lib/gpt.ts`  
- All Supabase logic goes through `lib/supabaseClient.ts`  

---

## 🛡️ Architecture Principles

- Modular vertical slices  
- Clean folder separation  
- Scalable to GovCon B2B & DoD pipelines  
- Built for AI-first infrastructure  
- Designed for military training, onboarding, and job funneling

---

## 👥 Contact

Lead: Leonard Val  
Repo: https://github.com/Leonard-Val/miltechv5

---

## 📌 License

Proprietary – All rights reserved to MilTech Inc.
