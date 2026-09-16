# Game Design Document (GDD)
## Team Shooter 3D - 5v5 Mobile Multiplayer Shooter

**Document Version:** 1.0  
**Last Updated:** September 16, 2026  
**Status:** Pre-Alpha

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Game Concept](#game-concept)
3. [Core Mechanics](#core-mechanics)
4. [Squad System](#squad-system)
5. [Match Format](#match-format)
6. [Weapons & Equipment](#weapons--equipment)
7. [Maps & Environments](#maps--environments)
8. [Progression & Rewards](#progression--rewards)
9. [User Interface](#user-interface)
10. [Audio Design](#audio-design)
11. [Art Direction](#art-direction)

---

## Overview

**Game Title:** Team Shooter 3D  
**Platform:** iOS / Android  
**Target Audience:** Mobile gamers aged 13+  
**Genre:** Tactical Team-Based Shooter  
**Game Mode:** 5v5 Competitive Multiplayer  
**Perspective:** First-Person Shooter (FPS)

### Vision Statement
A fast-paced, tactical 3D team shooter that brings console-quality competitive gaming to mobile devices, emphasizing teamwork, strategy, and individual skill.

---

## Game Concept

### Core Premise
Two squads of 5 elite operators face off in intense tactical combat. Victory requires teamwork, communication, and strategic positioning. Each squad must coordinate their abilities and weapons to outmaneuver and eliminate their opponents.

### Key Selling Points
- **Squad-Focused Gameplay** - Requires team coordination and communication
- **Tactical Depth** - Multiple approaches to objectives and map control
- **Fast-Paced Action** - Quick matches (15 minutes per round)
- **Mobile-Optimized** - Touchscreen controls designed for mobile play
- **Cross-Platform** - Play with friends on iOS or Android
- **Balanced Multiplayer** - Skill-based matchmaking and weapon balancing

---

## Core Mechanics

### 1. Player Movement

**Sprint**
- Hold sprint button to run faster
- Limited sprint duration (5-7 seconds)
- Sprint cooldown (3 seconds)
- Speed: 1.5x normal speed

**Crouch**
- Reduces player hitbox by 30%
- Decreases movement speed to 0.5x
- Improved accuracy while crouching
- Silent footsteps when crouching

**Climb/Vault**
- Climb obstacles up to 2 meters high
- Vault over low walls
- Climbing animation takes 1-2 seconds

**Sliding**
- Slide while sprinting
- Dodge incoming fire
- Brief invulnerability during slide (0.5 seconds)
- Can fire while sliding

### 2. Combat System

**Shooting Mechanics**
- Point-and-shoot with crosshair
- Weapon accuracy varies by weapon type
- Recoil compensation based on weapon
- Headshots deal 2x damage
- Bodyshots deal 1x damage
- Leg shots deal 0.75x damage

**Damage Falloff**
- Full damage within effective range
- Damage reduction beyond effective range
- Different falloff for each weapon type

**Shield System**
- Optional shield item (150 HP)
- Shield depletes separately from health
- Takes 5 seconds to regenerate after 3 second delay

### 3. Health & Respawn

**Player Health**
- Base health: 100 HP
- Maximum health with armor: 150 HP
- Health does not regenerate
- Teammates can provide healing

**Respawn Mechanics**
- Respawn after 10 seconds if squad has alive member
- Wave respawn (all dead players spawn together) after 15 seconds
- No respawn after squad elimination (wait for round end)
- Spawn locations marked on minimap

### 4. Loadout & Equipment

**Primary Weapons**
- Assault Rifles
- SMGs
- Sniper Rifles
- Shotguns

**Secondary Weapons**
- Pistols
- Machine Pistols

**Equipment**
- Grenades (Frag, Flashbang, Smoke)
- Tactical Equipment (Deployable Shield, C4)
- Utility Items (Ammo Pack, Medical Kit)

---

## Squad System

### Squad Structure
- **Squad Size:** 5 players
- **Squad Leader:** Player with most leadership points
- **Squad Roles:**
  - Attacker (Rush role)
  - Support (Healing/Equipment role)
  - Defender (Shield/Tank role)
  - Scout (Mobility/Intel role)
  - Specialist (Unique abilities)

### Squad Formation Screen
Before match starts, players can:
- Select their role
- Choose loadout
- Assign squad leader
- Set squad tactics (Aggressive, Defensive, Balanced)

### Squad Communication
- **In-Game Chat** - Text communication
- **Voice Chat** - Real-time squad voice
- **Quick Ping System:**
  - Enemy here
  - Need backup
  - Clear
  - Watch left/right/up/down
  - Affirmative/Negative

### Squad Status Display
- Teammate health bars
- Teammate ammunition count
- Teammate ability cooldowns
- Teammate location on minimap
- Downed teammate callout

### Squad Respawn
- When squad has living members: respawn at alive teammate location
- When entire squad is down: wait for round end or squad wipe

---

## Match Format

### Round Structure

**Pre-Match (2 minutes)**
- Squad formation
- Loadout selection
- Map overview
- Countdown to match start

**In-Match (15 minutes per round)**
- Real-time 5v5 combat
- Objectives based on game mode
- Continuous score tracking
- Kill feed on screen

**Post-Match (2 minutes)**
- Results screen
- MVP selection
- Statistics display
- Squad performance analysis

### Win Conditions

**Elimination Victory**
- Entire enemy squad eliminated
- Winning squad gets 100 points

**Objective Victory (Mode Dependent)**
- Plant/Defuse the bomb
- Capture the objective
- Secure the area
- Depends on game mode

### Scoring System

| Action | Points |
|--------|--------|
| Enemy Kill | 50 |
| Assist | 25 |
| Headshot | +25 |
| Objective Completion | 100 |
| Objective Assist | 50 |
| Healing Teammate | 10 |
| Reviving Teammate | 50 |

### Match Types

**Team Deathmatch**
- Best of 3 rounds
- First team to 5,000 points wins
- Respawns enabled

**Bomb Defusal**
- Best of 5 rounds
- Attackers plant bomb
- Defenders prevent planting/detonation
- No respawns

**Capture Point**
- Best of 3 rounds
- Capture and hold central point
- First team to 3 captures wins

---

## Weapons & Equipment

### Assault Rifles

**AR-15**
- Damage: 25
- Fire Rate: 600 RPM
- Accuracy: Medium
- Effective Range: 20m
- Magazine: 30 rounds
- Rate: Balanced

**ACE-32**
- Damage: 30
- Fire Rate: 450 RPM
- Accuracy: High
- Effective Range: 30m
- Magazine: 20 rounds
- Rate: High damage per shot

### Submachine Guns

**MP7**
- Damage: 18
- Fire Rate: 950 RPM
- Accuracy: Low
- Effective Range: 10m
- Magazine: 40 rounds
- Rate: Close quarters specialist

**UMP45**
- Damage: 22
- Fire Rate: 600 RPM
- Accuracy: Medium
- Effective Range: 15m
- Magazine: 25 rounds
- Rate: Balanced SMG

### Sniper Rifles

**AWP Dragon**
- Damage: 100
- Fire Rate: 40 RPM
- Accuracy: Very High
- Effective Range: 50m+
- Magazine: 10 rounds
- Rate: One-shot kill weapon

**Scout Elite**
- Damage: 75
- Fire Rate: 90 RPM
- Accuracy: High
- Effective Range: 40m
- Magazine: 20 rounds
- Rate: Faster than AWP, less damage

### Shotguns

**SPAS-12**
- Damage: 60 (per pellet, 8 pellets)
- Fire Rate: 100 RPM
- Accuracy: Very Low
- Effective Range: 5m
- Magazine: 8 rounds
- Rate: Close range devastation

### Grenades

**Frag Grenade**
- Detonation time: 4 seconds
- Blast radius: 10m
- Damage: 50 (falloff)
- Bounces on ground

**Flashbang**
- Detonation time: 2 seconds
- Blind radius: 15m
- Duration: 3 seconds of blindness
- No damage

**Smoke Grenade**
- Detonation time: 1 second
- Smoke radius: 12m
- Duration: 8 seconds
- Blocks vision and thermal

---

## Maps & Environments

### Map Design Principles
- Multiple paths and flanking routes
- Verticality with buildings and elevated areas
- Objective locations balanced between teams
- Cover systems and sightline management
- Environmental hazards (breakable walls, collapsing structures)

### Map 1: "Downtown"
- **Setting:** Urban city center
- **Size:** Medium (100m x 100m)
- **Theme:** Modern city with shops, apartments, streets
- **Key Areas:**
  - Central plaza (objective area)
  - Apartment complex (high ground)
  - Underground parking
  - Market stalls (cover)
- **Spawn Points:** 2 per team

### Map 2: "Desert Base"
- **Setting:** Military compound in desert
- **Size:** Large (150m x 150m)
- **Theme:** Military installation with bunkers
- **Key Areas:**
  - Central control tower
  - Barracks buildings
  - Perimeter walls
  - Underground tunnels
- **Spawn Points:** 2 per team

### Map 3: "Industrial Complex"
- **Setting:** Abandoned factory
- **Size:** Medium-Large (120m x 120m)
- **Theme:** Warehouse and assembly lines
- **Key Areas:**
  - Production floor (open area)
  - Storage racks (cover)
  - Catwalks (high ground)
  - Control room (objective)
- **Spawn Points:** 2 per team

---

## Progression & Rewards

### Player Progression

**Experience System**
- Gain XP from every match
- XP based on performance and objectives
- Level cap: 100 (can reset for prestige)

**Battle Pass**
- 50 tiers per season (2 months)
- Free and Premium tracks
- Cosmetic rewards (skins, emotes, sprays)
- Weapon skins
- Operator skins

### Cosmetics

**Operator Skins**
- Character appearance customization
- Rarity tiers: Common, Rare, Epic, Legendary
- Purchasable with premium currency or battle pass

**Weapon Skins**
- Weapon appearance customization
- Custom kill effects for legendary skins
- Blueprint skins (unique firing animations)

**Emotes & Sprays**
- Post-match celebration emotes
- Spray tags for environment marking
- Victory animations

### Ranked System

**Ranking Tiers**
1. Bronze (0-1000 SR)
2. Silver (1000-2000 SR)
3. Gold (2000-3000 SR)
4. Platinum (3000-4000 SR)
5. Diamond (4000-5000 SR)
6. Master (5000+ SR)

**Skill Rating (SR)**
- Gained/lost based on match result
- Win: +50 SR
- Loss: -50 SR
- Bonus: Squad performance multiplier

### Achievements

**Combat Achievements**
- First Blood (first kill of match)
- Multi-Kill (3+ kills in 10 seconds)
- Headshot Spree (3 headshots in a row)
- Flawless Victory (win without dying)

**Squad Achievements**
- Teamwork (5 assists in 1 match)
- Squad Wipe (eliminate entire enemy squad)
- Clutch (1v5 and win)
- Rally (revive 3 teammates in 1 match)

---

## User Interface

### Main Menu
- Play button (Quick Match / Ranked)
- Squad Management
- Battle Pass
- Store
- Settings
- Profile

### Lobby Screen
- Squad members display
- Ready/Not Ready toggle
- Map preview
- Estimated match time
- Leave button

### In-Game HUD

**Center Screen**
- Crosshair (weapon-specific)
- Damage indicator (red arrow from hit direction)
- Objective indicator (bomb/capture point location)

**Top Left**
- Squad member status
- Health bars and ammo count

**Top Right**
- Timer (round time)
- Score display (Team A vs Team B)
- Objectives status

**Bottom Left**
- Minimap with radar
- Squad member positions
- Enemy last-known positions

**Bottom Center**
- Ammo counter
- Current weapon name
- Reload indicator

**Bottom Right**
- Ability cooldowns
- Equipment status

### Pause Menu
- Resume game
- Settings
- Quit to lobby
- Report player

---

## Audio Design

### Sound Effects Categories

**Weapon Sounds**
- Unique firing sound for each weapon
- Reload sounds
- Bullet impact sounds (concrete, metal, organic)
- Suppressed weapon sounds (quieter)

**Player Sounds**
- Footsteps (different for surface type)
- Reload grunts
- Pain sounds (damage taken)
- Death sounds
- Breathing sounds (heavy when damaged)

**UI Sounds**
- Button clicks
- Match start horn
- Round end notification
- Objective complete chime
- Kill notification sound

**Ambient Sounds**
- Background music (combat-themed)
- Environmental sounds (wind, traffic)
- Match countdown
- Victory/Defeat music

### Spatial Audio
- 3D positional audio for footsteps
- Direction indication through stereo
- Distance attenuation for distant sounds

---

## Art Direction

### Visual Style
- **Style:** Realistic military aesthetic
- **Color Palette:** Dark grays, earth tones, tactical colors
- **Tone:** Professional military/tactical ops

### Character Design
- 5-6 unique operator models
- Tactical gear and equipment
- Cosmetic customization support
- Diverse character roster

### Environment Design
- High-poly destruction elements
- Destructible walls and cover
- Dynamic lighting
- Environmental particle effects (dust, smoke)

### UI Design
- Minimalist tactical style
- Dark theme with bright accents
- Clear information hierarchy
- Mobile-optimized layouts

### Animation Priority
- Weapon reload animations
- Character movement animations
- Damage reactions
- Death animations
- Emote animations

---

## Technical Specifications

### Performance Targets
- **Frame Rate:** 60 FPS (high-end), 30 FPS (standard)
- **Resolution:** Scales from 720p to 1440p
- **Network:** Target 60Hz server tick rate
- **Latency:** <100ms for smooth gameplay

### Platform Requirements
- **iOS:** 14.0 or later
- **Android:** 10 or later
- **Minimum RAM:** 2GB (recommended 4GB+)
- **Storage:** 2-3GB installation size

---

**Document End**

*For questions or suggestions, contact the Game Design Lead.*
