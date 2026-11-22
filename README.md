# Non-Linear Data Structures in C
### PAED-Project-3

Implementation of **graphs**, **trees** and **hash tables** in C, applied to three problems set in the *Super Structure Bros* videogame universe.

Project 3 of the *Advanced Programming Data Structures* (APDS) course, BSc in Artificial Intelligence & Data Science, La Salle – Universitat Ramon Llull.

**Authors:** Sara Gibert, Oriol Pros, Francesc Mateu and Jan Porcar (group APDS-P3-G10)

## What it does

| Module | Structure | Problem |
|---|---|---|
| **Kart** | Graph | Represents racing circuits and checkpoints; detects circuits and optimises vehicle routes. |
| **Brawl** | Tree | Stores fighters ordered by attack power, with insertion, deletion, visualisation and range queries. |
| **Wonder** | Table | Stores game elements by name for fast lookup, spatial queries by area and statistics by world. |

## Project structure

```
├── main.c                  # Entry point: puts the three modules together
├── graph.c / graph.h       # Graphs (Kart)
├── graphPQ.c / graphPQ.h   # Priority queue used by the graph algorithms
├── tree.c / tree.h         # Trees (Brawl)
├── table.c / table.h       # Tables (Wonder)
├── tableLL.c / tableLL.h   # Linked list used by the tables
├── graphData.txt           # Input data for graphs (= graphsXS.paed)
├── treeData.txt            # Input data for trees  (= treesXXS.paed)
└── tableData.txt           # Input data for tables (= tablesM.paed)
```

## Build and run

Requires **GCC**. All source files must be compiled together:

```bash
gcc main.c tree.c graph.c graphPQ.c table.c tableLL.c -o main
./main
```

## Using other input files

Each module reads its data file from a hardcoded path. To use a different dataset, change the `fopen` call in:

| File | Line | Default |
|---|---|---|
| `graph.c` | 17 | `fopen("graphData.txt", "r")` |
| `tree.c` | 150 | `fopen("treeData.txt", "r")` |
| `table.c` | 138 | `fopen("tableData.txt", "r")` |

## Output

The program follows the exact output format defined in the project statement.
