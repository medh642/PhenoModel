# PhenoModel
## A Comparative Analysis of Process-Based and Machine Learning Phenological Models for Red Maple(Acer rubrum), North United States
We are attempting to use the springtime package to perform machine learning and process-based modeling to understand climate change by observing changes in phenology. We use springtime data to focus on the phenological study of Red Maple (Acer rubrum). This is a replication of the paper ,Harmonizing Machine Learning Based Phenological Modeling: A Unified Workflow for Comparative Analyses <sup>[1]</sup>  The states that are focused on are New York (NY), Illinois(IL), and Minnesota (MN).The project also uses documentation from [springtime](https://springtime.readthedocs.io/en/latest/installation/)

### Objective 
The objective of this project is to understand and predict the phenological events of Red Maple trees in relation to environmental conditions.

### Data Sources
*Daymet:* A gridded dataset providing daily weather data for temperature, precipitation, and other climate variables.
*National Phenology Network (NPN):* Provides observational data for plant and animal phenology, which is used for understanding the timing of phenological events.

### Repository Structure
The repository contains the following directories and files:

scripts/: Python scripts for data preprocessing, cleaning, and analysis. 

### Installation
To get started with this project, clone the repository and install the necessary dependencies.  

*Prerequisites*  

Make sure you have Python 3.10.0 installed on your system

In R:  

- Rscript -e "install.packages('devtools', repos = 'https://cloud.r-project.org')"  

- Rscript -e "devtools::install_github('bluegreen-labs/phenor', upgrade = 'never')"  

- Rscript -e "devtools::install_github('ropensci/rppo', upgrade = 'never')"  

- Rscript -e "install.packages(c('daymetr', 'MODISTools', 'phenocamr', 'rnpn'), repos = 'https://cloud.r-project.org')"

In Python:  

- pip install Springtime  

- pip install rnpn

## Additional installation requirements for Windows users
Replace the "utils.py" within the springtime package to [here](https://github.com/medh642/PhenoModel/blob/main/utils.py) and adjust the path within the run_r_script function
r_binary_path = r" "  # Update to your R path</br>
r_library_path = r" " # Locate to win-library
Run on local R env
To get binary path:
r_home <- R.home()
r_bin_path <- file.path(r_home, "bin", "R")
print(r_bin_path)

To get the library path: 
system.file(package="springtime")


## Key Features

- Integration of **Daymet** climate data and **NPN** phenology observations.
- Automated data preprocessing and cleaning scripts.
- Statistical modeling of phenological events based on climate variables.


### Acknowledgments
Daymet and NPN for providing the climate and phenological data.
 

### License
This project is licensed under the Apache License, Version 2.0 – see the LICENSE file for details.  

### Future Recommendations  




### References  
1. Khodadadzadeh, M., Kalverla, P., & Zurita-Milla, R. (2024). Harmonizing Machine Learning Based Phenological Modeling: A Unified Workflow for Comparative Analyses. IGARSS 2024 - 2024 IEEE International Geoscience and Remote Sensing Symposium, 5333–5336.[DOI:10.1109/Phenology 2024]( https://doi.org/10.1109/IGARSS53475.2024.10641356)

