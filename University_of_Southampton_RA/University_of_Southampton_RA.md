# University of Southampton 
* Industry collabrator: Airbus

👩‍⚕️ Research Fellow, Digital Design Engineer   
🗓️ Nov. 2023 – Nov. 2024  
📍 Southampton, UK 

## Algorithmic Pathfinding & Graph Theory
•	3D High-Density Discretisation: Discretisation the complex 3D aeronautical geometries using Rihno, Grasshopper (3D modelling) into mathematical graphs using Python, NetworkX. Managed a high-resolution search space, integrating orthogonal, face-diagonal, and cubic-diagonal vectors to maximize path precision.
•	Multi-Objective Spatial Optimization: Programmed a custom search engine utilising A* and Dijkstra algorithms to minimize a global cost function. The logic optimised for minimal cable weight (path length) while simultaneously navigating dense regulatory and structural constraints.
•	NURBS-Based Geometric Synthesis: Developed a novel algorithm utilising Non-Uniform Rational B-Splines (NURBS) to interpolate discrete paths into physically realistic 3D geometries. Integrated control laws to enforce outlet/inlet vector alignment and ensure strict adherence to minimum bending radius constraints based on cable physical properties.

## Combinatorial Optimisation & Constraint Logic
•	Genetic Algorithm (TSP) Implementation: Modelled the cable installation sequence as a Constrained Traveling Salesman Problem (TSP). Employed the DEAP framework to execute permutation-based genetic algorithms, achieving a 3.5% reduction in total system mass.
•	Dynamic Rule & Penalty Enforcement: Translated qualitative aerospace regulations into quantitative penalties. Used KD-Tree spatial indexing for rapid nearest-neighbour queries to enforce "Separation" (redundancy safety) and "Harnessing" (structural affinity/bundling) in real-time.
•	Geometric Packing Solver: Developed a solver for the "Smallest Enclosing Circle" problem to dynamically calculate bundle diameters. Implemented recursive splitting logic that triggers when a bundle's diameter exceeds structural rib aperture limits.
•	Environmental Heat Avoidance: Engineered thermal sensitivity logic that dynamically increases graph edge weights near "Hot Zones" (e.g., engines) to steer automated routing toward safer thermal environments.
## Visualization & Interactive Systems
•	Full-Stack Optimization Dashboard: Developed a web-based interactive interface using Plotly and Dash to visualize 3D graph networks and pipe-rendered cable paths. Built a "click-and-trace" mechanism for real-time inspection of bundle thickness and cable metadata.
•	Human-in-the-Loop Sensitivity Interface: Created a parametric interface allowing users to manipulate optimisation weights (e.g., prioritizing harnessing vs. separation) and instantly visualize the impact on the global routing solution.
