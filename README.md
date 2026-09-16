# Team Shooter 3D - Mobile Multiplayer Game

## 🎮 Project Overview

**Team Shooter 3D** is a competitive 3D multiplayer team-based shooting game for iOS and Android platforms. Players form squads of up to 5 members and compete in intense tactical gameplay.

### Key Features
- **5v5 Team-based Gameplay** - Squad-focused tactical combat
- **Squad System** - Form teams, squad management, and coordination
- **3D Graphics** - High-quality 3D environments and character models
- **Cross-platform** - iOS and Android support
- **Real-time Multiplayer** - Powered by Mirror networking framework
- **Mobile Optimized** - Touch controls and mobile-friendly UI

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|-----------|
| **Engine** | Unity 2022 LTS |
| **Language** | C# |
| **Networking** | Mirror (Free & Open Source) |
| **Platform** | iOS / Android |
| **Physics** | Unity Physics |
| **Audio** | Unity Audio System |

---

## 📁 Project Structure

```
team-shooter-3d/
├── Assets/
│   ├── Scripts/
│   │   ├── Player/
│   │   │   ├── PlayerController.cs
│   │   │   ├── PlayerHealth.cs
│   │   │   └── PlayerMovement.cs
│   │   ├── Squad/
│   │   │   ├── SquadManager.cs
│   │   │   ├── SquadMember.cs
│   │   │   └── SquadUI.cs
│   │   ├── Network/
│   │   │   ├── NetworkGameManager.cs
│   │   │   ├── PlayerNetworkIdentity.cs
│   │   │   └── ServerManager.cs
│   │   ├── Weapons/
│   │   │   ├── Weapon.cs
│   │   │   ├── Gun.cs
│   │   │   ├── Projectile.cs
│   │   │   └── WeaponManager.cs
│   │   ├── GameManager/
│   │   │   ├── GameManager.cs
│   │   │   ├── MatchManager.cs
│   │   │   └── SceneManager.cs
│   │   ├── UI/
│   │   │   ├── HUD/
│   │   │   ├── MainMenu.cs
│   │   │   ├── SquadUI.cs
│   │   │   └── GameOverScreen.cs
│   │   └── Audio/
│   │       ├── AudioManager.cs
│   │       └── SoundEffects.cs
│   ├── Prefabs/
│   │   ├── Player/
│   │   ├── Weapons/
│   │   ├── Effects/
│   │   └── UI/
│   ├── Scenes/
│   │   ├── MainMenu.unity
│   │   ├── GameLobby.unity
│   │   ├── Map01.unity
│   │   ├── Map02.unity
│   │   └── Map03.unity
│   ├── Materials/
│   ├── Textures/
│   ├── Audio/
│   │   ├── SFX/
│   │   └── Music/
│   └── Resources/
├── Packages/
├── ProjectSettings/
├── Documentation/
│   ├── GameDesignDocument.md
│   ├── NetworkArchitecture.md
│   ├── SquadSystem.md
│   └── Controls.md
└── README.md
```

---

## 🎯 Core Game Systems

### 1. Squad System
- Players form squads before match starts
- Squad leader can manage squad members
- Squad communication (in-game chat/voice)
- Squad respawn mechanics
- Squad objectives and markers

### 2. Player Controller
- Character movement and animation
- Health and damage system
- Respawn system
- Equipment and loadout system

### 3. Weapon System
- Multiple weapon types (Rifles, SMGs, Sniper, Shotguns)
- Ammunition management
- Firing mechanics
- Weapon recoil and accuracy
- Weapon balancing

### 4. Network System (Mirror)
- Server-client architecture
- Player spawning and despawning
- Real-time position synchronization
- Damage and health synchronization
- Squad state management

### 5. Game Manager
- Match initialization
- Round management (Best of 3, etc.)
- Score tracking
- Win/Loss conditions
- Player statistics

### 6. UI System
- Main Menu
- Squad formation screen
- In-game HUD
  - Health bar
  - Ammo counter
  - Squad member status
  - Mini map
  - Kill feed
- Game over screen
- Settings menu

---

## 🚀 Getting Started

### Prerequisites
- Unity 2022 LTS or later
- Mirror networking framework
- Visual Studio or Rider
- Android SDK / Xcode (for mobile deployment)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/uvrnv2856-wq/team-shooter-3d.git
cd team-shooter-3d
```

2. Open project in Unity 2022+

3. Install Mirror from Asset Store or package manager

4. Open MainMenu scene to start development

### Development Setup

```bash
# Initialize project
unity -projectPath . -executeMethod InitializeProject.Setup

# Build for Android
unity -projectPath . -buildTarget Android -executeMethod BuildScript.BuildAndroid

# Build for iOS
unity -projectPath . -buildTarget iOS -executeMethod BuildScript.BuildiOS
```

---

## 📱 Mobile Controls

### Touch Controls
- **Left Joystick** - Movement
- **Right Joystick** - Camera rotation
- **Fire Button** - Shoot
- **Reload Button** - Reload weapon
- **Squad Menu** - Squad management
- **Mini Map** - Tactical view

### UI Elements
- **Health Bar** - Player health status
- **Ammo Counter** - Ammunition display
- **Squad Status** - Teammates health and position
- **Kill Feed** - Recent kills and deaths

---

## 🌐 Network Architecture

### Mirror Setup
- **NetworkManager** - Handles connections and scene management
- **NetworkIdentity** - Player and game object synchronization
- **SyncVars** - Synchronized variables across network
- **Commands & RPCs** - Client-to-server and server-to-client communication

### Server Requirements
- Minimum 2 concurrent player connections
- Match server for 10 players (5v5)
- Squad coordination server
- Statistics and matchmaking database

---

## 🎮 Gameplay Loop

1. **Main Menu** - Player starts game
2. **Squad Formation** - Player joins or creates squad
3. **Matchmaking** - System finds opponents
4. **Loading** - Players load into map
5. **In-Game** - 5v5 tactical combat
6. **Match End** - Score calculation and results
7. **Results Screen** - MVP, statistics, rewards
8. **Return to Menu** - Continue or exit

---

## 📊 Match Format

- **Team Size** - 5 vs 5 players
- **Match Duration** - Best of 3 rounds (15 min per round)
- **Win Condition** - Eliminate all enemy squad or complete objective
- **Respawn** - After round or squad respawn mechanics
- **Scoring** - Kills, assists, objectives

---

## 🔧 Development Roadmap

### Phase 1 - Core Systems (Weeks 1-4)
- [ ] Player controller and movement
- [ ] Weapon system and firing mechanics
- [ ] Basic networking with Mirror
- [ ] Squad system foundation

### Phase 2 - Gameplay (Weeks 5-8)
- [ ] Game manager and match system
- [ ] Squad UI and communication
- [ ] Health and damage system
- [ ] Respawn mechanics

### Phase 3 - Polish & Optimization (Weeks 9-12)
- [ ] UI/UX refinement
- [ ] Mobile optimization
- [ ] Graphics and effects
- [ ] Audio implementation

### Phase 4 - Testing & Deployment (Weeks 13+)
- [ ] Beta testing
- [ ] Bug fixes
- [ ] iOS build and deployment
- [ ] Android build and deployment

---

## 👥 Team Structure

| Role | Responsibility |
|------|-----------------|
| Game Programmer | Core gameplay systems |
| Network Programmer | Mirror integration and multiplayer |
| UI Programmer | Menu and HUD systems |
| Graphics Programmer | Rendering and effects |
| Audio Programmer | Sound and music |

---

## 📚 Documentation

- [Game Design Document](./Documentation/GameDesignDocument.md) - Detailed game mechanics
- [Network Architecture](./Documentation/NetworkArchitecture.md) - Networking design
- [Squad System](./Documentation/SquadSystem.md) - Squad mechanics and UI
- [Controls Guide](./Documentation/Controls.md) - Input and controls

---

## 🐛 Issues & Bugs

Report bugs and issues on the [GitHub Issues](https://github.com/uvrnv2856-wq/team-shooter-3d/issues) page.

---

## 📝 License

This project is licensed under the MIT License - see LICENSE file for details.

---

## 🤝 Contributing

Contributions are welcome! Please follow the [Contributing Guidelines](./CONTRIBUTING.md).

---

**Last Updated:** September 16, 2026

**Project Status:** 🟡 In Development (Pre-Alpha)
