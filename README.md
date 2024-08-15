# HEK-Flare-Positions

Even though the HEK contains flare position data, these hpc coordinates are inaccurate. This code finds the correct positions, using data from AIA. 
To use it, read in a dataframe with the HEK defined start and peak times of the flares you want positions for, with empty rows for 'hpc_x' and hpc_y'. The code will then find the correct hpc values and add them to the dataframe.
