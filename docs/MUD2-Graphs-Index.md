# MUD2.BAS - Complete Graph Documentation Index

## Overview

This directory contains comprehensive control flow analysis for MUD2.BAS using Mermaid diagrams. The analysis includes both **flowcharts** (showing control flow with line labels and GOTO statements) and **state diagrams** (showing the game as a state machine).

---

## 📚 Start Here

1. **[MUD2-Control-Flow-README.md](MUD2-Control-Flow-README.md)** - Main documentation and guide
2. **[MUD2-Analysis-Summary.md](MUD2-Analysis-Summary.md)** - Detailed analysis with statistics

---

## 🔄 State Diagrams (Recommended)

State diagrams show the game as a state machine with states and transitions.

### Complete State Machine
- **[MUD2-State-Diagram-Complete.md](MUD2-State-Diagram-Complete.md)**
  - All 362 line labels as states
  - All 742 GOTO statements as transitions
  - Organized by functional category
  - Best for understanding the complete state machine

### High-Level Overview
- **[MUD2-State-Diagram-HighLevel.md](MUD2-State-Diagram-HighLevel.md)**
  - Simplified view of major game states
  - Shows: Main Menu → Character Creation → Game World → Combat → Boss Battles
  - Best for understanding overall game flow
  - Includes composite states with internal structure

---

## 🏗️ Architecture Diagrams (NEW!)

Architecture diagrams show the system's modular structure, components, and data model.

### Component Architecture
- **[MUD2-Component-Architecture.md](MUD2-Component-Architecture.md)**
  - 69 SUBs and FUNCTIONs organized by subsystem
  - Shows modular structure and component relationships
  - 9 functional categories (Character, Combat, Equipment, Magic, etc.)

### C4 Architecture Model
- **[MUD2-Architecture-C4.md](MUD2-Architecture-C4.md)**
  - Level 1: System Context (Player, Game, File System, Audio)
  - Level 2: Container Diagram (UI, Game Logic, Data layers)
  - Level 3: Component Diagram (detailed subsystems)
  - Follows C4 model best practices

### Data Model
- **[MUD2-Data-Model.md](MUD2-Data-Model.md)**
  - Class diagram showing data structures
  - Character, Equipment, Familiar, Enemy, GameState, RuneSystem
  - Relationships and cardinality

---

## 📊 Flowcharts (Control Flow Graphs)

Flowcharts show control flow using line labels as vertices and GOTO statements as edges.

### Complete Flowchart
- **[MUD2-Complete-Graph.md](MUD2-Complete-Graph.md)**
  - All 362 nodes (line labels)
  - All 742 edges (GOTO connections)
  - Complete control flow graph

### By Functional Area

#### Game Systems
- **[MUD2-Character-Creation.md](MUD2-Character-Creation.md)** - 23 nodes, 25 edges
- **[MUD2-Battle-System.md](MUD2-Battle-System.md)** - 22 nodes, 17 edges
- **[MUD2-Equipment-Shop.md](MUD2-Equipment-Shop.md)** - 8 nodes, 8 edges
- **[MUD2-Menu-System.md](MUD2-Menu-System.md)** - 16 nodes, 12 edges

#### Navigation Areas
- **[MUD2-Navigation-Act1-Level1.md](MUD2-Navigation-Act1-Level1.md)** - 41 nodes, 103 edges
- **[MUD2-Navigation-Act1-Levels2-3.md](MUD2-Navigation-Act1-Levels2-3.md)** - 41 nodes, 94 edges
- **[MUD2-Navigation-Encampment.md](MUD2-Navigation-Encampment.md)** - 74 nodes, 166 edges

#### Boss Battles
- **[MUD2-Boss-Battles.md](MUD2-Boss-Battles.md)** - 131 nodes, 136 edges (includes magic system)

---

## 📄 Raw Data

- **[mud2_analysis.txt](mud2_analysis.txt)** - Complete text listing of all labels and GOTO connections

---

## 📈 Statistics Summary

| Metric | Value |
|--------|-------|
| Total Lines of Code | 15,193 |
| Line Labels | 362 |
| GOTO Statements | 2,209 |
| Unique Control Flow Edges | 742 |
| Functional Categories | 12 |

---

## 🎯 Use Cases

### For Game Understanding
- **Start with**: High-Level State Diagram
- **Then explore**: Specific area flowcharts
- **Deep dive**: Complete state diagram

### For Code Analysis
- **Start with**: Analysis Summary
- **Then review**: Complete flowchart
- **Reference**: Raw data file

### For Refactoring
- **Identify**: Dead code and unreachable states
- **Analyze**: Complexity metrics from edge counts
- **Plan**: Modularization based on functional areas

---

## 🔍 Graph Types Explained

### State Diagrams vs Flowcharts

**State Diagrams** (`stateDiagram-v2`)
- Show the game as a state machine
- States represent game conditions/locations
- Transitions show how states change
- Better for understanding game flow
- More intuitive for game design

**Flowcharts** (`flowchart TD`)
- Show control flow structure
- Nodes represent line labels
- Edges represent GOTO statements
- Better for code analysis
- More technical/programming-focused

---

## 🛠️ Viewing the Graphs

### GitHub
Graphs render automatically in GitHub's Markdown viewer.

### VS Code
Install the "Markdown Preview Mermaid Support" extension.

### Online
Copy Mermaid code to [mermaid.live](https://mermaid.live)

### Command Line
```bash
npm install -g @mermaid-js/mermaid-cli
mmdc -i MUD2-State-Diagram-Complete.md -o diagram.png
```

---

## 📝 File Naming Convention

- `MUD2-State-Diagram-*.md` - State machine diagrams
- `MUD2-*-Graph.md` or `MUD2-*.md` - Flowchart diagrams
- `MUD2-Analysis-*.md` - Analysis documents
- `MUD2-Control-Flow-README.md` - Main documentation

---

## 🔗 Quick Links by Interest

**I want to understand the game flow:**
→ [High-Level State Diagram](MUD2-State-Diagram-HighLevel.md)

**I want to see the system architecture:**
→ [Component Architecture](MUD2-Component-Architecture.md) or [C4 Architecture](MUD2-Architecture-C4.md)

**I want to understand the data model:**
→ [Data Model Diagram](MUD2-Data-Model.md)

**I want to see all states and transitions:**
→ [Complete State Diagram](MUD2-State-Diagram-Complete.md)

**I want to analyze the code structure:**
→ [Complete Flowchart](MUD2-Complete-Graph.md)

**I want statistics and patterns:**
→ [Analysis Summary](MUD2-Analysis-Summary.md)

**I want to explore a specific area:**
→ Choose from functional area flowcharts above

---

## 📅 Generation Info

- **Generated**: 2026-02-20
- **Source File**: `src/MUD2.BAS` (15,193 lines)
- **Analysis Tool**: Python 3 with regex pattern matching
- **Graph Format**: Mermaid (flowchart TD & stateDiagram-v2)

---

## 💡 Tips

1. **Start simple**: Begin with the high-level state diagram
2. **Zoom in**: Move to specific area flowcharts as needed
3. **Reference**: Use the complete diagrams for comprehensive views
4. **Compare**: Look at both state diagrams and flowcharts for different perspectives
5. **Search**: Use your editor's search to find specific labels or states

---

For questions or detailed documentation, see [MUD2-Control-Flow-README.md](MUD2-Control-Flow-README.md)