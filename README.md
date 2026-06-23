# rsCVR Projects
This repository contains analysis codes for resting-state cerebrovascular reactivity (rsCVR) projects.  
The repository is intended to organise Jupyter notebooks, MATLAB/SPM scripts, and Python-based workflows used for resting-state BOLD preprocessing, SPM-based image processing, rapidtide lag analysis, rsCVR map generation, and quality-control procedures.

# Project overview
The main project included in this repository focuses on the development and organisation of an rsCVR analysis workflow using resting-state BOLD MRI.  
The analysis workflow includes:  
- environment checking and package validation
- data indexing and manifest generation
- directory structure preparation
- SPM-based realignment and reslicing
- meanBOLD generation
- T1-to-meanBOLD coregistration
- tissue segmentation using SPM
- spatial normalisation
- temporal preprocessing
- rapidtide-based lag analysis
- rsCVR-related map generation
- quality control and visualisation
  
The repository currently includes code-only materials. Raw MRI data, NIfTI files, SPM outputs, rapidtide outputs, intermediate derivatives, figures, and generated result files are intentionally excluded.
  
# Repository structure
```text
rsCVR_Projects/
│
├── KHNMC_RapidtideProcessing.ipynb
│   └── Rapidtide processing workflow for KHNMC rsCVR data
│
├── rsCVR M02-1 EnvCheck_Apr2026.ipynb
│   └── Environment and package-checking workflow
│
├── rsCVR M02-2 DataIndexing_Apr2026.ipynb
│   └── Data indexing and file-structure inspection
│
├── rsCVR M02-3 manifest-DIRs Making_Apr2026.ipynb
│   └── Manifest and project directory generation
│
├── rsCVR M02-4 SPM-Testing_Apr2026.ipynb
│   └── Initial SPM execution and testing workflow
│
├── rsCVR M02-5 SPM-PrepTrial_Apr2026.ipynb
│   └── Trial preparation for SPM-based preprocessing
│
├── rsCVR M02-6R3 SPM-Batch Realignment testing_Apr2026.ipynb
│   └── SPM batch realignment testing workflow
│
├── rsCVR M02-7 SPM-Batch Realignment_Apr2026.ipynb
│   └── SPM batch realignment workflow
│
├── rsCVR M02-8 CoRegist-SpatialNorm-Segmentation_Apr2026.ipynb
│   └── Coregistration, spatial normalisation, and segmentation workflow
│
├── rsCVR M02-9 Rapidtide_processing_May2026.ipynb
│   └── Rapidtide-based lag analysis and rsCVR processing workflow
│
├── rsCVR_BET_Mod1.ipynb
│   └── Brain extraction and mask-related workflow
│
├── rsCVR_preprocessed-SPM_Jun2026.ipynb
│   └── *SPM-preprocessed rsCVR analysis workflow
│
├── pyscript.m
│   └── MATLAB/SPM script
│
├── pyscript_realign.m
│   └── MATLAB/SPM realignment script
│
├── README.md
└── .gitignore
```

# Main analysis components
1. Environment checking  
The environment-checking notebooks are used to confirm that the required Python, MATLAB Runtime, SPM, and rapidtide-related components are available in the analysis environment.
  
2. Data indexing and manifest generation  
The data-indexing workflow organises resting-state BOLD and anatomical MRI file paths, prepares analysis manifests, and supports reproducible project-level directory handling.
  
3. SPM-based preprocessing  
The SPM-related notebooks and MATLAB scripts include workflows for realignment, reslicing, meanBOLD generation, T1-to-meanBOLD coregistration, segmentation, and spatial normalisation.
  
4. Temporal preprocessing  
The temporal preprocessing workflow includes preparation steps for resting-state BOLD time-series analysis, including detrending and frequency filtering according to the rsCVR analysis pipeline.
  
5. Rapidtide-based lag analysis  
The rapidtide processing workflow is used for lag estimation and rsCVR-related map generation using resting-state BOLD signals.
  
6. Quality control and visualisation  
The repository includes workflows for checking image dimensions, affine information, masks, preprocessing outputs, and rsCVR-related maps.
  
# Data availability
Raw MRI data and generated neuroimaging derivatives are not included in this repository.  
The following files and directories are intentionally excluded:  
- raw BOLD and T1 MRI data
- NIfTI files
- DICOM files
- SPM output files
- rapidtide output files
- generated rsCVR maps
- masks and intermediate derivatives
- CSV, TSV, Excel, and result files
- figures and visualisation outputs
- log files
- local configuration files
- private data directories
  
This is to prevent accidental sharing of sensitive imaging data and unnecessary large output files.

## Environment
The analysis workflows were mainly developed on an Ubuntu server using:  
- Python
- Jupyter Notebook
- MATLAB Runtime
- SPM
- rapidtide
- nibabel
- nilearn
- numpy
- pandas
- scipy
- matplotlib
  
Package versions may differ depending on the analysis environment. For reproducibility, users should check the environment used for each notebook.

# Notes
This repository is primarily for internal research code management and rsCVR workflow development.
The codes are not intended to provide a fully reproducible public analysis package because the original MRI datasets and generated derivatives are not included.

# Author
J. Ahn  
Ph.D. Candidate in AI for Healthcare and Medicine, Radiological Technologist  
AI-WM Lab, Department of Biomedical Engineering, Kyung Hee University
