# Assignment 00: Local Notes App (Beginner Bridge)

## Period

**Days 1–7** (first week of onboarding).

This assignment sits in the **same week** as Assignment 01 ([Codex Repo Mapping](https://github.com/Zhihong0321/aqilah-assignment/blob/main/assignments/01-codex-repo-map.md)). Use this week to warm up: **Docker Desktop → Postgres in Docker → localhost app → Git → GitHub**. A typical order is: complete this small notes app first (so Git and AI workflow feel familiar), then do the two repo maps — unless your mentor sets a different order.

## Goal

Build confidence with **Cursor AI or Codex** on your own machine: a tiny project from scratch, saved in Git, published to GitHub. You write the app (with AI as a partner); this document only describes what to deliver.

## What You Will Build (you implement — not your mentor)

A **simple webpage** where you can:

- Type a note and save it.
- See your saved notes listed on the page.

Notes must be stored in **PostgreSQL** (not only in the browser). The page runs by opening it through a **local server** on your computer (`localhost`).

**Mandatory local runtime:** You must run Postgres **using Docker Desktop** (for example `docker compose` or `docker run` with the official Postgres image). Do not treat “Postgres installed directly on Windows/macOS” or a cloud database as the default path for this assignment unless your mentor explicitly waives this in writing.

## Constraints

- No production company repos and no real production secrets.
- **Docker Desktop** must be installed and used to run **PostgreSQL locally** for development and demos.
- Keep the stack **simple** (for example: plain HTML + a small Node server, or a minimal framework — choose what you can explain).
- **Before `git push`:** Your app must already work end-to-end on localhost against the Postgres container (add note → refresh → data still there). Pushing first and “fixing Docker later” does not meet this assignment.

## 💡 Beginner Guidance for Aqilah

Here is a quick cheat sheet for the core concepts:

- **Docker Desktop**: A tool that runs "containers". A container is like a tiny, separate computer inside your laptop. We use it to run our database safely.
- **Postgres (PostgreSQL)**: The database. It acts like a giant spreadsheet where your notes are saved so they don't disappear when you close your app.
- **Localhost**: Your own computer. Your app lives on `localhost` (not on the internet), meaning only you can see it right now.
- **Git**: A time machine for your code. It lets you save snapshots (called "commits") of your project as you build it.
- **GitHub**: A website where you upload your Git saves so others (like your mentor) can see and review your code.
- **AI (Cursor/Codex)**: Your coding assistant. Ask it questions, but make sure you understand the answers instead of just copying them!

## Tasks

1. **Plan briefly** (on paper or in `notes.md`): what pages/APIs you need, and how the browser talks to the database (you do not need a perfect diagram — just enough that you can explain it).

2. **Docker Desktop + Postgres (do this before you rely on GitHub):**

   *Useful References:*
   - 🎥 [Docker in 100 Seconds](https://www.youtube.com/watch?v=Gjnup-PuquQ)
   - 🎥 [PostgreSQL in 100 Seconds](https://youtu.be/n2Fluyr3lbc)

   - Install and start **Docker Desktop** on your machine.
   - Run **PostgreSQL in a container** (compose file, script, or documented `docker` commands — your choice, but it must be reproducible).
   - Confirm the database accepts connections from your app (host/port/user/password as you defined — never commit real passwords).

3. **Implement** on localhost **against that container**:

   - Web UI to add and list notes.
   - Server-side code that reads/writes Postgres.
   - A table for notes (for example: id, body/text, created_at — you may adjust).

4. **Use AI responsibly**:

   - Use **Cursor** or **Codex** to suggest code and explain files — **you** run commands, read the output, and fix errors until it works.
   - Write in your submission **what you asked** and **what you verified yourself** (copy-paste is not enough if you cannot explain it).

5. **Version control** (after local Docker + app work):

   *Useful Reference:*
   - 🎥 [Git in 100 Seconds](https://www.youtube.com/watch?v=hwP7WQkmECE)

   - Initialize Git in your project folder (if not already).
   - Commit sensible steps (for example: Docker/compose, server, DB layer, UI — not one giant mystery commit).
   - Include whatever files someone else needs to run Postgres the same way (`docker-compose.yml`, `compose.yaml`, or a clear `README` section — mentor may specify).

6. **GitHub** (only after your **end-to-end localhost demo** works: Docker Desktop → Postgres container → app saving and listing notes):

   *Useful Reference:*
   - 🎥 [Git and GitHub Tutorial for Beginners](https://www.youtube.com/watch?v=RGOj5yH7evk)

   - Create a **new repository** on GitHub (empty repo is fine).
   - Add the remote and **push** your work to `main` (or `master`, consistent with what GitHub shows — ask AI how if unsure).

## Deliverables (in *this* assignment repo or your mentor’s workspace)

Create a folder:

`submissions/00-local-notes-postgres/`

Include:

| File | Purpose |
|------|---------|
| `notes.md` | What you asked the AI, what confused you, what you decided. |
| `evidence.md` | Commands you ran, outputs that prove **Docker Desktop + Postgres container + app on localhost** work, then **your public GitHub repo URL** after push. |
| `reflection.md` | What went well, what was hard, what you would do next time. |

Also link or paste in `evidence.md`:

- The **HTTPS clone URL** of your GitHub repo (the notes app — not the assignment repo unless they are the same).

Optional but helpful:

- `architecture-one-paragraph.md`: In five sentences, how a saved note gets from the browser to Postgres and back.

## Required Evidence (minimum)

In `evidence.md`, show that you actually ran things locally **in order**:

- **Docker Desktop:** Proof it is running (for example screenshot of Docker Desktop showing the engine green / running, or `docker version` / `docker info` output that shows a working client talking to the daemon — redact anything sensitive).
- **Postgres container:** Proof the container is up (for example `docker ps` showing `postgres` or your compose service name, or compose logs snippet).
- **App + DB:** Proof the app serves on localhost and persists notes (screenshot or terminal lines: server started, URL opened, note saved, refresh still shows the note).
- **Postgres data:** Proof rows exist in the database from your test (for example one `docker exec … psql … SELECT` or GUI output — redact passwords).
- **Then Git:** `git status` (or equivalent) before a commit.
- **Then GitHub:** Link to your public repo + optional screenshot of the repo page **after** push.

If something is blocked (Docker won’t start, port conflict, etc.), write **what** blocked you and **what** you tried — do not invent output.

## Acceptance Criteria

- **Docker Desktop** is what you use to run **PostgreSQL locally** for this project (not a substitute unless mentor-approved).
- You can **demo** add + list notes on localhost with data **persisting** after you refresh the page (because it lives in Postgres in Docker).
- You can **name** the main files and what each does (browser, server, DB, Docker/compose).
- **Before** you push: the Docker + Postgres + app path works on your machine (see Required Evidence).
- Your **GitHub repo exists** and contains the app you built (not only empty commits), including enough for someone to understand how to run Postgres via Docker.
- Your submission files show **honest** evidence and reflection — safe workflow matters more than polish.

## Evaluation Notes (for reviewer)

Prioritize:

- Safety (no leaked secrets; `.env` in `.gitignore`; sample env in `.env.example` if used).
- Docker discipline (Postgres actually runs in Docker Desktop; evidence matches).
- Understanding (she explains the path from click → DB → screen, including how the app reaches the container).
- Verification (real command output, Docker + DB + app **before** push, then real repo link).

Codex judgment: she uses AI to speed learning, not to skip thinking.
