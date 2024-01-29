# Tiny Diffusion Experiment

Diffusion method attempt to learn the underlying distribution of complex data, such as images. Trainig a diffusion model involeves iteratively transform a simple distribution (e.g., a noise distribution) into the desired complex data distribution. The model learns to generate realistic samples by iteratively adding noise to an initial noise vector, creating a sequence of correlated samples that approximate the true data distribution.

For experimenting with diffusion models and their potentials in learing the underlying distribution in data, this project attempts to investigate whether the model can effectively capture the underlying distribution of a maze structures and discern the existence of a continuous path. One can considering a black and white maze as a mathematical function based on pixel values. The distribution of white pixels must carry information about the structure of the maze and the presence of a continuous, uninterrupted path from one side to the exit on the other side. 

The training process involves presenting the diffusion model with a dataset of maze images, encoding the maze information into the model's parameters. After training, the model can be used to generate new maze image sample. By evaluating the generated images, one can assess whether the model has successfully learned the distribution of mazes with continuous paths, as evidenced by the coherent generation of paths from one side to the exit on the other side. This experiment helps study the potential of diffusion models in understanding and reproducing intricate spatial structures within images. 



<p align="center">
  <img  src="https://github.com/sabhaee/tiny_diffusion_experiment/blob/main/maze.png">
</p>
## Project Structure

The project structure is organized as follows:

- `requirements.txt`: This file contains the libraries and dependencies required to set up the project environment.
- `tiny_diffusion.ipynb`: This script perfoms trainig and generating new images
- `utllity_functions.py`: utility functions and classes necessary for training diffusion model.
- `/weights`: This directory should contain the .pth file for the saved model weights. The weights can be downloaded from the provided link (`best_svhn_model_state_MyModel_weights.pth`).
- `/plots`: This directory contains plots generated during the training process.
- `/data`: This directory should contain the training data. Download maze dataset from kaggle: [Maze Dataset](https://www.kaggle.com/datasets/emadehsan/rectangular-maze-kruskals-spanning-tree-algorithm).

## Usage

To use this project, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/sabhaee/tiny_diffusion_experiment.git
cd tiny_diffusion_experiment
```
2. Set up the project environment by installing the required libraries and dependencies listed in requirements.txt. Run the following command:
```bash
conda env create -f requirements.txt
```
3. Activate the created environment:

4. Use the tiny_diffusion.ipynb notebook to generate new maze images.

## Acknowledgments
