# ORIE 5135 Project

This repository contains the implementation and writeup for the ORIE 5135 exam scheduling project.

## Files

- `report.pdf`: final written report, including formulations, computational tables, and discussion.
- `ORIE5135_Project_final_clean_fixed.ipynb`: Jupyter Notebook implementation.
- `final_project_results.csv`: computational results used in the report.
- `dataset1/`: Dataset 1 JSON instances.
- `dataset2/`: Dataset 2 JSON instances.

## Implementation

The implementation uses Python with `gurobipy`.

The notebook implements:

- F1: natural assignment formulation.
- F2: clique-strengthened assignment formulation.
- F3: extended grouping formulation.

Dataset 1 is solved with F1, F2, and F3.

Dataset 2 is solved with F1 and F2 only, because the extended formulation requires enumerating all feasible exam groupings, which is computationally impractical for larger instances.

## How to run

1. Make sure `dataset1/` and `dataset2/` are in the same directory as the notebook.
2. Open `ORIE5135_Project_final_clean_fixed.ipynb`.
3. Run all cells.
4. The notebook generates `final_project_results.csv`.

## Notes

The code reads instances directly from JSON files.  
Dataset 1 uses a 120-second time limit per MIP solve.  
Dataset 2 uses a 600-second time limit per MIP solve, following the project PDF.
