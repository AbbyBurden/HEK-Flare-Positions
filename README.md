# HEK Flare Positions using AIA

## Overview

This repository provides accurate solar flare position data, correcting and supplementing the information available in the Heliophysics Event Knowledgebase (HEK). While HEK offers flare position data, its helioprojective Cartesian (HPC) coordinates are often missing or inaccurate. Our project addresses this issue using data from the Atmospheric Imaging Assembly (AIA).

## Key Features

- **Pre-generated Dataframe**: The main product of this project is a comprehensive dataframe containing accurate flare positions.
- Corrected HPC coordinates for flares listed in HEK
- Flare locations determined using AIA 94 Å difference images
- Methodology similar to SolarMonitor for consistent flare detection

## Dataframe Contents

The dataframe includes:
- HEK-defined start and peak times of flares
- Corrected HPC coordinates ('hpc_x' and 'hpc_y')

## Methodology

Our approach to generating accurate flare positions:
1. Start with HEK-defined flare times
2. Generate difference images from AIA 94 Å data
3. Apply Gaussian blurring to these images
4. Identify the brightest pixel as the flare location
5. Calculate and record the corrected HPC coordinates

## Usage

Researchers can directly use the pre-generated dataframe for their studies. The dataframe is available.

For those interested in the underlying process:
1. The code used to generate this dataframe is included in this repository.
2. It can be run on a dataframe with HEK-defined start and peak times to populate 'hpc_x' and 'hpc_y' columns.

## Data Coverage

The current version of this dataset includes flare positions up to 2022.

## Note on HPC Coordinate Generation

The exact method used by HEK to generate the original HPC coordinates is uncertain. Our approach provides a more accurate alternative by directly analyzing AIA imagery.

## Project Origin

This work is one of the results from the 2024 ESA-Leiden University LEAPS project, supervised by Dr. Andy To.

## Citation

If you use this data in your research, please cite this repository

## Contact

For queries regarding this dataset or methodology, please contact andysh.to@esa.int.
