# MUD2.BAS Control Flow Graph Documentation

This directory contains comprehensive control flow analysis and Mermaid graphs for MUD2.BAS, a text-based adventure game written in BASIC.

## Quick Start

1. **Start with the Summary**: Read `MUD2-Analysis-Summary.md` for an overview
2. **Explore by Area**: Choose a specific graph based on what you want to understand
3. **View Complete Graph**: See `MUD2-Complete-Graph.md` for the full picture

## Generated Files

### Analysis Documents
- **`MUD2-Analysis-Summary.md`** - Comprehensive analysis with statistics and patterns
- **`mud2_analysis.txt`** - Detailed text listing of all labels and GOTO connections

### Mermaid Flowcharts (Control Flow Graphs)

#### Complete Graph
- **`MUD2-Complete-Graph.md`** - All 362 line labels and 742 GOTO connections

#### Functional Area Graphs
- **`MUD2-Character-Creation.md`** - Character creation system (23 nodes, 25 edges)
- **`MUD2-Navigation-Act1-Level1.md`** - Encampment & Labyrinth Level 1 (41 nodes, 103 edges)
- **`MUD2-Navigation-Act1-Levels2-3.md`** - Labyrinth Levels 2-3 (41 nodes, 94 edges)
- **`MUD2-Navigation-Encampment.md`** - Encampment exploration areas (74 nodes, 166 edges)
- **`MUD2-Battle-System.md`** - Combat mechanics and AI (22 nodes, 17 edges)
- **`MUD2-Boss-Battles.md`** - Boss battles and magic system (131 nodes, 136 edges)
- **`MUD2-Equipment-Shop.md`** - Equipment and shop system (8 nodes, 8 edges)
- **`MUD2-Menu-System.md`** - Main menu and save/load (16 nodes, 12 edges)

### Mermaid State Diagrams

#### Complete State Diagram
- **`MUD2-State-Diagram-Complete.md`** - All 362 states with 742 transitions (complete state machine)

#### High-Level State Diagram
- **`MUD2-State-Diagram-HighLevel.md`** - Simplified view showing major game states and flow

## Understanding the Graphs

### Node Format
Each node represents a line label in the BASIC code:
```
L210["210: You are now standing in an intersec"]
```
- `L210` - Node ID (sanitized label)
- `210` - Original line label
- Description - First 40 characters of code at that label

### Edge Format
Arrows represent GOTO statements:
```
L210 --> L220
```
This means there's a `GOTO 220` statement in the code section labeled `210`.

### Viewing the Graphs

**GitHub**: Graphs render automatically in GitHub's Markdown viewer

**VS Code**: Install the "Markdown Preview Mermaid Support" extension

**Online**: Copy the Mermaid code to [mermaid.live](https://mermaid.live)

**Command Line**: Use `mmdc` (mermaid-cli) to generate images:
```bash
npm install -g @mermaid-js/mermaid-cli
mmdc -i MUD2-Complete-Graph.md -o MUD2-Complete-Graph.png
```

## Key Statistics

- **Total Lines**: 15,193
- **Line Labels**: 362
- **GOTO Statements**: 2,209
- **Unique Edges**: 742

## Code Structure

The game is organized into functional sections by label ranges:

| Range | Purpose | Labels | Edges |
|-------|---------|--------|-------|
| 0-27 | Character Creation | 23 | 25 |
| 200-399 | Act 1 Level 1 | 41 | 103 |
| 400-499 | Equipment & Shop | 8 | 8 |
| 500-699 | Act 1 Levels 2-3 | 41 | 94 |
| 700-999 | Encampment Areas | 74 | 166 |
| 1000-1999 | Battle System (Adv) | 10 | - |
| 2000-2999 | Battle System (Basic) | 4 | - |
| 3000-4001 | Magic & Boss Battles | 131 | 136 |
| 9000-11000 | Menu & System | 16 | 12 |
| 35000-40000 | Necrotalia Boss | 14 | - |
| 99000-103000 | Save/Load | 8 | - |

## Analysis Methodology

1. **Label Extraction**: Regex pattern `^\s*(\d+(?:\.\d+)?)\s+(.*)$` identifies line labels
2. **GOTO Detection**: Pattern `\bGOTO\s+(\d+(?:\.\d+)?)\b` finds all GOTO statements
3. **Context Mapping**: Each GOTO is mapped to its nearest preceding label
4. **Graph Generation**: Mermaid flowchart syntax with nodes and directed edges
5. **Categorization**: Labels grouped by numeric range into functional areas

## Use Cases

### Game Development
- Understand game flow and structure
- Identify unreachable code or dead ends
- Plan refactoring or modernization

### Code Analysis
- Study control flow patterns in legacy BASIC
- Analyze complexity and coupling
- Document game mechanics

### Learning
- Understand text adventure game architecture
- Study GOTO-based control flow
- Learn graph visualization techniques

## Technical Notes

- **Decimal Labels**: Labels like `21.5` are converted to `L21_5` for Mermaid compatibility
- **Missing Edges**: Some GOTOs may target labels outside the analyzed sections
- **Subroutines**: SUB/FUNCTION calls are not included (only GOTO statements)
- **Conditional GOTOs**: All GOTO statements are included regardless of conditions

## Source Code

- **File**: `src/MUD2.BAS`
- **Language**: BASIC (QB/FreeBASIC)
- **Size**: 15,193 lines
- **Project**: SevenHelms

## Generation Date

Generated: 2026-02-20

## Tools Used

- Python 3 with regex
- Mermaid.js for graph visualization
- Custom analysis scripts

---

For questions or issues, refer to the main project README or examine the source code directly.