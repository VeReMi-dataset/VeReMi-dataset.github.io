# VeReMi dataset

These pages describe the Vehicular Reference Misbehavior (VeReMi) dataset, a dataset for the evaluation of misbehavior detection mechanisms for VANETs.
This dataset consists of message logs of on-board units, including a labelled ground truth, generated from a simulation environment.
The dataset includes malicious messages intended to trigger incorrect application behavior, which is what misbehavior detection mechanisms aim to prevent.
The initial dataset contains a number of simple attacks: the idea of this dataset release is not just to provide a baseline for the comparison of detection mechanisms, but also to serve as a starting point for more complex attacks.
VeReMi is part of a recently accepted paper, submitted to the [SecureComm](http://securecomm.org/) conference.

## Overview

VeReMi is a **simulated** dataset, generated using [LuST](https://github.com/lcodeca/LuSTScenario) (Version 2) and [VEINS](http://veins.car2x.org/) (with modifications, based on Version 4.6).
It has two primary purposes: it serves as a baseline to assess how misbehavior detection mechanisms operate on a city scale, and it saves you a lot of computational power typically required to run VEINS sufficiently often.
VeReMi consists of three different density levels, five different attacks, and three different attacker densities.
The code and configuration files that are the input of VEINS are available in [a separate repository](https://github.com/VeReMi-dataset/veins).
We also provide a [popper](https://falsifiable.us) repository that contains all the scripts we used to generate the dataset (see below).

## Accessing &amp; Using VeReMi
To use VeReMi, or parts of the dataset, clone the corresponding repository, which is also [on github](https://github.com/VeReMi-dataset/VeReMi).
The repository uses [git-lfs](https://git-lfs.github.com/) to store the actual message logs, because their size exceeds the amounts suitable for git.

## Reproducing the Dataset

The repository with scripts that we used to generate the data (as well as all the other processing tasks done for the first paper) can be found [on github](https://github.com/VeReMi-dataset/VeReMi-popper).
We are currently working on making those scripts more portable -- right now, a lot of deployment happens manually, and this is only documented in notes in the scripts.
Please contact us if you have issues with these scripts.

## Extending the Dataset

There are many ways to extend the dataset: for example, running on a different subset of LuST, adding new attacks, or changing simulation parameters.
To add your results to this repository, please create a pull request on the [data repository](https://github.com/VeReMi-dataset/VeReMi) through the following steps:

 - publish your code (preferably as a fork of [VeReMi's fork of veins](https://github.com/VeReMi-dataset/veins))
 - fork VeReMi
 - clone VeReMi locally
 - create a folder in the repository and update the VeReMi `index.md` file
 - add your results into the new folder and use git LFS to add the message outputs
 - push your results to your fork on github
 - create a pull request in the github interface

Please note that at this stage we will only accept pull requests with public source code.
If you'd like to contribute real-world data, please contact us directly.

## Acknowledgement

The dataset was primarily put together by [Rens van der Heijden](https://www.uni-ulm.de/in/vs/inst/team/rens-van-der-heijden/) at the Institute of Distributed Systems, part of Ulm University. Please contact Rens if you have any questions, comments or criticism.
This work was supported in part by the [Baden-Württemberg Stiftung gGmbH Stuttgart](https://www.bwstiftung.de/) as part of the project IKT-05 [AutoDetect](https://www.uni-ulm.de/in/vs/res/proj/autodetect/) of its IT security research programme. Simulations for this work were performed on the computational resource bwUniCluster funded by the Ministry of Science, Research and the Arts Baden-Württemberg and the Universities of the State of Baden-Württemberg, Germany, within the framework program bwHPC.
