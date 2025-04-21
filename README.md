# ElasticNotebook: A Lightweight Checkpoint & Restore UI for Jupyter

This is a minimal, human-centered reimplementation of the ElasticNotebook system introduced in:

Zhaoheng Li, Supawit Chockchowwat, Hanxi Fang, Ribhav Sahu, Sumay Thakurdesai, Kantanat Pridaphatrakun, and Yongjoo Park. 2024. Demonstration of ElasticNotebook: Migrating Live Computational Notebook States. In Companion of the 2024 International Conference on Management of Data (SIGMOD '24). Association for Computing Machinery, New York, NY, USA, 540–543. https://doi.org/10.1145/3626246.3654752

## What This Project Does

This notebook-based tool allows users to:
- Manually or automatically save variable checkpoints
- Restore notebook state at any time
- See the exact code that generated each checkpoint
- View variables and their types in a friendly UI

It builds on the original ElasticNotebook **concept**, but reimplements the logic using:
- `ipywidgets` for interactive UI
- `dill` for checkpoint serialization
- A simplified post-cell hook to simulate lineage tracking

---

## Features

| Feature        | Description |
|----------------|-------------|
| Manual Checkpoint | Save all public variables and code from the last cell |
| Auto Checkpoint   | Save state automatically after each cell execution |
| Restore State     | Reload a saved checkpoint |
| Snippet Viewer    | Show the exact code that created a checkpoint |
| Variable Preview  | Table view of stored variables (name, type, preview) |

---

## Installation

No custom dependencies are required beyond Jupyter:

```bash
pip install dill ipywidgets pandas
