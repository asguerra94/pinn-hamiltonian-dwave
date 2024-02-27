# Physics Informed Neural Network for a Hamiltonian D-Wave system

## Description

This repository is our project for the Qhack 2024 presented by Antonio Guerra and Mauricio Casanova. Inspired by the internal conections inside our brain, Neural Networks (NN) consists of layers made by nodes (also known as neurons). Those layers are connected to each other one-by-one and several mathmatics operations are made by each neuron. Finally, after a previous calibration of those mathmatics operations (also known as train the NN), for a certain input value on the first layers give us a specific result in the last layer.

Many types of Neural Networks has been developed, being forward neural network (FNN) the simplest one for our purposes. In [1] the authors make a complete mathmatical description for FNN and, particularly, they describe how to use FNN to solve partial differential equations (PDEs). This way of working with FNN is known as Physics-Informed Neural Network (PINN) and it consists to train a neural network to simulate the solution of a PDE with specific constrains.

There are an infinite number of problems that can be modeled with PDE. For example, Einstein's field equation used in gravitation, the wave equation used to describe oscillations, Maxwell's equations to describe different electromagnetic effects, Schrodinger's equation to describe the evolution of quantum states, etc.

Our project consists of training a neural network to simulate the temporal evolution of a set of observables to describe the measurements made in a quantum system. Specifically, we use Pennylane to simulate the value of a set of observables at differents times and, then, we use those data to train our PINN. We consider a D-wave system that is describe by a Hamiltonian given by

$$ H = \frac{\hbar}{2} \left[ J_1 (\sigma_0 \otimes \sigma_x + \sigma_x \otimes \sigma_0) + J_2 (\sigma_0 \otimes \sigma_z + \sigma_z \otimes \sigma_0) + J_3 \sigma_z \otimes \sigma_z \right], $$

where $\sigma_i$, $i = 0,1,2,3$ are the Pauli matrices with 0 for the identity.

D-wave systems are used to characterizing superconductivity matherials. They represent a significant interest in Condensed Matter Physics and they are related to systems with strong electron-electron interactions, such as high-temperature superconductors.

[1] https://doi.org/10.1137/19M1274067

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Installation

Libraries as PyTorch, Nympy, Matplotlib and Pennylane are used for this project. Before to run our program, be sure that previous libaries are correctly installed. To install them using pip just run in the terminal the following command.

```
pip install numpy pennylane matplotlib torch torchvision
```

## Usage

After install the necessary libraries, just run this project and feel free to change the parameters of the system and neural network.

## Contributing

We welcome contributions from the community! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/my-feature`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature/my-feature`).
6. Create a new Pull Request.

Please ensure that your contributions adhere to our [code of conduct](CODE_OF_CONDUCT.md).

## License

[Indicate the license under which the project is distributed. For example, MIT, Apache 2.0, etc.]

```
[License Text]
```

## Additional Information

[Include any additional information that may be relevant, such as contact information, project status, or acknowledgments.]
