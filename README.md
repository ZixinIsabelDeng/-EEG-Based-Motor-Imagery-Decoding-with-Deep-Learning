# EEG-Based-Motor-Imagery-Decoding-with-Deep-Learning

Overview
This project leverages advanced deep learning techniques to develop an EEG model using the Speechbrain library, based on the well-regarded EEGNet architecture. The objective was to explore the capabilities of EEGNet with modifications to enhance its performance on the BNCI2014001 dataset, which includes EEG recordings essential for brain-computer interface applications.

Dataset
The model was trained and validated on the BNCI2014001 dataset, a widely used benchmark in the EEG research community. This dataset offers a robust platform for training due to its diverse array of EEG recording settings.

Methodology
Framework: The project utilized Speechbrain, a versatile toolkit for processing speech and EEG data with PyTorch.
Architecture: Based on EEGNet, known for its efficiency in handling EEG data through deep learning.
Hyperparameter Optimization: Employed MOABB (Mother of All BCI Benchmarks) to run a HyperPyYAML file, facilitating a structured two-step hyperparameter search.

Data Preprocessing:
Data Augmentation: Enhanced the robustness of the model against overfitting and improved generalization.
Normalization: Standardized input features to improve model training efficiency.

Results
The fine-tuned EEGNet model achieved a performance metric (accuracy) of 0.492298 ± 0.015639, compared to the original EEGNet's performance of 0.731559±0.003888. Although the fine-tuned version did not surpass the original in performance, it provided valuable insights into parameter tuning and model scalability.

Requirements
To run the project, you will need the following:

Python 3.6+
PyTorch 1.4+
Speechbrain 0.5+
MOABB
HyperPyYAML


System Requirements:

GPU Availability: 
It is highly recommended to have a GPU to accelerate the training process. The model is configured to run using CUDA. If a GPU is not available, the setup can be altered to use the CPU.

Configuring the Environment:
Check for GPU: Ensure that a GPU is available in your system to utilize CUDA capabilities for faster computation.

Switch to CPU:
If a GPU is not available, you can change the configuration from 'cuda' to 'cpu'.

To do this, locate the device setting in the notebook where it specifies device='cuda' and change it to device='cpu'.

Note on Performance:
Using a GPU significantly speeds up the training process. Running the model on a CPU will work but expect the training to take an extensive amount of time.


Steps to Run:
Open the provided notebook in a Python environment that supports Jupyter (e.g., JupyterLab, colab).
Ensure all dependencies are installed as per the 'Requirements' section.
Follow the instructions within the notebook, adjusting the device configuration as necessary based on your hardware setup.
