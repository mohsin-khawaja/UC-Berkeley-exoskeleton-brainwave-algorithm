# UC Berkeley Exoskeleton Brainwave Algorithm

**UC Berkeley Exoskeleton Brainwave Algorithm** is a Python-based framework that processes EEG/EOG recordings, classifies gaze or motor intentions, and translates those signals into real-time commands for an assistive exoskeleton. Building on established neuroimaging toolkits and machine learning pipelines, this repository brings brain–machine interfacing into a robotics context.

## Features

- **EEG & EOG Data Processing**  
  • Import raw EEG/EOG files (e.g. `.fif`, `.edf`)  
  • Band-pass filter, notch filter, artifact rejection  
  • Epoching and baseline correction  

- **Feature Extraction & Machine Learning**  
  • Compute statistical features (mean, variance, skewness, kurtosis)  
  • Time- and frequency-domain feature sets  
  • Train and evaluate Random Forest (or other scikit-learn) classifiers  
  • Persist models for offline or online use  

- **Real-Time Exoskeleton Control**  
  • Stream new EEG/EOG data in real time (via LSL or custom I/O)  
  • Classify each incoming window for “left” vs. “right” (or other intentions)  
  • Send control signals (e.g. via ROS or socket) to exoskeleton actuators  

- **Visualization & Monitoring**  
  • Plot raw and filtered time series  
  • Topographic scalp maps and 3D field reconstructions (using MNE & PyVista)  
  • Live dashboard for prediction confidence and actuator status  

- **Hardware-Agnostic Framework**  
  • Easily swap in different acquisition systems or exoskeleton interfaces  
  • Configurable via YAML/JSON for channel layouts, filter parameters, model paths  

## Installation

1. **Clone this repository**  
   ```bash
   git clone https://github.com/mohsin-khawaja/UC-Berkeley-exoskeleton-brainwave-algorithm.git
   cd UC-Berkeley-exoskeleton-brainwave-algorithm
