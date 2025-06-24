# Project Title

Distance-Amplified Power-law Distributions Better
Characterize Human Long-Distance Travel

## Description

These are six scripts for the simulation and experiments in the this project.

The executing scripts are listed belows:
- **Modelling_Utils.ipynb**
  This script provides the tools (functions) used to derive:
  - The best-fitting amplified power-law process
  - The best-fitting dynamically truncated power-law
  - The optimal exponentially truncated power-law
   Additionally, the symmetric mean absolute percentage error (sMAPE) is calculated within this script.
   The parameters of the best-fitting models are saved in the **results** folder for future use.

- **Modelling and Visualization_MiD.ipynb**
  
  This script is primarily used for modeling long-distance travel in the MiD dataset. Its functionality is organized into four main sections:
  1. **Dataset reading**: This section reads, extracts, and preprocesses the empirical data from the Mobility in Germany (MiD) survey. More information about the [datasets](#datasets) can be found below.
  2. **Configurations for modelling**: Defines the combinations of parameters to be tested during the modeling process.
  3. **Model training and storage**: Simulates the models by generating a large number of sampled trip lengths (using functions from Modelling_Utils.ipynb) for different parameter combinations. The optimal set of parameters is identified by minimizing the sMAPE error between the empirical data and the simulated CCDFs.</n>
   The results are saved in the **results** folder with the following filenames:
      - **Our model**: Optimal results of LR Modelling in MiD17 with car.pkl
      - **Power-law [D]**: Optimal results of Power-law with dynamic truncation for LR Modelling in MiD17 with car.pkl
      - **Power-law [E]**: Optimal power-law with exponential truncation in MiD.pkl
  4. **Plotting**:
  Visualizes the comparison between the CCDFs of our distance-amplified power-law model (Our model), the optimal dynamically truncated power-law (Power-law [D]), the optimal exponentially truncated power-law (Power-law [E]) and the empirical data for the long-distance travel in MiD.

- **Modelling and Visualization_NHTS.ipynb**
  - This script functions similarly to **Modelling and Visualization_MiD.ipynb**, but processes data from the American National Household Travel Survey (NHTS).
  - The corresponding output files and plots are also saved in the **results** folder.

- **Modelling and Visualization_UK.ipynb**
  - This script functions similarly to **Modelling and Visualization_MiD.ipynb**, but processes data from the United Kingdom (UK).
  - The corresponding output files and plots are also saved in the **results** folder.

- **Fitting other Distributions.ipynb**

   - The script is an attempt to fit commonly used distributions (i.e.,'Beta','Exponential','Gamma','Log-norm') to the German MiD long-distance data.

- **Modelling Short Distance Trips.ipynb**
   - Caculate the power-law properties, plot the CCDF of it, show the power-law properties of different short and medium-distance transportation modes (i.e., MiD Walking, MiD Bicycling, NHTS Short Distance Public Transportation) in comparison to the empirical data. Check if power-law existed or not in these transportation modes.

## Getting Started

### Environment and Dependencies

* Python version 3.11.3.
* Jupyter notebook
* Libraries: Numpy, Pandas, Matplotlib, Scipy, Seaborn, Datetime, Random, Math, nbimporter

### Datasets

1. MiD 2017: MiD2017_Wege.csv 
   * Mobility in Germany survey (MiD) data which was conducted in the year 2017
2. Nhts 2017: trippub_2017NHTS.csv
   * The American National Household Travel survey (NHTS)data, it collects on travel behavior in the United States. This file contains data items collected for each trip taken by household members aged 5 and above on the household’s designated travel day, with one record for each trip made by each individual.
3. UK (MNO) 2022: UK_data.csv
   * Mobility data derived from the movements of individuals carrying celluar devices in the United Kingdom
   
* Note: the above datasets are used in the scripts. The NHTS 2017 data is publicly available at https://nhts.ornl.gov/downloads directly in .csv format (trippub.csv) . The MiD data needs to be requested via https://www.mobilitaet-in-deutschland.de/archive/index.html. The UK data: UK_data.csv is not public available.


### Executing program

* Download all scripts and relevant folders, open it in the Juypter notebook.
* Note: Feel free to try running the scripts by downloading the NHTS dataset from the link provided above. Please ensure the file paths in the script are updated to match your local environment.
* Note: Although the original raw dataset is not provided due to privacy concerns, the **results** folder contains all the pre-processed output files, which can be used to reproduce the part of the visualizations.

## Contact
Huiran Liu - huiran.liu@campus.tu-berlin.de <br>
Gregor Bankhamer - bankhamer@tu-berlin.de
