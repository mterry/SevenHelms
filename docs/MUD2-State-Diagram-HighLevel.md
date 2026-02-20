# MUD2.BAS - High-Level State Diagram

This is a simplified state diagram showing major game states and their relationships.

```mermaid
stateDiagram-v2
    [*] --> MainMenu

    state MainMenu {
        [*] --> MenuDisplay
        MenuDisplay --> NewGame
        MenuDisplay --> LoadGame
        MenuDisplay --> Options
        MenuDisplay --> Credits
        MenuDisplay --> [*]
    }

    state CharacterCreation {
        [*] --> EnterName
        EnterName --> SelectGender
        SelectGender --> SelectClass
        SelectClass --> SelectFamiliar
        SelectFamiliar --> RollStats
        RollStats --> ConfirmCharacter
        ConfirmCharacter --> [*]
    }

    state GameWorld {
        [*] --> Encampment
        Encampment --> Shop
        Encampment --> LabyrinthLevel1
        LabyrinthLevel1 --> LabyrinthLevel2
        LabyrinthLevel2 --> LabyrinthLevel3
        LabyrinthLevel3 --> BossArea
        Shop --> Encampment
    }

    state Combat {
        [*] --> BattleStart
        BattleStart --> PlayerTurn
        PlayerTurn --> EnemyTurn
        EnemyTurn --> CheckVictory
        CheckVictory --> PlayerTurn : Continue
        CheckVictory --> Victory : Enemy Defeated
        CheckVictory --> Defeat : Player Defeated
        Victory --> [*]
        Defeat --> [*]
    }

    state BossBattle {
        [*] --> XanathusFight
        XanathusFight --> NecrotaliaFight
        NecrotaliaFight --> EndGame
        EndGame --> [*]
    }

    MainMenu --> CharacterCreation : New Game
    MainMenu --> GameWorld : Load Game
    CharacterCreation --> GameWorld
    GameWorld --> Combat : Enemy Encounter
    Combat --> GameWorld : Victory
    Combat --> MainMenu : Defeat
    GameWorld --> BossBattle : Enter Boss Area
    BossBattle --> MainMenu : Complete
    GameWorld --> MainMenu : Save & Quit
```

**High-Level Game Flow:**
1. Main Menu - Entry point
2. Character Creation - Set up player
3. Game World - Exploration and navigation
4. Combat - Battle encounters
5. Boss Battle - Final challenges
