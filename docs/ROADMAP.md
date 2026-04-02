# Roadmap — Happy Al

## Slice 1 — Core Game Foundation
**Scope:** Set up the basic HTML5 Canvas game structure with the Happy Al bird (happyal.png) responding to input, scrolling background (background.png), and game loop using requestAnimationFrame. Implement basic gravity and jump mechanics.
**Done when:** Player can control the bird with keyboard/mouse input, the background scrolls continuously, and the bird falls with gravity when not actively controlled.

## Slice 2 — Column System and Collision
**Scope:** Add moving columns (column.png) that spawn at regular intervals and move from right to left. Implement collision detection between the bird and columns, plus ground/ceiling boundaries.
**Done when:** Columns appear and move across the screen, the game ends when the bird hits a column or boundary, and the player can navigate through column gaps successfully.

## Slice 3 — Power-Up System Implementation
**Scope:** Implement both power-up types with their mechanics: column retraction power-up (snow.png) that reduces column height by 2.5% per collection, and invulnerability power-up (monkey.png) that disables collision for 10 seconds with progressive flashing visual feedback.
**Done when:** Both power-ups spawn using the hybrid timer/progress system, collection triggers their respective effects, and the invulnerability flashing intensifies as the 10-second duration expires.

## Slice 4 — Scoring and Game States
**Scope:** Add session-based high score tracking that persists only during the current browser session, plus a complete game state system including game over detection and restart functionality.
**Done when:** Score increases as player progresses, current session high score is displayed and updated, and players can restart after game over without refreshing the page.

## Slice 5 — Homepage and Polish
**Scope:** Create the game's entry point with homepage background (homepage.png), animated start game button (startgamebutton.png) with bouncing animation, and integrate all game states into a cohesive user experience.
**Done when:** Game opens to homepage with bouncing start button, clicking the button launches gameplay, and players can return to homepage after game over.

## Slice 6 — Deployment and Final Integration
**Scope:** Package the complete game as a single HTML file with embedded JavaScript and CSS, ensure all assets (happyal.png, column.png, snow.png, monkey.png, background.png, homepage.png, startgamebutton.png) are properly integrated, and deploy to GitHub Pages.
**Done when:** Game runs flawlessly in browser from GitHub Pages URL, all visual assets display correctly, and the complete gameplay experience matches the specified requirements.
