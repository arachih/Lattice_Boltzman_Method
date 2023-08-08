# 2D Flow Around a Cylinder Simulation

This repository contains a Python script that simulates 2D flow around a cylinder using the lattice Boltzmann method. The lattice Boltzmann method is a popular numerical technique for simulating fluid flow and is particularly well-suited for parallel computation.

## Description

The script implements a 2D lattice Boltzmann simulation of fluid flow around a cylindrical obstacle. It uses the D2Q9 lattice with nine discrete velocity directions and the Bhatnagar-Gross-Krook (BGK) collision model.

The key features of the simulation include:
- 2D flow simulation using the lattice Boltzmann method.
- Definition of a cylindrical obstacle in the flow domain.
- Velocity inlet with a slight perturbation to trigger instability.
- Outflow and inflow boundary conditions.
- Visualization of the velocity field during the simulation.

## Prerequisites

Before running the simulation, ensure you have the following installed on your system:
- Python 3.x
- NumPy
- Matplotlib

## Usage

1. Clone the repository to your local machine.

2. Open a terminal or command prompt and navigate to the cloned repository directory.

3. Run the simulation script using the following command:

   ```
   python cylinder_flow_simulation.py
   ```

4. The script will execute the simulation and save the visualization of the velocity field at regular intervals.

## Parameters

The following parameters can be modified in the script to adjust the simulation behavior:

- `maxIter`: Total number of time iterations.
- `Re`: Reynolds number of the flow.
- `nx`, `ny`: Number of lattice nodes in the x and y directions.
- `ly`: Height of the domain in lattice units.
- `cx`, `cy`, `r`: Coordinates of the cylinder and its radius.
- `uLB`: Velocity in lattice units.
- `nulb`: Viscosity in lattice units.
- `omega`: Relaxation parameter for the BGK collision model.

## Output

During the simulation, visualizations of the velocity field will be saved in PNG format at regular intervals. The output files will be named `vel.XXXX.png`, where `XXXX` represents the time step.


## Examples

Here are visualizations of the simulation results using different methods:

### Fluent

![til](./figs/fluent.gif)

### OpenFOAM

![til](./figs/of.gif)

### Lattice Boltzmann

![til](./figs/lbm.gif)


## Acknowledgments

This simulation script is based on the lattice Boltzmann method provided by EPFL course on Coursera. I would like to acknowledge their contributions and research.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify the code for your purposes. If you find this project helpful, I would appreciate it if you provide attribution or mention this repository in your work.

