# MUD2.BAS Control Flow Analysis - Summary

## Overview

This document provides a comprehensive analysis of the control flow structure in MUD2.BAS, a text-based adventure game written in BASIC. The analysis extracts all line labels and GOTO statements to create detailed control flow graphs.

## Statistics

- **Total Lines of Code**: 15,193
- **Total Line Labels**: 362
- **Total GOTO Statements**: 2,209
- **Unique Control Flow Edges**: 742

## File Organization

Based on comments in the source code and label analysis, MUD2.BAS is organized into the following sections:

### 1. Character Creation (Labels 0-27)
- **Labels**: 23
- **GOTO Connections**: 25
- **Purpose**: Character creation system including name, gender, class selection, and familiar choice
- **Key Labels**: 0, 10, 21, 21.5, 22, 24, 25
- **Graph**: `MUD2-Character-Creation.md`

### 2. Act 1 - Encampment & Labyrinth Level 1 (Labels 200-399)
- **Labels**: 41
- **GOTO Connections**: 103
- **Purpose**: First dungeon level navigation, including the encampment and initial labyrinth areas
- **Key Areas**: Areas 1-16 (labels 209-395)
- **Graph**: `MUD2-Navigation-Act1-Level1.md`

### 3. Equipment & Shop System (Labels 400-499)
- **Labels**: 8
- **GOTO Connections**: 8
- **Purpose**: Equipment management and shop interactions
- **Key Labels**: 400, 410, 430, 431, 445, 450, 460, 470
- **Graph**: `MUD2-Equipment-Shop.md`

### 4. Act 1 - Labyrinth Levels 2-3 (Labels 500-699)
- **Labels**: 41
- **GOTO Connections**: 94
- **Purpose**: Deeper dungeon levels with more complex navigation
- **Key Areas**: Areas 17-31 (labels 500-645)
- **Graph**: `MUD2-Navigation-Act1-Levels2-3.md`

### 5. Act 1 - Encampment Areas (Labels 700-999)
- **Labels**: 74
- **GOTO Connections**: 166
- **Purpose**: Extended encampment exploration areas
- **Key Areas**: Areas 35-67 (labels 680-997)
- **Graph**: `MUD2-Navigation-Encampment.md`

### 6. Battle System (Labels 1-2500)
- **Labels**: 22
- **GOTO Connections**: 17
- **Purpose**: Combat mechanics and AI protocols
- **Components**:
  - Basic Battle System (labels 1-16, 2000-2500)
  - Advanced Battle System (labels 1000-1510)
- **Graph**: `MUD2-Battle-System.md`

### 7. Magic/Runes & Boss Battles (Labels 3000-4001)
- **Labels**: 131
- **GOTO Connections**: 136
- **Purpose**: Magic system, rune combinations, and boss battle mechanics
- **Key Systems**:
  - Rune magic (labels 3000-3100)
  - Xanathus boss battle (labels 3500-4001)
- **Graph**: `MUD2-Boss-Battles.md`

### 8. Main Menu & System (Labels 9000-11000)
- **Labels**: 16
- **GOTO Connections**: 12
- **Purpose**: Main menu, save/load system, and game management
- **Key Labels**: 9998-10000 (main menu), 99998-100002 (save/load)
- **Graph**: `MUD2-Menu-System.md`

### 9. Necrotalia Boss Battle (Labels 35000-40000, 1000000+)
- **Labels**: Included in Boss Battles graph
- **Purpose**: Final boss encounter with Necrotalia
- **Key Labels**: 35000-39900, 1000000, 1000005

## Control Flow Patterns

### Navigation Pattern
The game uses a consistent pattern for area navigation:
- Each area has a primary label (e.g., 210, 220, 230)
- Secondary labels handle specific interactions (e.g., 215, 225, 235)
- GOTO statements connect areas based on directional commands (north, south, east, west, etc.)

### Battle Pattern
Battle sequences follow a structured flow:
1. AI protocol selection (labels 11-16)
2. Combat action execution (labels 1, 20, 70, 100, 110)
3. Result processing (label 2500)
4. Return to game world

### Menu Pattern
Menu systems use a loop structure:
1. Display options (e.g., label 9998)
2. Get user input (e.g., label 9999)
3. Process selection with GOTO to appropriate handler
4. Return to menu or continue game

## Graph Files Generated

1. **MUD2-Complete-Graph.md** - Complete control flow with all 362 labels and 742 edges
2. **MUD2-Character-Creation.md** - Character creation flow (23 nodes, 25 edges)
3. **MUD2-Navigation-Act1-Level1.md** - First dungeon level (41 nodes, 103 edges)
4. **MUD2-Navigation-Act1-Levels2-3.md** - Deeper dungeon levels (41 nodes, 94 edges)
5. **MUD2-Navigation-Encampment.md** - Encampment areas (74 nodes, 166 edges)
6. **MUD2-Battle-System.md** - Combat mechanics (22 nodes, 17 edges)
7. **MUD2-Boss-Battles.md** - Boss battles and magic (131 nodes, 136 edges)
8. **MUD2-Equipment-Shop.md** - Equipment system (8 nodes, 8 edges)
9. **MUD2-Menu-System.md** - Menus and save/load (16 nodes, 12 edges)

## Notable Observations

1. **High Connectivity**: The navigation areas show high connectivity (166 edges in encampment alone), indicating a complex, interconnected world.

2. **Modular Design**: Despite using GOTO statements, the code shows modular organization with clear functional boundaries between systems.

3. **Label Naming**: Labels use numeric ranges to group related functionality, making the code structure more understandable.

4. **Decimal Labels**: Some labels use decimal notation (e.g., 21.5, 10000.15) to insert additional control points without renumbering.

5. **Battle Complexity**: The battle system has relatively few labels but handles complex AI and combat mechanics through subroutine calls.

## Viewing the Graphs

All generated Mermaid graphs can be viewed in:
- GitHub (native Mermaid support)
- VS Code with Mermaid extension
- Any Markdown viewer with Mermaid support
- Online at mermaid.live

## Technical Details

- **Analysis Tool**: Python 3 with regex pattern matching
- **Graph Format**: Mermaid flowchart syntax
- **Node Format**: `L{label}` (e.g., L210, L21_5 for decimal labels)
- **Edge Format**: Directed arrows showing GOTO connections

## Source File

- **File**: `src/MUD2.BAS`
- **Size**: 15,193 lines
- **Language**: BASIC (QB/FreeBASIC dialect)
- **Analysis Date**: 2026-02-20