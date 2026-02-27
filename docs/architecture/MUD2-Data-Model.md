# MUD2.BAS - Data Model Diagram

This diagram shows the main data structures and their relationships.

```mermaid
classDiagram
    class Character {
        +String Name
        +String Sex
        +String Class
        +Integer STR
        +Integer DEX
        +Integer VIT
        +Integer ENG
        +Integer HP
        +Integer HPS
        +Integer EXPR
        +Integer Lvl
        +Long Gold
    }

    class Equipment {
        +String LH
        +String RH
        +String Armour
        +String Helm
        +Integer DAMAGEADDED
        +Integer DamageLostArmour
        +Integer DamageLostHelm
    }

    class Familiar {
        +String Name
        +Integer HP
        +Integer HPS
        +Integer DAMAGE
        +Integer MP
        +Integer MPS
        +Boolean Owl
    }

    class Enemy {
        +String Name
        +Integer PTS
        +Boolean Ethereal
        +Boolean Undead
    }

    class GameState {
        +Integer SavePos
        +Boolean SavedGame
        +Boolean LoadedGame
        +Boolean GameOn
        +Integer Diff
    }

    class RuneSystem {
        +String RUNE1
        +String RUNE2
        +String RUNE3
        +Boolean ken
        +Boolean yoo
        +Boolean tog
        +Boolean wir
        +Boolean gnu
    }

    Character "1" --> "1" Equipment : has
    Character "1" --> "1" Familiar : has
    Character "1" --> "1" RuneSystem : uses
    Character "1" --> "*" Enemy : fights
    GameState "1" --> "1" Character : manages
```

## Data Structure Details

### Character
Core player attributes including stats, class, and progression.

### Equipment
Player's equipped items and their effects on combat.

### Familiar
Companion creature with its own stats and abilities.

### Enemy
Opponent data including special properties (ethereal, undead).

### GameState
Overall game state including save/load status and difficulty.

### RuneSystem
Magic rune collection and combinations for spells.

