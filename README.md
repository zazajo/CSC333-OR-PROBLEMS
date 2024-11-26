# CSC333-OR-PROBLEMS
Project Title: Linear Programming Problem Solver
Project Description

This project focuses on solving Linear Programming (LP) problems using Python. Linear Programming is a mathematical optimization technique used to achieve the best outcome (e.g., maximum profit or minimum cost) in a mathematical model where the requirements are represented as linear relationships.

The goal of this project is to:

    Define a set of constraints and an objective function.
    Utilize Python libraries, such as scipy.optimize, to solve the LP problems efficiently.
    Provide a reusable framework to solve custom LP problems with clear instructions for users.

Objective

The primary objective of this project is to:

    Develop a Python-based solution to LP problems.
    Maximize or minimize an objective function under given constraints.
    Demonstrate how LP techniques can be applied to real-world scenarios, such as resource allocation, supply chain optimization, or financial planning.

Solution Approach

The LP problems were solved using the following steps:

    Defining the Problem:
        Specify the objective function (e.g., maximize Z=3x+4yZ=3x+4y).
        List the constraints (e.g., 2x+y≤14,x+3y≤182x+y≤14,x+3y≤18).
        Ensure all variables are non-negative (x,y≥0x,y≥0).

    Using Python Libraries:
    The scipy.optimize.linprog function was utilized. It implements the Simplex or Interior Point method to find optimal solutions.

    Solving the Problem:
        Input the coefficients of the objective function, constraints, and bounds into the linprog function.
        The function returns the optimal values for the decision variables and the maximum/minimum value of the objective function.

    Validating Results:
    After obtaining results, the solution was validated by manually checking if the constraints were satisfied and whether the optimal solution aligned with expectations.

How to Run the Python Code
Requirements

    Python 3.7 or above
    Required Python libraries:
        scipy
        numpy (optional, for numerical operations)
    A code editor (e.g., VS Code, PyCharm) or Jupyter Notebook for interactive exploration.

Setup

    Clone or download the repository:

git clone https://github.com/username/project-repo.git
cd project-repo

Install the required libraries:

    pip install scipy numpy

Usage

    Open the main script lp_solver.py in your code editor.
    Modify the objective_function and constraints variables according to your problem.

# Example
# Coefficients of the objective function: Maximize Z = 3x + 4y
objective_function = [-3, -4]  # Use negative values for maximization

# Coefficients of the constraints
lhs_constraints = [[2, 1], [1, 3]]  # Left-hand side coefficients
rhs_constraints = [14, 18]          # Right-hand side values

# Variable bounds (x >= 0, y >= 0)
bounds = [(0, None), (0, None)]

Run the script:

    python lp_solver.py

    The output will display:
        The optimal values of the decision variables.
        The maximum or minimum value of the objective function.

Example Output

For the sample problem Z=3x+4yZ=3x+4y, subject to:

    2x+y≤142x+y≤14
    x+3y≤18x+3y≤18
    x,y≥0x,y≥0

The output is:

Optimal Solution Found:
x = 4.0, y = 5.0
Maximum Value of Z = 32.0
