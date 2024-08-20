Spike sorting plays a critical role in analyzing neural signals captured by high-density multi-electrode arrays (HD-MEAs). This project focuses on evaluating and optimizing feature extraction and clustering methods for spike sorting in neural data.

# Project Overview
Advancements in neurotechnology have enabled the recording of neuronal activity with unprecedented detail using HD-MEAs. Spike sorting, the process of distinguishing and categorizing neuronal action potentials, is pivotal for interpreting these complex signals. This project investigates various feature extraction and clustering methods to enhance spike sorting accuracy in neural data obtained from HD-MEAs.

Key methodologies include:

- Feature Extraction: Principal Component Analysis (PCA), Independent Component Analysis (ICA), Uniform Manifold Approximation and Projection (UMAP), Isometric Mapping (Isomap)
- Clustering Algorithms: K-means, Agglomerative Clustering, HDBSCAN, Mean Shift
- Performance Metrics: Accuracy, Precision, Recall
Systematic parameter tuning and rigorous performance evaluation reveal that combining HDBSCAN with PCA offers superior performance with an accuracy of 0.87. This combination effectively minimizes noise while preserving essential data features.

The project also considers the computational complexities of these methods to balance effectiveness and efficiency, guiding future developments in brain-machine interfaces and neurological research.

# Getting Started
These instructions will guide you through setting up the development environment for running the project locally.

1. Clone the Repository
First, clone the forked repository to your local machine:
git clone https://github.com/SpikeInterface/spikeinterface.git
cd YourRepoName

2. Setting Up a Virtual Environment
It is recommended to use a virtual environment to isolate project dependencies. You can set it up using Python’s 'venv' module or 'conda':

Using venv (Python’s Built-in Virtual Environment)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Using conda (Anaconda/Miniconda)
conda create -n spikeinterface-env python=3.8
conda activate spikeinterface-env

3. Installing Dependencies
Once the virtual environment is activated, install the required dependencies. Depending on your needs, you can install the full suite of SpikeInterface packages or customize it.

For full installation (including all extra features):
pip install "spikeinterface[full]"

If your project includes additional dependencies or specific packages, list them in a requirements.txt file and install them with:

pip install -r requirements.txt

You can also install from the forked source code to get the latest updates:
pip install -e .

4. Running Your Custom Code
After setting up the environment and installing the dependencies, you can start running your custom scripts:
jupyter notebook Feature_Analysis.ipynb

To get the latest updates, you can install spikeinterface from source:
git clone https://github.com/SpikeInterface/spikeinterface.git
cd spikeinterface
pip install -e .
cd ..


4. Project Structure
- features/: Contains feature extraction modules.
- pca_model/: Pre-trained PCA models.
- simulated_short_recording/: Simulated neural data.
- sortinganalyser/: Scripts related to clustering and evaluation.
- src/: Core source code.
- gt_analyzer_results/: Ground truth results.
- waveforms_*: Datasets and recordings used for analysis.

5. Citing the Project
bibtex
@article{buccino2020spikeinterface,
  title={SpikeInterface, a unified framework for spike sorting},
  author={Buccino, Alessio Paolo and Hurwitz, Cole Lincoln and Garcia, Samuel and Magland, Jeremy and Siegle, Joshua H and Hurwitz, Roger and Hennig, Matthias H},
  journal={Elife},
  volume={9},
  pages={e61834},
  year={2020},
  publisher={eLife Sciences Publications Limited}
}


