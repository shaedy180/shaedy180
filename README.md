# Hi, I'm shaedy

## About

- Working with TypeScript, Java, Python, C#, and HTML

## Tech

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white)

## Featured Projects

- [Atlas](https://github.com/shaedy180/atlas) - Recipe and item intelligence mod for Minecraft. Search, browse, and understand every recipe, crafting path, and acquisition source in the game. 
- [OBS Now-Playing Overlay](https://github.com/shaedy180/obs-overlay-nowplaying) - Python and HTML based overlay for OBS.

## Contact

- Website: shaedy.de
- Ko-fi: [ko-fi.com/shaedy](https://ko-fi.com/shaedy)

## Repository maintenance

This repository publishes the GitHub profile above. Changes use the single `working-branch` → `main` PR, passing content validation, and a merge commit followed by fast-forward synchronization. Read [AGENTS.md](AGENTS.md). There is no deployment workflow or application runtime.

## Efficient CI and verified releases

Open a draft or ready PR from `working-branch` to `main` to run the complete validation suite. A push to `working-branch` alone does not start CI; use **Run workflow** for checks before opening a PR. New PR updates cancel obsolete runs for that PR. Main and release runs are never cancelled by a newer PR update.

After every required PR job succeeds, **CI provenance** records the tested merge commit. On a `main` push, CI runs only a small verification gate: the latest matching PR run must be successful, its receipt must be current and unexpired, and its tested Git tree and both merge parents must exactly match the actual merge. Missing, failed, stale or mismatched evidence blocks release instead of silently skipping checks. Update the PR against current `main` and wait for all required checks before merging. If a receipt has expired, rerun the complete original PR workflow, then rerun the main gate.

Release-specific builds, tag checks, immutable commit labels, publishing and deployment safeguards remain in place. Main publication starts only after the verification gate succeeds; the application test suite is not repeated after merge. Manual and tag/release validation remain available. Keep both the existing required checks and **CI provenance** required in branch protection.
