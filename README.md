## DOI

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19452984.svg)](https://doi.org/10.5281/zenodo.19452984)

## Overview

This repository contains the experimental dataset used in the paper:

“Data-driven surrogate material model for the mechanical simulation of additively manufactured architected weaves”

The dataset provides full-field deformation data, reconstructed truss models, and force response measurements for additively manufactured textile samples under tensile loading.

## Dataset Structure

The repository is organized into two main folders:

```
/Training
/Validation
```

Each folder contains MATLAB .m files representing individual samples:
- Training samples: T01 – T24
- Validation samples: V01 – V12
  
## File Format

Each .m file contains a MATLAB struct with the following fields:

**p - Point Data**
- `p.measured`: Cell array containing DIC grid points for each recorded image
- `p.reconstructed`: Cell array containing reconstructed textile node positions (truss representation)

**b - Connectivity**
- `b.main`: Connectivity of truss members along yarn (main members)
- `b.shear`: Connectivity of diagonal truss members (shear members)

**t - Time**
- Time stamps corresponding to each recorded frame

**load**
- Measured reaction force for each time step

**ext**
- Measured extension for each time step

**name**
- Sample identifier (e.g., "T01", "V05")

## Experimental Description

The dataset contains tensile test results of additively manufactured biaxial weaves with varying:
- Yarn diameter
- Yarn spacing
- Weave pattern
- Yarn orientation (aligned and bias)
Each sample is represented as a sequence of deformation states.
  
## Citation
If you use this dataset, please cite:
- Wirth, M., Shea, K., *Data-driven surrogate material model for the mechanical simulation of additively manufactured architected weaves*. (2026).

## License

This dataset is licensed under CC BY 4.0.

The associated publication may be subject to a different license.
