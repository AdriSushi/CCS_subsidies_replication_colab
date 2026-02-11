READ ME

Dear user,

This repository contains all the code and data necessary to reproduce the results of our study.

1. Folder structure

- Jupyter notebooks (ipynb)
	- 1_data_cleaning.ipynb
	- 2_milp.ipynb
	- 3_results_analysis.ipynb

- Folders
	- data/ which contains the raw data for the case study, including emissions and spatial data for France’s industry. Do not modify this folder. Running 1_data_cleaning.ipynb will generate additional processed files in a data_clean/ folder.
	- results/ stores the results of the Mixed Integer Linear Program (MILP) and a subfolder figures/ containing all generated figures


2. How to run the code

a. Download the zip folder CODE_V3
b. Unzip the folder and name it (e.g., "CODE_V3")
c. Open this folder in Jupyter Notebook
d. Install all required Python packages listed in requirements.txt.
e. The notebook 1_data_cleaning.ipynb, has a line to install all the packages.
f. Run the notebooks in numerical order, using the 'Run all cells' function to make sure that all the code is run on the right sequence

Notebook descriptions
- 1_data_cleaning.ipynb
	- produces cleaned data files
	- Generates Figure 2 (Map of France with all industrial sites)
	- Generates Figure 3 (Map of France after Delaunay triangulation)
- 2_milp.ipynb
	- solves the MILP using either CPLEX or Gurobi (automatically selects the first available solver)
	- Saves model outputs in the results/ folder.
- 3_results_analysis.ipynb
	- Produces Figure 4, first part (Map of France with the various clusters) 
	- Produces Figure 4, second part (Map of the S0 cluster in the South-East of France
	- Figure 6 (Graph plotting the results for the P allocation)
	- Figure 7 (Graph plotting the results for the regret analysis on the P allocation)
	- relevant tables used in the paper (see section "Tables" of this file)

3. Notes
- No manual modification of the code is necessary. Notebooks will run normally if packages and at least one solver are installed
- At least one solver (CPLEX or Gurobi) must be installed and licensed for the MILP to run
- Figures are automatically saved in results/figures for reference
- Kernel crashes may occur if the solver is not properly installed or if the computational environment does not meet memory requirements.
- Tables 1, 2, and 4, and Figure 5 are constructed manually from the model outputs and are therefore not produced by the replication code.


Authors remain at your disposal for any inquiry regarding the code.
