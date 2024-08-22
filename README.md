# Automated-Data-Quality-Control-STATA
This is a real use case of automating the process of quality control any micro economic data to ensure that the data possessing pipeline has not altered the raw data in any unfavorable manner. This shall ensure data integrity and reliability. The scripts is capable to examine and test for multiple individual datasets concurrently, and will run the checks and outputs a standard formatted QA report in an .xlsx format.

#### [Note] This procedure is currently in-use by the World Bank’s Global Education Unite (the Global Education Policy Dashboard team).

### What does the procedure exactly include?
The procedure runs checks to report on the following:
- Changes to # of unique count of observations for each dataset; between raw and processed data
- Changes to # of duplicates between raw and processed data
- Changes to # of observations with a missing unique ID between raw and processed data
- Changes to # of features/variables between raw and processed data

### Pre-requisites for error-free implementation 
To ensure that the script will run with no error, please ensure the following:
- Redefine file paths and data directories (at the top of the script) according to your machine and workflow.
- Redefine the macros (globals/locals) (at the top of the script) according to your data files names and id variables
- This script uses the "frames" functionality, which was introduced in STATA 16 (Stata-16 or higher is recommended).
