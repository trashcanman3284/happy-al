# Happy Al

## Commands
- `npx http-server .` - Dev server for HTML5 game testing
- `git push origin main` - Deploy to GitHub Pages

## Stack
- HTML5 Canvas with vanilla JavaScript
- Single-file architecture using requestAnimationFrame
- Bounding box collision detection only

## Code style
- Use consistent naming: `gameState` not `game_state` 
- Power-up spawn timing: 8-20 second random intervals
- Column retraction: 2.5% reduction, 15-second duration

## Workflow
- IMPORTANT: Test collision boundaries after any sprite size changes
- IMPORTANT: Verify power-up spawn timing doesn't create impossible scenarios
- Keep all game logic in single JavaScript file per architecture decision

## Gotchas
- YOU MUST NOT: Use pixel-perfect collision - causes performance issues
- YOU MUST NOT: Make column retraction permanent - breaks difficulty curve
- YOU MUST NOT: Skip requestAnimationFrame timing validation on mobile

## Docs
- Current state: @docs/PROJECT_STATE.md
- Today's standup: @docs/DAILY_SNAPSHOT.md  
- Task history: @docs/TASK_LOG.md
- Architecture: @docs/ARCHITECTURE.md

## Autonomous Execution Rules
- NEVER start long-running processes (http servers, watch modes, dev servers, python -m http.server, npx serve, etc.) during autonomous execution. The Agent SDK cannot interact with or terminate persistent processes — they will block the entire pipeline indefinitely.
- To verify HTML/JS works, check file syntax and structure — do not attempt to serve and browse.

<!-- Last optimized: 2026-04-02 -->
