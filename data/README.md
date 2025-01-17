# README

This repository contains a dataset derived from the study:

**Wang, H., Feng, S., He, T., Tan, Z., Han, X., & Tsvetkov, Y. (2024). Can language models solve graph problems in natural language? Advances in Neural Information Processing Systems, 36.**

The paper explores the use of natural language as a graph encoding function, benchmarking various graph-related tasks. Using diverse prompting strategies, including zero-shot, few-shot, and chain-of-thought (CoT), the study evaluates the performance of language models on tasks such as:

- Connectivity
- Cycle detection
- Topological sorting
- Shortest path
- Maximum flow
- Bipartite graph matching
- Hamiltonian path problems

This benchmark serves as a resource for understanding the capability of language models to solve graph problems when expressed in natural language. Researchers can leverage the dataset for further exploration in this emerging field of AI and graph theory.

## Dataset Structure

The `data` folder contains the following structure:

- **Tasks (8 folders):**
  - `connectivity`, `cycle`, `flow`, `GNN`, `hamilton`, `matching`, `shortest_path`, `topology`
  - Each folder represents a specific task and contains the following files and directories:
    - `main.json`: Used for supervised fine-tuning and divided into:
    - `train.json`: Training data
    - `test.json`: Testing data
    - `graph/`: Directory containing raw graph data divided into:
      - `easy/`, `medium/`, and `hard/`: Representing different difficulty levels
      - `graph.txt`: Raw graph data format:
        - First line: Two numbers representing the number of nodes and edges
        - Following lines: Edge definitions and queries

## Data Dictionary

| Variable        | Description                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------|
| `tasks`         | Folders representing 8 graph-related tasks: `connectivity`, `cycle`, `flow`, `GNN`, etc.         |
| `main.json`     | JSON file containing supervised fine-tuning data. Divided into `train.json` and `test.json`.    |
| `train.json`    | Training data for the corresponding task.                                                       |
| `test.json`     | Testing data for the corresponding task.                                                        |
| `graph/`        | Directory containing raw graph data files.                                                      |
| `easy/`         | Subdirectory with raw graph data for tasks of low difficulty.                                   |
| `medium/`       | Subdirectory with raw graph data for tasks of medium difficulty.                                |
| `hard/`         | Subdirectory with raw graph data for tasks of high difficulty.                                  |
| `graph.txt`     | File containing raw graph data in text format.                                                  |
| `nodes`         | First number in the first line of `graph.txt`, representing the number of nodes in the graph.   |
| `edges`         | Second number in the first line of `graph.txt`, representing the number of edges in the graph.  |
| `edge list`     | Lines in `graph.txt` that define connections between nodes.                                      |
| `queries`       | Additional lines in `graph.txt` representing queries related to the graph task.                 |