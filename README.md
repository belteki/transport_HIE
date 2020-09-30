# transport_HIE

This repository contains the Python code used for data processing,
analysis and visualization described in the following paper:

Lantos, L., Berenyi, A., Morley, C., Somogyvari Zs., Belteki G. **Volume guarantee ventilation in neonates treated with hypothermia for hypoxic-ischemic encephalopathy during interhospital transport.** *J Perinatol (2020). ( https://doi.org/10.1038/s41372-020-00823-8)*

Contact: gusztav.belteki@addenbrookes.nhs.uk; gbelteki@aol.com

____


The outputs (numbers, tables, graphs) of the cells of the Jupyter Notebooks
(.ipynb files) have been suppressed in order to comply with copyrights.
Some of the corresponding data and graphs can be found in the paper and its
only supplementary material.

This code can be viewed in any web browser. If the code is displayed (rendered)
 in Github, copy and paste the URL (web adress) of the Notebook into **nbviewer**
(https://nbviewer.jupyter.org) for a read-only display.

To run the code, you need to use Jupyter.
The raw ventilator data are not shared but the user can run this code on his or
her own data obtained in the same format.

____


Packages required to run this Notebook:

Python version: 3.7.4

IPython version: 7.10.2

pandas version: 0.25.3

matplotlib version: 3.1.1

NumPy version: 1.17.4

SciPy version: 1.3.1

I recommend downloading these packages using the freely availably Anaconda
built: https://www.continuum.io/downloads

# Jupyter Notebooks

### 1. Initial processing of raw ventilator slow (0.5 Hz) data

[ventilator_data_1_150](ventilator_data_1_150.ipynb): This notebook imports all ventilator data of these recordings (including ventilator parameters, settings, alarms (0.5Hz sampling rate) and waveform data (150Hz sampling rate).

- Total: **150 cases**
- 21 cases were removed as they were less than 15 minutes long (empty or partial recordings) 
- **129 cases** remaining

Dictionary containing the processed ventilation data exported as pickle archive: **data_pars_1_150.pickle** 


[ventilator_data_151_300](ventilator_data_151_300.ipynb): This notebook imports all ventilator data of these recordings (including ventilator parameters, settings, alarms (0.5Hz sampling rate) and waveform data (150Hz sampling rate).

- Total: **150 cases**
- 1 case (AL000257) was removed it was fragmented with multiple in data
- 32 cases were removed as they were less than 15 minutes long (empty or partial recordings) 
- **117 cases** remaining

Dictionary containing the processed ventilation data exported as pickle archive: **data_pars_151_300.pickle** 


[ventilator_data_301_450](ventilator_data_301_450.ipynb): This notebook imports all ventilator data of these recordings (including ventilator parameters, settings, alarms (0.5Hz sampling rate) and waveform data (150Hz sampling rate).

- Total: **150 cases**
-  19 cases were removed as they were less than 15 minutes long (empty or partial recordings) 
- **131 cases** remaining

Dictionary containing the processed ventilation data exported as pickle archive: **data_pars_300_450.pickle**


[ventilator_data_451_600](ventilator_data_451_600.ipynb): This notebook imports all ventilator data of these recordings (including ventilator parameters, settings, alarms (0.5Hz sampling rate) and waveform data (150Hz sampling rate).

- Total: **150 cases**
-  26 cases were removed as they were less than 15 minutes long (empty or partial recordings) 
- **124 cases** remaining

Dictionary containing the processed ventilation data exported as pickle archive: **data_pars_451_600.pickle**


[ventilator_data_601_674](ventilator_data_601_674.ipynb): This notebook imports all ventilator data of these recordings (including ventilator parameters, settings, alarms (0.5Hz sampling rate) and waveform data (150Hz sampling rate).

- Total: **74 cases**
-  7 cases were removed as they were less than 15 minutes long (empty or partial recordings) 
- **67 cases** remaining

Dictionary containing the processed ventilation data exported as pickle archive: **data_pars_601_674.pickle**


##### From AL000001-AL000674: Appropriate ventilator data are available for a total of: **129 + 117 + 131 + 124 + 67 = 568 cases**
