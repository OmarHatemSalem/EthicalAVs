# Ethical AV Modelling

This repository provides ethical evaluation of car scenery using concepts of graph and order theory. It builds on the `CommonRoad` simulator and ethical trajectory planning algorithm built by Geisslinger et al. at TUM.

## System Requirements
* Operating System: Linux Ubuntu (tested on 22.04)
* Programming Language: Python >= 3.7 (tested on 3.8)
* [Software Dependencies](/requirements.txt)


## Installation

The installation of this repository takes around 10 min and consists of three steps.
We recommend using an isolated [virtual environment](https://pypi.org/project/virtualenv/) for installation.

1. Clone this repository with:

    `git clone https://github.com/TUMFTM/EthicalTrajectoryPlanning.git`

2. Navigate to the root folder of the repository (`[..]/EthicalTrajectoryPlanning`) and install requirements:

    `pip install -r requirements.txt`

3. Download [CommonRoad scenarios](https://gitlab.lrz.de/tum-cps/commonroad-scenarios) by cloning the scneario repository next to this repository:

    `git clone https://gitlab.lrz.de/tum-cps/commonroad-scenarios`

    so that you have the following folder structure:

    ```
    ├── EthicalTrajectoryPlanning (This repository)
    ├── commonroad-scenarios
    ```

    [Results](#how-to-reproduce-results) were obtained with commonroad-scenarios at commit `35b9cfb5b89d33249ea0d5507b9465650ebeb289`.
    Instead of cloning you can download and unpack this commit directly with:
    
    `wget -c  https://gitlab.lrz.de/tum-cps/commonroad-scenarios/-/archive/35b9cfb5b89d33249ea0d5507b9465650ebeb289/commonroad-scenarios-35b9cfb5b89d33249ea0d5507b9465650ebeb289.tar.gz -O - | tar -xz`

# Quick Start Demo

To run the ethical planner on an exemplary default scenario, execute the following command from the root directory of this repository:
    
* `python planner/Frenet/frenet_planner.py`

![Exemplary Result](readme/running_sample.gif)

You will see a live visualization of the scenario being solved by the planner.
Now you can start with your own experiments by changing the [configs](/planner/Frenet/configs/README.md) or selecting another scenario by adding

* `--scenario <path-to-scenario>`

to the command.