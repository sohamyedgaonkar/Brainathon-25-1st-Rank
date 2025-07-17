# Brainathon 25 EEG Analysis Workflow

Welcome to the **Brainathon 25 EEG Analysis** repository! This project provides a comprehensive workflow for analyzing EEG data collected during cognitive tasks, as implemented in [`Brainathon.ipynb`](Brainathon.ipynb).

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Workflow Steps](#workflow-steps)
  - [1. Data Loading](#1-data-loading)
  - [2. Preprocessing](#2-preprocessing)
  - [3. Denoising](#3-denoising)
  - [4. Visualization](#4-visualization)
  - [5. Feature Extraction](#5-feature-extraction)
  - [6. Saving Processed Data](#6-saving-processed-data)
- [Usage](#usage)
- [Results](#results)
- [References](#references)

---

## Overview

This repository contains a Jupyter notebook that guides users through the complete process of EEG data analysis for Brainathon 25. The workflow covers data loading, preprocessing, denoising, visualization, feature extraction, and exporting processed data. Each step is documented for clarity and reproducibility.

## Project Structure

- [`Brainathon.ipynb`](Brainathon.ipynb): Main notebook containing the analysis workflow.
- [`Brainathon 25 Soham_Yedgaonkar.pdf`](Brainathon%2025%20Soham_Yedgaonkar.pdf): Project report or supplementary documentation.
- [`README.md`](README.md): Project overview and instructions.

## Requirements

To run the notebook, ensure you have the following Python packages installed:

- `numpy`
- `pandas`
- `matplotlib`
- `scipy`
- `mne` (for EEG data handling)
- `sklearn` (for machine learning tasks, if applicable)
- `pywt` (for wavelet transforms, if used)

Install dependencies using:

```sh
pip install numpy pandas matplotlib scipy mne scikit-learn pywt
```

## Workflow Steps

### 1. Data Loading

- Imports raw EEG data files from various cognitive tasks.
- Supports common EEG formats (e.g., `.edf`, `.csv`).
- Example:
  ```python
  import mne
  raw = mne.io.read_raw_edf('subject1.edf')
  ```

### 2. Preprocessing

- Applies bandpass filtering to remove unwanted frequencies.
- Removes artifacts (e.g., eye blinks) using ICA or other methods.
- Normalizes signals for consistency.

### 3. Denoising

- Uses advanced techniques such as Independent Component Analysis (ICA) or wavelet transforms to further reduce noise.
- Improves signal quality for downstream analysis.

### 4. Visualization

- Plots time-series EEG signals.
- Generates power spectral density (PSD) plots.
- Creates topographic brain maps for spatial analysis.

### 5. Feature Extraction

- Computes features like band power (alpha, beta, theta, delta).
- Extracts event-related potentials (ERPs) if applicable.
- Prepares features for statistical analysis or machine learning.

### 6. Saving Processed Data

- Exports cleaned and processed EEG data to CSV or other formats.
- Facilitates further analysis or modeling outside the notebook.

## Usage

1. Clone the repository:
   ```sh
   git clone <repo-url>
   cd Brainathon-25-1st-Rank
   ```
2. Open [`Brainathon.ipynb`](Brainathon.ipynb) in Jupyter Notebook or VS Code.
3. Follow the step-by-step workflow, modifying paths and parameters as needed for your data.

## Results

- Cleaned EEG datasets ready for analysis.
- Visualizations for interpretation of cognitive task data.
- Extracted features for statistical or machine learning models.

## References

- [MNE Documentation](https://mne.tools/stable/index.html)
- [EEG Signal Processing](https://www.sciencedirect.com/topics/engineering/eeg-signal-processing)
- [Wavelet Transform for EEG](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6422461/)

---

For questions or contributions, please open an issue or submit a pull request.
