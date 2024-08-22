# HEK-Flare-Positions

## Overview

This repository contains code to accurately determine the positions of solar flares. While the Heliophysics Event Knowledgebase (HEK) provides flare position data, the helioprojective Cartesian (HPC) coordinates in HEK are often inaccurate. This project aims to correct these positions using data from the Atmospheric Imaging Assembly (AIA).

## Features

- Corrects inaccurate HPC coordinates from HEK
- Uses AIA 94 Å difference images to locate flares
- Implements a method similar to SolarMonitor for flare detection
- Provides accurate flare locations for nearly every detected flare

## How It Works

1. The code reads a dataframe containing HEK-defined start and peak times of flares.
2. It then finds the correct HPC values using the following method:
   - Generates difference images from AIA 94 Å data
   - Applies Gaussian blurring to these images
   - Identifies the brightest pixel, which corresponds to the flare location
3. The corrected HPC coordinates are added to the input dataframe

## Usage

1. Prepare a dataframe with HEK-defined start and peak times of the flares you're interested in.
2. Ensure the dataframe has empty columns for 'hpc_x' and 'hpc_y'.
3. Run the code to populate these columns with the corrected HPC values.

## Note on HPC Coordinate Generation

The exact method used by HEK to generate the original HPC coordinates is uncertain. This repository's approach provides a more accurate alternative by directly analyzing AIA imagery.

## Data Coverage

The current version of this project includes data up to 2022.

## Project Origin

This work is one of the results from the ESA-Leiden University LEAPS project, supervised by Dr. Andy To.
