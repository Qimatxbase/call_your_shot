# Call Your Shot — CYS Solar

One hackathon project containing both the FastAPI backend and Next.js UI for CYS Solar: solar sharing, tenant/landlord workflows, ROI estimates, proposals and green credits.

Local workspace: `hackathon/call_your_shot/`. The `backend/` and `frontend/` components belong to this single repository. SunShare was the earlier portfolio label.

Canonical repository: [Qimatxbase/call_your_shot](https://github.com/Qimatxbase/call_your_shot).

**Technologies:** Next.js · React · TypeScript · FastAPI · Supabase

## What is included

- Solar assessment, bill extraction, generation estimates and Monte Carlo ROI.
- Tenant/landlord dashboards, proposals, pricing and contract workflows.
- A Next.js server layer that calls FastAPI and keeps service keys on the server.

## Setup

```bash
python3.11 -m venv .venv
source .venv/bin/activate
pip install -r backend/requirements.txt
```

## Run

```bash
cd backend
python3.11 -m uvicorn app.main:app --host 127.0.0.1 --port 8001

# In another terminal, from the repository root:
cd frontend
cp .env.local.example .env.local
npm ci
npm run dev -- --hostname 127.0.0.1 --port 3000
```

Frontend: http://127.0.0.1:3000. API documentation: http://127.0.0.1:8001/docs. Copy backend/.env.example to backend/.env when configuring integrations. Demo and fallback data are described in the component READMEs. This was a team project.

## Checks

```bash
cd backend && python -m pytest tests
# Frontend, from the repository root:
cd frontend && npm test
```

## Source and credits

This portfolio snapshot preserves work from the following repositories. Existing author credits, citations and license files are retained; team and upstream code are not presented as solely authored work.

- https://github.com/Call-your-shot/backend-call-your-shot
- https://github.com/Call-your-shot/ui-call-your-shot

[Portfolio index](https://github.com/Qimatxbase/engineering_portfolio)
