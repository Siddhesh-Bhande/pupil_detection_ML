# Computer Vision Pupil Detection and Behavioral Gaze Analysis

A computer vision and machine learning analysis pipeline for automated human pupil boundary detection, gaze fixation mapping, and behavioral telemetry analysis.

## Overview

Precise pupillometry and gaze tracking are foundational to cognitive load estimation, human-computer interaction (HCI), and neurological diagnostic screening. This project develops an automated image processing and machine learning workflow to isolate the pupil ellipse, extract spatial coordinates, and correlate fixation patterns with behavioral reaction data.

## Methodology

1. **Image Preprocessing & Region of Interest (ROI)**:
   - Grayscale conversion, contrast adjustment (CLAHE), and Gaussian noise smoothing.
   - Thresholding and morphological closing operations to suppress corneal glare reflections.
2. **Pupil Center & Boundary Isolation**:
   - Contour extraction and Starburst / Hough Circle algorithms for ellipse fitting.
   - Sub-pixel center coordinate regression across progressive frame sequences.
3. **Behavioral Telemetry Correlation**:
   - Time-series synchronization of pupil diameter fluctuations with behavioral response latency logs (`subject_1_behave.csv`).

## Project Structure

```
pupil_detection_ML/
├── data/
│   ├── Behavioral_Data/       # Participant behavioral reaction time series
│   ├── Pupil_Data/            # Eye image frame sequences
│   ├── Test_Data/             # Evaluation frame sequences
│   └── subject_1_behave.csv   # Normalized trial timestamps and response tags
├── docs/
│   ├── Observations.docx                         # Empirical observations and error notes
│   └── Siddhesh_Bhande_Project2_report_v2.pdf    # Comprehensive experimental report
├── notebooks/
│   └── Source_Code.ipynb      # Main end-to-end CV detection pipeline and visualizations
├── .gitignore                 # Checkpoints, pycache, and OS ignore rules
├── LICENSE                    # MIT License
└── README.md                  # Methodology overview and setup instructions
```

## Getting Started

### Prerequisites
- Python 3.8+
- OpenCV (`cv2`)
- NumPy, Matplotlib, Pandas, Jupyter

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Siddhesh-Bhande/pupil_detection_ML.git
   cd pupil_detection_ML
   ```

2. Install dependencies:
   ```bash
   pip install opencv-python numpy matplotlib pandas jupyter
   ```

3. Launch Jupyter:
   ```bash
   jupyter notebook notebooks/Source_Code.ipynb
   ```

## Documentation

Full experimental methodologies, accuracy benchmarks under lighting variations, and mathematical formulations are available in [docs/Siddhesh_Bhande_Project2_report_v2.pdf](docs/Siddhesh_Bhande_Project2_report_v2.pdf).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
