# ShipSafe 🛡️

**Only safe code ships.**

> 🚧 **In development.** Not ready for use yet.

ShipSafe is an AI-powered security agent that tells you which vulnerabilities in your dependencies **actually affect your code**, and blocks unsafe releases before they reach Azure.

## Why

Tools like Dependabot flag every vulnerable library version, but most alerts don't matter because the vulnerable code is never used. ShipSafe checks whether your code actually calls the affected part, so you only fix what's real.

## How it works

1. **Scan:** read the project's dependencies and check them against [OSV.dev](https://osv.dev).
2. **Triage:** AI reads each advisory to find the affected function, and code analysis checks whether the project calls it.
3. **Verdict:** `reachable`, `not_reachable` or `needs_review`, always with evidence.
4. **Act:** explain the risk, open a fix PR, and block deployment until it's fixed.

## Tech stack

Python · uv · FastAPI · Microsoft Foundry · Azure SQL · GitHub Actions · Azure Container Apps · Copilot Studio