## Installation

### Google colab notebooks
Install conda with a handy pip package by Jaime Rodríguez-Guerra
You have to run this first, and then wait to run any other cells.
This terminates and reboots the Python session.

```bash
!pip install -q condacolab
import condacolab
condacolab.install()
```

To make sure Conda was installed correctly, run
```bash
import condacolab
condacolab.check()
```

Get the Conda env file we are going to need and install the file
```bash
!wget https://raw.githubusercontent.com/MolSSI/mmic_autodock_vina/main/devtools/conda-envs/test_env.yaml
!mamba env update -n base -f test_env.yaml
!pip install git+https://github.com/MolSSI/mmic_autodock_vina.git
```

### Local machine
Make sure conda is installed on your system, then run the following:
```bash
conda env create -f https://raw.githubusercontent.com/MolSSI/mmic_autodock_vina/main/devtools/conda-envs/test_env.yaml
```

Then activate the `test` environment:
```bash
conda activate test
```

## MMIC workflows

- [Docking](https://molssi.github.io/mm_workflows/workflows/docking/qc.ipynb): QC-based ligand conformation generation for rigid-receptor docking.
- [Dynamics](https://molssi.github.io/mm_workflows/workflows/dynamics/md.ipynb): forcefield assignment, energy minimization, and molecular dynamics

## MMElemental
- [Molecule](https://molssi.github.io/mm_workflows/workflows/mmelemental/molecule.ipynb): molecule object creation from common file formats
- [ForceField](https://molssi.github.io/mm_workflows/workflows/mmelemental/forcefield.ipynb): forcefield object creation and manipulation
