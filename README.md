# Thesis project 
## The computational study of anxiety using AI algorithms

Neuro-Nav (Juliani, A. et. al, 2022), an open-source library for neurally plausible reinforcement learning (RL), was used to perform the simulations and program the RL models developed in the thesis project.  

The main modifications added to the neronav library are the following: 

- TDSR - finisehd to implement the B-pessimisitc module to the succesors function.
- TDSR_RP - added different learning rate for rewards and punishments to the TDSR model, which we call as a-SR.
- DynaSR_B - refeering to the Dyna B-pessimistic SR model implementation.
- DynaSR_RP - refeering to the Dyna a-SR model implementation.

As a side project a variation of the SR model with elegibility traces was programmed, as well as a model that combines the B-pessimisitc module and DynaSR_RP. 

- TDSR_ET - SR with temporal difference learning and alegibility traces.
- TDSR_AB - SR model that combines the B-pessimistic module and different learning rate for rewards and punishments.

See [agents](./agents) for more information.

## Poster presented at MAIN 2024 (Montreal Artificial Intelligence and Neuroscience)

"The Impact of Punishment Sensitivity and Learning Rate on Anxiety: A Computational Modeling Approach in a Sequential Evaluation Task". This work won the Best Undergraduate Poster Award.

Currently a scientific paper is in preparation, but you can see the [poster](.Poster_MAIN_2024.pdf) and [abstract](https://www.main2024.org/abstracts) of the work presented at MAIN.

## Experiment Notebook

A Google Colab Notebook includes the simulations made for the thesis project. 

See [Notebook.ipynb](./Notebook.ipynb) for more information.


## Requirements

Requirements for the `neuronav` library can be found [here](./setup.py).





## Reference


* Juliani, A., Barnett, S., Davis, B., Sereno, M., & Momennejad, I. (2022). Neuro-Nav: A Library for Neurally-Plausible Reinforcement Learning. The 5th Multidisciplinary Conference on Reinforcement Learning and Decision Making.


