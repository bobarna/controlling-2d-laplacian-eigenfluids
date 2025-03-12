# Controlling 2D Laplacian Eigenfluids
This is the source code repository for the CESCG 2023 paper [Controlling 2D
Laplacian Eigenfluids](https://cescg.org/wp-content/uploads/2023/04/Borcsok-Controlling-2D-Laplacian-Eigenfluids-6.pdf).

The Central European Seminar on Computer Graphics (CESCG) is an annual student
seminar (non-peer reviewed). [More info](https://cescg.org/)

## Abstract
Understanding and modeling our environment is a great and important challenge,
spanning many disciplines from weather and climate forecast, through vehicle
design to computer graphics. Physical systems are usually described by Partial
Differential Equations (PDEs), which we can approximate using established
numerical techniques. Next to predicting outcomes, planning interactions to
control physical systems is also a long-standing problem.

In our work, we investigate the use of Laplacian Eigenfunctions to model and
control fluid flow. We make use of an explicit description of our simulation
domain to derive gradients of the physical simulation, enabling neural network
agents to learn to control the physical process to achieve desired outcomes.

## Citation
If you found this work useful in your research, please consider citing it using the following BibTeX entry:
```
@inproceedings{borcsok2023,
  title       = {Controlling 2D Laplacian Eigenfluids},
  author      = {B{\"o}rcs{\"o}k, Barnab{\'a}s and Sz{\'e}csi, L{\'a}szl{\'o}},
  booktitle   = {Proceedings of CESCG 2023: The 27th Central European Seminar on Computer Graphics},
  year        = {2023},
  url         = {https://cescg.org/wp-content/uploads/2023/04/Borcsok-Controlling-2D-Laplacian-Eigenfluids-6.pdf}
}
```

## Running the Code
### Dependencies
- [Φ<sub>Flow</sub>](https://github.com/tum-pbs/PhiFlow)
    - dash
- [Pytorch](https://pytorch.org/)
- [Tensorflow](https://www.tensorflow.org/) -- as an alternative backend
- [Jupyter notebook](https://jupyter.org/install) -- for running the notebooks

All of these can be installed via [pip](https://pypi.org/project/pip/) on
[Python 3.6](https://www.python.org/downloads/) and above:
```
pip install phiflow==2.2.2 dash torch torchvision tensorflow
pip install notebook
```

### Running the Notebooks
#### Locally
```
jupyter notebook
```
#### In Google Colab 
- [Intro](https://colab.research.google.com/github/bobarna/controlling-2d-laplacian-eigenfluids/blob/main/eigenfluid-intro.ipynb)
- [Optimization -- Velocity Only](https://colab.research.google.com/github/bobarna/controlling-2d-laplacian-eigenfluids/blob/main/eigenfluid-optimization-velocity-only.ipynb)
- [Optimization -- Initial Velocity for Points](https://colab.research.google.com/github/bobarna/controlling-2d-laplacian-eigenfluids/blob/main/eigenfluid-optimization-points.ipynb)
- [Optimization -- Control Force](https://colab.research.google.com/github/bobarna/controlling-2d-laplacian-eigenfluids/blob/main/eigenfluid-force-optimization.ipynb)
- [Neural Network for Control Force Estimation](https://colab.research.google.com/github/bobarna/controlling-2d-laplacian-eigenfluids/blob/main/network-training.ipynb)
- [Shape sampling demo](https://colab.research.google.com/github/bobarna/controlling-2d-laplacian-eigenfluids/blob/main/shape-samples-demo.ipynb)

### Code Layout
- `src/`: Python/Φ<sub>Flow</sub> source code, imported in the notebooks
- `*.ipynb`: interactive notebook files
