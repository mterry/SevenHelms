# MUD2.BAS - Component Architecture Diagram

This diagram shows the modular architecture of MUD2.BAS, organized by functional subsystems.

## Architecture Overview

```mermaid
graph TB
    subgraph Core["Core Game Engine"]
        Main[Main Game Loop]
    end

    subgraph Cat0["Character System"]
        CHARCREATE["CHARCREATE"]
        CLASSBONUS["CLASSBONUS"]
        CallFamiliar["CallFamiliar"]
        EXPERIENCE1000["EXPERIENCE1000"]
        EXPERIENCE2000["EXPERIENCE2000"]
        EXPERIENCELVLUP["EXPERIENCELVLUP"]
        FamiliarCall["FamiliarCall"]
        JACOB1000["JACOB1000"]
        JACOB2000["JACOB2000"]
        displaystats["displaystats"]
        MoreCat0["... 1 more"]
    end

    subgraph Cat1["Combat System"]
        AI["AI"]
        AIProtocols["AIProtocols"]
        BATTLE["BATTLE"]
        BATTLE2["BATTLE2"]
        ENEMYHPSBONUS["ENEMYHPSBONUS"]
        MainMenu["MainMenu"]
        NecrotaliaAI["NecrotaliaAI"]
        NecrotaliaBattle["NecrotaliaBattle"]
        NecrotaliaFight["NecrotaliaFight"]
        XanathusAI["XanathusAI"]
        MoreCat1["... 5 more"]
    end

    subgraph Cat2["Equipment System"]
        EQlh["EQlh"]
        EQrh["EQrh"]
        EqArmour["EqArmour"]
        EqHead["EqHead"]
        PurchaseSamael["PurchaseSamael"]
        RemoveArmour["RemoveArmour"]
        RemoveHelm["RemoveHelm"]
        RemoveLH["RemoveLH"]
        RemoveRH["RemoveRH"]
        ReturnWeapon["ReturnWeapon"]
        MoreCat2["... 2 more"]
    end

    subgraph Cat3["Magic System"]
        CheckRunes["CheckRunes"]
        MAGIC["MAGIC"]
        OWLSPELL["OWLSPELL"]
        RANDOMRUNEDROP["RANDOMRUNEDROP"]
        Runes["Runes"]
        USEOWLSPELL["USEOWLSPELL"]
    end

    subgraph Cat4["Other"]
        A56GetHint["A56GetHint"]
        BardMusic["BardMusic"]
        EndGame["EndGame"]
        EndGameCutscene["EndGameCutscene"]
        ExamineSymbol["ExamineSymbol"]
        GameIntro["GameIntro"]
        GemPuzzle["GemPuzzle"]
        SoundTest["SoundTest"]
        Steal["Steal"]
        ToadSteal["ToadSteal"]
    end

    subgraph Cat5["Persistence System"]
        GetSaveLoadPos["GetSaveLoadPos"]
        LoadGame["LoadGame"]
        PreSave["PreSave"]
        Preload["Preload"]
        SaveGame["SaveGame"]
        SaveToSavegame["SaveToSavegame"]
    end

    subgraph Cat6["UI System"]
        Credits["Credits"]
        HELP["HELP"]
        Options["Options"]
    end

    subgraph Cat7["Utility"]
        ClearFlags["ClearFlags"]
        RANDOMSTRING["RANDOMSTRING"]
    end

    subgraph Cat8["World Navigation"]
        ACT1["ACT1"]
        ACTSELECT["ACTSELECT"]
        Act1Pt2["Act1Pt2"]
        WorldHelp["WorldHelp"]
    end

    %% System Relationships
    Main --> Cat0
    Main --> Cat1
    Main --> Cat6
    Cat0 --> Cat2
    Cat1 --> Cat3
    Cat1 --> Cat0
    Cat4 --> Cat1
    Cat6 --> Cat5
```

## Component Details

### Character System

**Total Components**: 11

**Subroutines (11)**:
- `CHARCREATE`
- `CLASSBONUS`
- `CallFamiliar`
- `EXPERIENCE1000`
- `EXPERIENCE2000`
- `EXPERIENCELVLUP`
- `FamiliarCall`
- `JACOB1000`
- `JACOB2000`
- `displaystats`
- `jacobstats`

### Combat System

**Total Components**: 15

**Subroutines (14)**:
- `AI`
- `AIProtocols`
- `BATTLE`
- `BATTLE2`
- `MainMenu`
- `NecrotaliaAI`
- `NecrotaliaBattle`
- `NecrotaliaFight`
- `XanathusAI`
- `XanathusBattle`
- `XanathusFlee`
- `XanathusTaunt`
- `XanathusWorldFlee`
- `combat`

**Functions (1)**:
- `ENEMYHPSBONUS`

### Equipment System

**Total Components**: 12

**Subroutines (12)**:
- `EQlh`
- `EQrh`
- `EqArmour`
- `EqHead`
- `PurchaseSamael`
- `RemoveArmour`
- `RemoveHelm`
- `RemoveLH`
- `RemoveRH`
- `ReturnWeapon`
- `displayequip`
- `displayinventory`

### Magic System

**Total Components**: 6

**Subroutines (6)**:
- `CheckRunes`
- `MAGIC`
- `OWLSPELL`
- `RANDOMRUNEDROP`
- `Runes`
- `USEOWLSPELL`

### Other

**Total Components**: 10

**Subroutines (10)**:
- `A56GetHint`
- `BardMusic`
- `EndGame`
- `EndGameCutscene`
- `ExamineSymbol`
- `GameIntro`
- `GemPuzzle`
- `SoundTest`
- `Steal`
- `ToadSteal`

### Persistence System

**Total Components**: 6

**Subroutines (6)**:
- `GetSaveLoadPos`
- `LoadGame`
- `PreSave`
- `Preload`
- `SaveGame`
- `SaveToSavegame`

### UI System

**Total Components**: 3

**Subroutines (3)**:
- `Credits`
- `HELP`
- `Options`

### Utility

**Total Components**: 2

**Subroutines (2)**:
- `ClearFlags`
- `RANDOMSTRING`

### World Navigation

**Total Components**: 4

**Subroutines (4)**:
- `ACT1`
- `ACTSELECT`
- `Act1Pt2`
- `WorldHelp`

