InsightForge Build Plan
Overview

Project: InsightForge, a SaaS for AI-driven business ideation, validation, and prototyping.
Goal: Deliver an MVP in 6-8 weeks (by Nov 10-17, 2025) with X sentiment analysis, basic prototyping, and Next.js UI.
Environment: Mac M2, SSD, Python 3.11 venv, open-source tools (Next.js, FastAPI, Supabase), cloud (Vercel).
Owner: Mark Bailey, with Grok as AI co-pilot.

Build Phases



Phase
Weeks
Goals
Key Artifacts
Status



Planning
1 (Sep 29-Oct 5)
Define scope, set up tools/repos
Project Charter, Trello board, GitHub repo
In Progress


MVP Build
2-4 (Oct 6-26)
Core features: X API, FastAPI backend, Next.js UI
Codebase, wireframes, sprint logs
Not Started


Testing
5-6 (Oct 27-Nov 9)
Refine UI, fix bugs, validate X integration
Bug tracker, test checklist
Not Started


Launch
7+ (Nov 10+)
Deploy to Vercel, monitor usage
Launch checklist, analytics dashboard
Not Started


Week 1 Tasks (Sep 29-Oct 5)



Task
Description
Tool
Due
Status



Set up Notion
Create workspace, import Charter
Notion
Sep 29
Done


Set up Trello
Create board, import JSON template
Trello
Sep 30
To-Do


Set up GitHub
Create repo, push initial structure
GitHub
Sep 30
To-Do


Install Next.js
Run npx create-next-app
Terminal/VS Code
Oct 1
To-Do


Install FastAPI
Run pip install fastapi uvicorn in venv
Terminal/VS Code
Oct 2
To-Do


Draft Specs
Outline MVP features (X search, prototyping)
Notion
Oct 3
To-Do


Notes

Tool Setup: Use Notion for docs, Trello for tasks, GitHub for code/artifacts. VS Code for editing, Terminal for commands.
venv Isolation: Always activate .venv (source .venv/bin/activate) to avoid conflicts with other projects (e.g., ConfiDoc, Sonique).
Grok Support: Prompt for code (e.g., X API integration), debugging, or artifact updates.
Risks:
Learning curve: Mitigated by Grok’s step-by-step commands.
Dependency conflicts: Use .venv and check pip list before installs.
Homebrew issues: Resolved (CLT/Xcode updated per Sep 29).



Next Steps

Sep 29: Import Trello JSON, paste Charter into Notion.
Sep 30: Run GitHub CLI setup (gh auth login), push repo.
Oct 1: Initialize Next.js (npx create-next-app src/frontend).
