# NeRC (Coming Soon) 
The codes are the implementation of the following paper that has been accepted by the <a href="https://sensys.acm.org/2026/">ACM/IEEE International Conference on Embedded Artificial Intelligence and Sensing Systems (SenSys 2026)</a> with an acceptance rate of 18.99%:

`Weng, X., Ling, K. V., Liu, H., Wang B., & Cao K. (2025). NeRC: Neural Ranging Correction through Differentiable Moving Horizon Location Estimation. arXiv:2508.14336 [cs.LG].`
<!--- Badge for paper link---> <a href="https://doi.org/10.48550/arXiv.2508.14336"><img src="https://img.shields.io/badge/ACM/IEEE%20SenSys '26-paper-green"/></a>
<!--- Badge for paper link---> <a href="https://doi.org/10.48550/arXiv.2508.14336"><img src="https://img.shields.io/badge/arXiv%202025-paper-informational"/></a>

## Configure Running Environment
This section introduces how to set up the environment to run NeRC from scratch, step by step. We also provide an environment file for rapid configuration:

`$ conda env create -f nerc_environment.yml`

However, it would be better to follow the guides to set up your own environment.

### Recommended Prerequisites:
* An NVIDIA GPU with no less than 16 GB of memory
* Ubuntu 18.04.6 LTS and later (we have successfully tested NeRC on Ubuntu 18.04.6 LTS and Ubuntu 24.04.3 LTS)
* Python 3.10 (for fast installation of Theseus)
* A PyTorch version compatible with CUDA 11.6 (for fast installation of Theseus)

Other versions of Python, PyTorch, and CUDA may also work. However, for rapid replication of our results, we recommend the settings above, primarily to facilitate the installation of <a href="https://github.com/facebookresearch/theseus">Theseus</a>.

### Step-by-step Guide:
* Create a new environment using <a href="https://www.anaconda.com/docs/getting-started/miniconda/install#linux-terminal-installer">conda</a>: `$ conda create --name nerc python=3.10 -y`
* Activate the nerc environment: `$ conda activate nerc`
* Install and update pip in the environment: `$ python -m pip install -U pip`
* Install <a href="https://pytorch.org/get-started/locally/">PyTorch</a>: `$ pip install torch==1.13.1+cu116 torchvision==0.14.1+cu116 torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cu116py`
* Install <a href="https://d2l.ai/">d2l</a> package (for visualizing training progress and friendly to beginners): `$ pip install -U d2l`
* Install the prerequisite <a href="https://people.engr.tamu.edu/davis/suitesparse.html">suitesparse</a> for <a href="https://github.com/facebookresearch/theseus">Theseus</a>: `$ sudo apt-get install libsuitesparse-dev`
* Install <a href="https://github.com/facebookresearch/theseus">Theseus</a>: `pip install theseus-ai`
* Install pymap3d for horizontal distance calculation: `$ pip install pymap3d`
* Install tqdm for progress bar display: `$ pip install tqdm`


## Datasets

## Training

## Inference

## NeRC on the Edge
This section presents how to deploy NeRC on edge servers.

## GnssQuest App on Android
This section introduces our developed GnssQuest app, which communicates with edge servers running NeRC.

## Baseline Methods




