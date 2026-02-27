# MUD2.BAS — Documentation

This directory contains comprehensive control flow analysis, architecture diagrams, and game documentation for `MUD2.BAS`, a text-based adventure game written in BASIC.

---

## 📚 Quick Start

1. **Understand the game flow** → [High-Level State Diagram](states/MUD2-State-Diagram-HighLevel.md)
2. **Understand the system design** → [Component Architecture](architecture/MUD2-Component-Architecture.md)
3. **Understand the data model** → [Data Model](architecture/MUD2-Data-Model.md)
4. **Analyze the code structure** → [Analysis Summary](analysis/MUD2-Analysis-Summary.md)
5. **See all states and transitions** → [Complete State Diagram](states/MUD2-State-Diagram-Complete.md)
6. **Explore a specific area** → [Flowcharts](#-flowcharts--control-flow-graphs)

---

## 📁 Directory Structure

```
docs/
├── README.md                              ← you are here
├── analysis/
│   ├── MUD2-Analysis-Summary.md           — statistics, patterns, methodology
│   └── mud2_analysis.txt                  — raw label and GOTO data
├── architecture/
│   ├── MUD2-Architecture-C4.md            — C4 model (context, containers, components)
│   ├── MUD2-Component-Architecture.md     — 69 SUBs/FUNCTIONs by subsystem
│   └── MUD2-Data-Model.md                 — class diagram of data structures
├── states/
│   ├── MUD2-State-Diagram-HighLevel.md    — simplified major game states
│   └── MUD2-State-Diagram-Complete.md     — all 362 states, 742 transitions
└── graphs/
    ├── MUD2-Complete-Graph.md             — all 362 nodes, 742 edges
    ├── MUD2-Character-Creation.md         — 23 nodes, 25 edges
    ├── MUD2-Battle-System.md              — 22 nodes, 17 edges
    ├── MUD2-Boss-Battles.md               — 131 nodes, 136 edges
    ├── MUD2-Equipment-Shop.md             — 8 nodes, 8 edges
    ├── MUD2-Menu-System.md                — 16 nodes, 12 edges
    ├── MUD2-Navigation-Act1-Level1.md     — 41 nodes, 103 edges
    ├── MUD2-Navigation-Act1-Levels2-3.md  — 41 nodes, 94 edges
    └── MUD2-Navigation-Encampment.md      — 74 nodes, 166 edges
```

---

## 🏗️ Architecture Diagrams

Diagrams showing the system's modular structure, components, and data model.

| File | Description |
|------|-------------|
| [MUD2-Architecture-C4.md](architecture/MUD2-Architecture-C4.md) | C4 model: System Context → Containers → Components |
| [MUD2-Component-Architecture.md](architecture/MUD2-Component-Architecture.md) | 69 SUBs and FUNCTIONs organized into 9 functional categories |
| [MUD2-Data-Model.md](architecture/MUD2-Data-Model.md) | Class diagram: Character, Equipment, Familiar, Enemy, GameState, RuneSystem |

---

## 🔄 State Diagrams

State diagrams show the game as a state machine with states and transitions.

| File | Description |
|------|-------------|
| [MUD2-State-Diagram-HighLevel.md](states/MUD2-State-Diagram-HighLevel.md) | Simplified view: Main Menu → Character Creation → Game World → Combat → Boss Battles |
| [MUD2-State-Diagram-Complete.md](states/MUD2-State-Diagram-Complete.md) | All 362 line labels as states, all 742 GOTO statements as transitions |

---

## 📊 Flowcharts — Control Flow Graphs

Flowcharts show control flow using line labels as nodes and GOTO statements as edges.

### Complete Graph
| File | Description |
|------|-------------|
| [MUD2-Complete-Graph.md](graphs/MUD2-Complete-Graph.md) | All 362 nodes and 742 edges — complete control flow graph |

### By Functional Area

#### Game Systems
| File | Nodes | Edges | Description |
|------|-------|-------|-------------|
| [MUD2-Character-Creation.md](graphs/MUD2-Character-Creation.md) | 23 | 25 | Name, gender, class, familiar selection |
| [MUD2-Battle-System.md](graphs/MUD2-Battle-System.md) | 22 | 17 | Combat mechanics and AI protocols |
| [MUD2-Equipment-Shop.md](graphs/MUD2-Equipment-Shop.md) | 8 | 8 | Equipment management and shop |
| [MUD2-Menu-System.md](graphs/MUD2-Menu-System.md) | 16 | 12 | Main menu, save/load system |
| [MUD2-Boss-Battles.md](graphs/MUD2-Boss-Battles.md) | 131 | 136 | Boss battles and magic/rune system |

#### Navigation Areas
| File | Nodes | Edges | Description |
|------|-------|-------|-------------|
| [MUD2-Navigation-Act1-Level1.md](graphs/MUD2-Navigation-Act1-Level1.md) | 41 | 103 | Encampment & Labyrinth Level 1 (labels 200–399) |
| [MUD2-Navigation-Act1-Levels2-3.md](graphs/MUD2-Navigation-Act1-Levels2-3.md) | 41 | 94 | Labyrinth Levels 2–3 (labels 500–699) |
| [MUD2-Navigation-Encampment.md](graphs/MUD2-Navigation-Encampment.md) | 74 | 166 | Extended encampment areas (labels 700–999) |

---

## 📄 Raw Data

| File | Description |
|------|-------------|
| [mud2_analysis.txt](analysis/mud2_analysis.txt) | Complete text listing of all labels and GOTO connections |
| [MUD2-Analysis-Summary.md](analysis/MUD2-Analysis-Summary.md) | Statistics, patterns, and methodology |

---

## 📈 Statistics

| Metric | Value |
|--------|-------|
| Total Lines of Code | 15,193 |
| Line Labels | 362 |
| GOTO Statements | 2,209 |
| Unique Control Flow Edges | 742 |
| Functional Categories | 12 |

---

## 🛠️ Viewing the Diagrams

**GitHub** — Mermaid diagrams render automatically in GitHub's Markdown viewer.

**VS Code** — Install the [Markdown Preview Mermaid Support](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid) extension.

**Online** — Copy any Mermaid code block to [mermaid.live](https://mermaid.live).

**Command Line** — Generate PNG/SVG images:
```bash
npm install -g @mermaid-js/mermaid-cli
mmdc -i graphs/MUD2-Complete-Graph.md -o MUD2-Complete-Graph.png
```

---

## 🔍 Graph Types Explained

**State Diagrams** (`stateDiagram-v2`) — Show the game as a state machine. States represent game conditions/locations; transitions show how states change. Better for understanding game flow.

**Flowcharts** (`flowchart TD`) — Show control flow structure. Nodes represent line labels; edges represent GOTO statements. Better for code analysis.

---

## 📝 Technical Notes

- **Decimal Labels**: Labels like `21.5` are converted to `L21_5` for Mermaid compatibility
- **Missing Edges**: Some GOTOs may target labels outside the analyzed sections
- **Subroutines**: SUB/FUNCTION calls are not included (only GOTO statements)
- **Conditional GOTOs**: All GOTO statements are included regardless of conditions
- **Analysis Tool**: Python 3 with regex pattern matching
- **Source File**: `src/MUD2.BAS` (15,193 lines, QB/FreeBASIC dialect)
- **Generated**: 2026-02-20