# Algorithm Toolkit

A set of cognitive neuroscience inspired agents and learning algorithms.

These consist of implementations of the canonical Successor Representation algorithms and more.


## Included algorithms

The main modifications added to the neronav library for the present work are the development of the following models:

**Found in [/td_agents.py](./td_agents.py) :**
* TDSR_A – Implemented different learning rates for rewards and punishments based on the original TDSR model, in order to develop the alpha-SR model.
* TDSR_B – Implemented the B-pessimistic module to allow differentiated sensitivity parameters for rewards and punishments within the successor representation function of the original TDSR model, constructing the beta-SR model.

**Found in [/dyna_agents.py](./td_agents.py) :**
* DynaSR_A – Developed the Dyna alpha-SR model using the TDSR_A model as a basis, along with the original Dyna SR algorithm from the library.
* DynaSR_B – Developed the Dyna beta-SR model using the TDSR_B model as a basis, along with the original Dyna SR algorithm from the library.

The algorithms' code from the original library that was not used in this work was removed to improve the organization of the information. However, the full codebase of the neuronav library can be accessed at the following [link](https://github.com/awjuliani/neuro-nav). 

It is also important to note that the algorithms of the library - TDSR and Dyna SR - used as foundation to construct the models of this work,  were originally developed based on the article by [Dayan, 1993](https://ieeexplore.ieee.org/abstract/document/6795455) for the TDSR algorithm, and the model proposed by [Russek et al., 2017](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005768) for the DynaSR implementation, which incorporates one-step temporal difference and replay-based Dyna learning. 


## Algorithm hyperparameters

Below is a list of the common hyperparameters shared between all algorithms and agent types. Typical value ranges provided are meant as rough guidelines for generally appropriate learning behavior. Depending on the nature of the specific algorithm or task, other values may be more desirable.

* `lr` - Learning rate of algorithm. Typical value range: `0` - `0.1`.
* `gamma` - Discount factor for bootstrapping. Typical value range: `0.5` - `0.99`.
* `poltype` - Policy type. Can be either `softmax` to sample actions proportional to action value estimates, or `egreedy` to sample either the most valuable action or random action stochastically.
* `beta` - The temperate parameter used with the `softmax` poltype. Typical value range: `1` - `1000`.
* `epsilon` - The probablility of randomly acting using with the `egreedy` poltype. Typical value range: `0.1` - `0.5`.
