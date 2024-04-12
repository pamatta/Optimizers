
Certainly! Here's a text-friendly version of the README that includes all necessary details and the full script. This format will be suitable for GitHub repositories where the markdown might not render code snippets correctly or where plain text is preferred.

Gradient Descent Optimization Visualization
This project visualizes the trajectories of different gradient descent optimization algorithms on the function 
The algorithms included are Stochastic Gradient Descent (SGD), SGD with Momentum, AdaGrad, and Adam. Each method's progress is animated on a 3D plot to compare their performance and convergence behaviors dynamically.

Purpose
The main goal of this visualization is to provide an intuitive understanding of how different optimization algorithms navigate the landscape of a quadratic function. This helps in understanding the mechanics of each method, particularly in terms of speed and accuracy towards reaching the function's global minimum.

Requirements
Python 3.8+
NumPy
Matplotlib
PyQt5 (for the Qt5Agg backend)
Installation
Ensure you have Python installed, then run the following commands to install required packages:

Copy code
pip install numpy matplotlib PyQt5
If you encounter issues with the backend, you may need to adjust it based on your Python environment or the capabilities of your interactive display setup.

Usage
To run this script:

Save the script as optimize_animation.py.
Execute the script using a Python environment with the necessary packages installed:
Copy code
python optimize_animation.py
The script will open a window displaying the animation of each optimizer's path toward the minimum of the function.

Explanation of Algorithms
Stochastic Gradient Descent (SGD): Updates parameters in the opposite direction of the gradient of the objective function.

SGD with Momentum: Builds on SGD by incorporating the moving average of past gradients to dampen oscillations.

AdaGrad: Adapts the learning rate to the parameters, performing smaller updates on parameters associated with frequently occurring features.

Adam: Combines the advantages of AdaGrad and RMSProp, specifically designed to handle non-stationary objectives; it calculates an exponential moving average of the gradients and the squared gradients.

Hyperparameters
Learning Rate:

SGD, Momentum: 0.1
AdaGrad: 1.0
Adam: 0.1 (Adjusted to be higher than the default for demonstration purposes)
Momentum (for SGD with Momentum): 0.9

Adam specific:

beta1: 0.9 (The exponential decay rate for the first moment estimates)
beta2: 0.999 (The exponential decay rate for the second-moment estimates)

Function Definitions: Define the objective function and its gradient.
Optimizer Functions: Each optimizer is defined as a function that updates the point estimates.
Animation Setup: Using Matplotlib's FuncAnimation to animate the trajectory of each optimizer on a 3D surface plot.
Execution Loop: Applies each optimizer over a set number of iterations and records their trajectory.
Visual Output
The output is a 3D animated plot showing four subplots, each illustrating the path taken by one of the optimization algorithms in real-time as they move towards the function's minimum.
