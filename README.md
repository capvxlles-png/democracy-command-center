# Democracy Brewing — Growth Command Center

Single-page dashboard for the growth and partnerships engagement.
Onboarding tracks, task lists, the 90-day plan and scope, backed by Supabase.

## What's here

- `index.html` — the whole application, one file
- `netlify.toml` — deploy settings and security headers

## Deploying

Push to `main`; Netlify redeploys automatically in seconds.
Every previous deploy is kept — roll back from Deploys → Publish deploy.

## Before the first launch

In Supabase → Authentication → Sign In / Providers → Email:
turn **Confirm email OFF**.

Sign-in uses internal addresses derived from each person's name, so nobody
has to type an email. With confirmation on, sign-up waits for a message
that never arrives.

## Access

One link for everyone. Each person picks their name, enters a one-time
invite code, and sets their own password. Row-level security in Postgres
keeps each person's answers, tasks and saved views private; the admin
account sees everything.

Onboarding answers are append-only — every save inserts a new row, so
earlier versions stay readable and nothing is ever overwritten.
