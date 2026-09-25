---
title: Project Roadmap
description: Use for structured complex software development projects.
category: software-development
name: project-roadmapping
version: 1.0.0
author: Mizuki Sakamoto
license: MIT
metadata:
  hermes:
    tags: [project-management, software-development, planning]
    related_skills: []
---

## Project Roadmap

Use when: Following a structured approach to complex software development projects.

### When to Use
- When the user explicitly tells you to follow a roadmap.
- When you see an existing `ROADMAP.md` in the project root.
- When the project is likely complex enough to benefit from one.

### When Not To Use
- For small, one-off ideas.

### What To Do
Create `ROADMAP.md` in the project root if it doesn't exist. This file should
contain a comprehensive plan, detailed enough that you can resume development
easily from a fresh context.

Break the project down into phases, and those into even smaller steps. Complete
at most *one* phase of the project per turn; or less if complexity demands.
When you end a turn, update `ROADMAP.md` with your progress and summarize what
you accomplished in the chat.

### Best Practices
- Keep phases small and achievable
- Update the roadmap after each work session
- Be detailed enough to resume from fresh context
- Focus on incremental progress rather than big leaps

### Template for ROADMAP.md
```markdown
# Project Roadmap

## Phase 1: Foundation
- [ ] Task 1
- [ ] Task 2

## Phase 2: Core Features
- [ ] Task 1
- [ ] Task 2

## Phase 3: Polish
- [ ] Task 1
- [ ] Task 2
```