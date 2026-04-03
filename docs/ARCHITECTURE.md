# Architecture — Happy Al

## Overview
Happy Al is a browser-based Flappy Bird clone built as a single HTML5 file with vanilla JavaScript, featuring enhanced gameplay mechanics including column retraction and invulnerability power-ups. The game uses a simple state machine architecture with requestAnimationFrame-based game loop for smooth 60fps gameplay.

## Tech Stack
- **HTML5 Canvas** - Core rendering engine for 2D game graphics and animations
- **Vanilla JavaScript** - Single-file implementation to maintain simplicity and avoid dependencies
- **requestAnimationFrame** - Browser-native game loop for smooth frame timing
- **GitHub Pages** - Static hosting for zero-cost deployment and easy version control

## Key Decisions

**Single JavaScript File Architecture** - All game logic consolidated into one file to maintain simplicity and eliminate module complexity for this scope.

**Simple Bounding Box Collision Detection** - Fast rectangular collision detection chosen over pixel-perfect detection to maintain 60fps performance without unnecessary complexity.

**Random Power-up Spawning with Constraints** - Power-ups spawn on random timers between 8-20 seconds rather than fixed intervals to balance predictability with surprise.

**Temporary Column Retraction** - Column retraction from power-ups reverts after 15 seconds to preserve difficulty curve rather than making game progressively easier.

**Session-only High Score Tracking** - Scores reset when browser closes, avoiding local storage complexity while maintaining core competitive element.

## Data Model

**Game State** - Single `gameState` variable managing screens (homepage, playing, gameOver) via switch statements

**Game Objects** - Simple JavaScript objects for bird (position, velocity), columns (height, gap, retraction level), and power-ups (type, position, spawn timers)

**Assets** - Static image references loaded at startup:
- `happyal.png` (bird sprite)
- `column.png` (obstacle sprites) 
- `snow.png` (column retraction power-up)
- `monkey.png` (invulnerability power-up)
- `background.png` (scrolling background)
- `homepage.png` (start screen)
- `startgamebutton.png` (animated start button)

## Integration Points
- **GitHub Pages** - Static file hosting with automatic deployment from repository
- **Browser Canvas API** - Direct rendering interface for all game graphics
- **Browser Animation Frame API** - Native timing control for game loop execution