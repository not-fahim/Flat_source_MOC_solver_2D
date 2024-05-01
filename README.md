# Flat_source_MOC_solver_2D

This repo contains a 1D and a 2D solver for neutron transport equation by the Method of Characteristics using flat source approximation. The solver is written entirely in Python. So the solver is really slow as global interpreter lock in python does not allow it to use more than a single thread. 

For each solver there are 3 versions:
  1. **Fixed source solver**: Does source iteration for a fixed source until flux is converged.
  2. **One Group Eigenvalue Solver**: Finds the eigenvalue (or Keff) and flux distribution using power iteration method for problems with a single neutron energy group.
  3. **Multigroup Eigenvalue Solver**: Finds the eigenvalue (or Keff) and flux distribution using power iteration method for problems with multiple neutron energy group.

Each notebook file containing the solver has a geometry section in which a benchmark geometry is written and the solver's solution is displayed in the end of the notebook. One can edit the geometry section to solve any other problem having the same nature and rectangular geometries. In that case an array containig mesh of the problem and associated arrays of sigma values has to be declared.
