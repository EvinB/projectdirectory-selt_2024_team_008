
## Shards of the Grid 

## Tech Stack 
- Ruby on Rails
- JavaScript
- HTML/CSS
- PostgreSQL
- Cucumber
- RSpec
- OpenAI DALLE API 

Shards of the Grid is a full-stack SaaS multiplayer web game where users compete to claim and control tiles on a 10×10 dynamic grid. Designed as a team capstone project, the platform combines real-time multiplayer gameplay with an in-game economy, live chat, task-based mechanics, and account customization.

This project was built over multiple agile sprints and developed using test-driven development, emphasizing both gameplay features and codebase reliability.

## Gameplay Overview
Players join or create a session, spawning into a shared grid map. From there, they:
- Move to unoccupied tiles to expand territory.
- Complete math, NPC, or mini-game tasks to retain or acquire tiles.
- Earn Shards (virtual currency) for gameplay participation.
- Use shards to buy items, open randomized mystery boxes, or purchase territory upgrades.
- Equip avatar items and track performance via a live leaderboard.

## Core Features
**Territory & Tile Mechanics**
- Each session starts with an empty 10×10 grid initialized per game.
- Player positions and tile ownership are tracked in real time via ActiveRecord and ActionCable.
- Each tile has randomized task types and background images.

**Tasks & Game Logic**
- Tasks are handled via controller-level logic with custom validation per type (math, npc, or tic_tac_toe).

**In-Game Economy & Shop**
- Players earn and spend Shards (virtual currency).
- Buy cosmetics and equipment through a virtual store.
- Open Mystery Boxes with randomized rewards.
- Inventory and item ownership is tracked per user, and items can be equipped for aesthetics.

**Character Customization & Avatars**
- Users can generate custom avatars using the OpenAI DALL·E API, adding personalization to their in-game presence.
- Equipped items (earned or purchased) are visually reflected on the character.
- Avatars are displayed on grid tiles and in task interactions, enhancing immersion.

**Multiplayer & Sessions**
- Each game session creates an isolated "server" and "chatroom" via a Server model.
- Users must join the server before entering the game, tracked via Membership records.
- Live chat is enabled via ActionCable (websockets).

**Authentication & Access Control**
- Handled via Devise with Google OAuth support.
- Authenticated users can join games, own items, and interact with task/chat/game logic.

## Testing & Coverage 
- RSpec used for unit and controller tests (models, services, routes).
- Cucumber used for high-level BDD feature tests.
- Test coverage exceeds 70%, including routes, payment logic, shard economy, and multiplayer sync behavior.

## Development Process 
- Agile sprints with weekly planning, retrospective, and role delegation.
- Feature-first development using BDD and TDD workflows.
- Version control with Git and GitHub, using PRs, issue tracking, and review pipelines.
- Daily team standups.



![Screenshot](https://github.com/EvinB/projectdirectory-selt_2024_team_008/blob/main/sg1.png)
![Screenshot](https://github.com/EvinB/projectdirectory-selt_2024_team_008/blob/main/sg2.png)
![Screenshot](https://github.com/EvinB/projectdirectory-selt_2024_team_008/blob/main/sg3.png)
![Screenshot](https://github.com/EvinB/projectdirectory-selt_2024_team_008/blob/main/sg4.png)

