# Prince Apple: The Rescue of Princess Pine

## Game Design Spec — by Tim & Eva

---

## 1. Overview

**Title:** Prince Apple
**Genre:** 2D Side-Scrolling Platformer
**Platform:** Web browser (HTML5 Canvas + JavaScript)
**Players:** 1
**Target audience:** Fun for all ages, designed with a 5–7 year old co-creator in mind

---

## 2. Story

In the peaceful Cat Kingdom, Prince Apple and Princess Pine live happily among their feline subjects. But one dark day, the evil Chicken King — the fearsome **McNug** — swoops in with his army of Chicken Knights and kidnaps Princess Pine, dragging her back to his fortress deep in the Chicken Kingdom.

Now Prince Apple must set out on a dangerous journey across five lands, battling Chicken Knights, solving puzzles in mysterious caves, and gathering powerful items — all to rescue Princess Pine from McNug's clutches.

---

## 3. Characters

### Prince Apple (Player Character)
- A brave young cat prince with a small crown
- **Default ability:** Jump and land on enemies to defeat them
- Can collect power-ups to gain special abilities
- Has **3 hearts** (hit points) — loses one heart each time he's hit by an enemy

### Princess Pine
- A kind and clever cat princess, captured by McNug
- Appears at the end of the game when rescued
- Could appear in short cutscenes between levels, showing she's okay and cheering Apple on

### McNug — The Chicken King (Final Boss)
- An oversized, menacing chicken wearing a golden crown and a red cape
- Rules the Chicken Kingdom with an iron wing
- Faced in the final level as the boss fight
- **Recurring cameo:** McNug appears near the end of EVERY level, taunting Prince Apple then running away. Each level he gets progressively more armoured and angrier:
  - **Level 1:** Crown and cape only, laughing smugly
  - **Level 2:** Adds a small shield, looking annoyed
  - **Level 3:** Adds a helmet, looking angry
  - **Level 4:** Full armour, fuming with rage
  - **Level 5:** Fully armoured boss fight — no more running!

### Chicken Knights (Standard Enemies)
- Chickens in little suits of armour
- Walk back and forth on platforms
- Can be defeated by jumping on them or hitting them with a yarn ball
- **Variants by level:**
  - **Basic Chicken Knight** — walks back and forth (Levels 1–2)
  - **Shield Chicken** — must be hit from behind or with a power-up (Levels 3–4)
  - **Flying Chicken** — hops/flutters in the air, harder to dodge (Levels 4–5)

### Cave Monsters (Puzzle Level Enemies)
- Found inside puzzle caves
- Could include: bats, slimes, or spiders
- Often guard puzzle solutions or power-ups

---

## 4. Power-Ups

Power-ups appear in floating gift boxes (with a paw print on them). Prince Apple breaks them open by jumping into them from below.

| Power-Up | Icon | Effect | Duration |
|---|---|---|---|
| **Yarn Ball Attack** | Ball of yarn | Throw yarn balls at enemies to defeat them from a distance | 10 throws per pickup |
| **Catnip Speed Boost** | Green leaf / herb | Run super fast, jump further | 8 seconds |
| **Fish Shield** | Golden fish | Become invincible — enemies bounce off you | 6 seconds |

---

## 5. Levels

### Level 1: The Cat Village
- **Setting:** A sunny village with cottages, fences, and trees
- **Difficulty:** Easy — teaches the player how to move, jump, and defeat enemies
- **Enemies:** Basic Chicken Knights (2–3 total)
- **Power-up introduced:** Yarn Ball Attack
- **End:** Reach the village gate to enter the Chicken Kingdom

### Level 2: The Feather Fields
- **Setting:** Open grassy fields with haystacks, scarecrows, and wooden fences
- **Difficulty:** Easy–Medium — more enemies, first moving platforms
- **Enemies:** Basic Chicken Knights (4–5)
- **Power-up introduced:** Catnip Speed Boost
- **New mechanic:** Moving platforms over mud puddles
- **End:** Enter the dark cave entrance at the edge of the fields

### Level 3: The Puzzle Caves
- **Setting:** Dark underground caves lit by glowing crystals
- **Difficulty:** Medium — introduces puzzles alongside platforming
- **Enemies:** Cave Monsters (bats, slimes) + Shield Chickens
- **Power-up introduced:** Fish Shield
- **Puzzle mechanic:** Push stone blocks onto pressure plates to open doors
- **End:** Climb up out of the caves into McNug's territory

### Level 4: McNug's Fortress Walls
- **Setting:** The outside of a huge stone castle, climbing upward
- **Difficulty:** Medium–Hard — vertical platforming, more enemy types
- **Enemies:** Shield Chickens, Flying Chickens, cave monsters on ledges
- **All power-ups available**
- **New mechanic:** Climbing sections (jump upward between walls)
- **End:** Reach the top of the fortress wall and enter through the window

### Level 5: The Throne Room of McNug
- **Setting:** Inside the grand (and slightly silly) chicken castle — golden eggs everywhere, feather banners, a giant nest throne
- **Difficulty:** Hard — gauntlet of enemies followed by the boss fight
- **Enemies:** All types of Chicken Knights in the corridor section
- **Boss fight — McNug:**
  - McNug charges across the room — Prince Apple must jump over him
  - McNug throws eggs that crack into mini chickens
  - McNug has a ground-pound attack that stuns Apple if he's on the ground
  - **To defeat McNug:** Jump on his head 10 times or hit him with yarn balls (he gets faster and angrier at HP thresholds — phase 2 at 6 HP, phase 3 at 3 HP)
  - McNug's crown falls off and he runs away clucking
- **End:** Princess Pine is freed! Celebration cutscene

---

## 6. Game Mechanics

### Movement
- **Left / Right arrow keys** — Move
- **Spacebar** — Jump
- **Up arrow or Z key** — Throw yarn ball (when equipped)

### Health
- Prince Apple has **3 hearts**
- Losing all 3 hearts = Game Over, return to the title screen
- Hearts can be restored by collecting **milk bottles** scattered through levels (max 3)

### Scoring
- **+100 points** — Defeat a Chicken Knight
- **+200 points** — Defeat a Cave Monster
- **+500 points** — Complete a puzzle
- **+1000 points** — Complete a level
- **+5000 points** — Defeat McNug
- Score displayed in the top-right corner

### Lives & Checkpoints
- Each level has **1 mid-level checkpoint** (a flag with a cat paw on it)
- On death, restart from the last checkpoint reached
- Game Over returns to the title screen

---

## 7. Visual Style

- **Pixel art** — chunky, colourful, friendly pixels (think classic 16-bit era)
- Bright, warm colours for the Cat Kingdom; slightly darker/sillier tones for the Chicken Kingdom
- Characters are cute and expressive — big eyes, simple animations
- McNug should look imposing but also a bit ridiculous

---

## 8. Sound & Music

- Cheerful, bouncy chiptune music for each level
- Satisfying sound effects: jump, land-on-enemy "boing", power-up "ding", yarn ball "whoosh"
- McNug gets his own dramatic (but silly) boss music
- Victory fanfare when Princess Pine is rescued

---

## 9. Screens & Flow

```
Title Screen ("Prince Apple")
    → Press Start
    → Level 1: The Cat Village
    → Level 2: The Feather Fields
    → Level 3: The Puzzle Caves
    → Level 4: McNug's Fortress Walls
    → Level 5: The Throne Room of McNug
    → Victory Screen / Celebration
    → Back to Title Screen
```

Each level has a short intro card showing the level name and a one-line description before gameplay begins.

---

## 10. Technical Notes

- **Engine:** Plain HTML5 Canvas + vanilla JavaScript (no framework)
- **Resolution:** 800 × 480 pixels (scales to fit browser window)
- **Frame rate:** 60fps target
- **Asset format:** PNG sprite sheets for characters and tiles
- **Level data:** JSON files defining tile maps, enemy positions, and power-up locations
- **No server required** — runs entirely in the browser as static files

---

## 11. Future Ideas (if we want to add more later)

- More levels and worlds (an underwater level? a sky level?)
- A second playable character (maybe Princess Pine in a prequel?)
- Collectible cat toys hidden in each level
- A level editor so Eva can design her own levels
- Co-op mode where a second player controls a friend character
- McNug returns with a bigger army in a sequel!

---

*Designed by Eva & Tim, specced with help from Claude*
*March 2026*
