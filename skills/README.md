# Shared Skill Sync

This directory is the shared ROAMS skill base.

## Source Of Truth

- the shared skills in this repository are the default operating model
- project repositories may copy or vendor these skills as a pinned snapshot
- project-local skills should only add repo-specific behavior or override repo-specific details

## Sync Contract

When a project consumes the shared skill base:

1. record the source repository and pinned tag or commit
2. keep local changes out of shared skill files when possible
3. place repo-specific behavior in project-local extension skills
4. review release-to-release diffs before syncing updated shared skills

## Versioning Guidance

- use tagged releases when available
- if a tag is not available, pin to a specific commit
- update the consuming repo's operating docs when a shared-skill sync changes workflow expectations

## Goal

Keep shared skill updates predictable without forcing every repository to fork the base operating model.
