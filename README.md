# MRI k-Space Reconstruction

A personal biomedical engineering learning project by **Sivanji Alluri**. The notebook demonstrates how Fourier-domain MRI data changes under ideal acquisition, complex Gaussian noise, k-space truncation, and Cartesian undersampling.

## Why this project?

MRI reconstruction is an inverse problem: the scanner acquires spatial-frequency information (k-space), and an inverse Fourier transform is used to form an image. This project uses a small, synthetic 2D phantom so that the acquisition and reconstruction steps can be explored without patient data.

## Experiments

1. **Ideal reconstruction** — transform the phantom to centred k-space and back.
2. **Noise** — add complex Gaussian noise and compare the reconstructed image.
3. **K-space truncation** — remove high spatial frequencies and observe smoothing and Gibbs ringing.
4. **Undersampling** — retain every second phase-encoding line and observe fold-over aliasing.
5. **Quantitative comparison** — calculate RMSE for each reconstruction.

## Repository contents

```text
MRI-k-Space-Reconstruction/
├── mri_k_space_reconstruction.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

The notebook generates its own synthetic phantom. **No university assignment template, hidden grading cells, course-provided MRI dataset, or patient data are included.** The work is an independent educational simulation inspired by MRI Fourier-encoding and sampling concepts studied in biomedical engineering coursework; it is not a copy of a course submission.

## Run locally

Python 3.9 or newer is recommended. From this directory, install the dependencies and launch Jupyter:

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Open `mri_k_space_reconstruction.ipynb` and run the cells from top to bottom. The notebook only requires NumPy and Matplotlib at runtime.

## Main concepts

- 2D discrete Fourier transform and inverse transform
- Centred k-space representation
- Complex-valued measurement noise
- Spatial-frequency truncation and Gibbs ringing
- Cartesian undersampling and aliasing
- RMSE as a reconstruction metric
- SENSE and GRAPPA at a conceptual level

## Scope

This is a learning demonstration, not a clinical reconstruction tool. It omits many effects present in real MRI systems, including coil sensitivity encoding, relaxation, motion, gradient errors, non-Cartesian trajectories, and advanced reconstruction algorithms.
