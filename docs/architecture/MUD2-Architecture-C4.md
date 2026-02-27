# MUD2.BAS - C4 Architecture Diagram

This is a C4-style architecture diagram showing the system context, containers, and components.

## Level 1: System Context

```mermaid
graph TB
    Player[Player]
    MUD2[MUD2 Game System]
    FileSystem[File System]
    Audio[Audio System]

    Player -->|Plays| MUD2
    MUD2 -->|Saves/Loads| FileSystem
    MUD2 -->|Plays Music/SFX| Audio
```

## Level 2: Container Diagram

```mermaid
graph TB
    subgraph MUD2["MUD2.BAS Game System"]
        UI[UI Layer<br/>Menu, Display, Input]
        Game[Game Logic<br/>Character, Combat, World]
        Data[Data Layer<br/>Save/Load, State]
    end

    Player[Player] --> UI
    UI --> Game
    Game --> Data
    Data --> FileSystem[File System]
    Game --> Audio[Audio System]
```

## Level 3: Component Diagram

```mermaid
graph TB
    subgraph UI["UI Layer"]
        MainMenu[Main Menu]
        WorldHelp[Help System]
        Display[Display Stats/Inventory]
    end

    subgraph GameLogic["Game Logic Layer"]
        CharSys[Character System]
        CombatSys[Combat System]
        WorldSys[World Navigation]
        EquipSys[Equipment System]
        MagicSys[Magic System]
    end

    subgraph DataLayer["Data Layer"]
        SaveGame[Save Game]
        LoadGame[Load Game]
        GameState[Game State]
    end

    MainMenu --> CharSys
    MainMenu --> SaveGame
    MainMenu --> LoadGame
    CharSys --> EquipSys
    WorldSys --> CombatSys
    CombatSys --> MagicSys
    CombatSys --> CharSys
    Display --> CharSys
    Display --> EquipSys
    SaveGame --> GameState
    LoadGame --> GameState
```

## Architecture Patterns

### Layered Architecture
- **Presentation Layer**: UI, menus, display functions
- **Business Logic Layer**: Game mechanics, combat, character management
- **Data Layer**: Save/load, state management

### Key Design Patterns
- **State Machine**: Game flow controlled by line labels and GOTO
- **Modular Subroutines**: Functionality separated into SUBs and FUNCTIONs
- **Shared State**: Global variables (DIM SHARED) for game state

