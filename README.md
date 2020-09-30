# Volume guarantee ventilation during neonatal transport in infants with hypoxic ischaemic encephalopathy


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

Python version: 3.7.4, IPython version: 7.10.2, pandas version: 0.25.3, matplotlib version: 3.1.1, NumPy version: 1.17.4, SciPy version: 1.3.1

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


### 2. Processing of clinical data


[clinical_data_1_665](clinical_data_1_665.ipynb)

- Total: **665 cases**
- Clinical data available in **539 cases**
- Only keep clinical data for cases where ventilation recordings (>15 minutes) are also available: **511 cases**

DataFrame containing the processed clinical data exported as **clin_df_1_665.pickle** 

This Notebook also generates and exports disease-specific Excel sheets: **clinical_data_diseases_1_665.xlsx**
It also exports pickle archives:
**clin_df_RDS, clin_df_MAS, clin_df_PPHN**,
**clin_df_cardiac** (except PFO and PDA), 
**clin_df_HIE**,
**clin_df_CDH, clin_df_NEC, clin_df_surgical** (except NEC and CDH)


### 3. Processing of blood gases

[blood gases_1_665](blood_gases_1_665.ipynb)

- Total: **665 cases**
- Clinical and appropriate ventilator data are available only for **511 cases**
- Blood cases not available in 28 cases; **483 cases remaining**

Dictionary containing the processed blood gas data exported as pickle archive: **blood_gases_1_665.pickle**


### 4. Further processing of slow (0.5Hz) ventilator data


[ventilator_data_processing_1_300](ventilator_data_processing_1_300.ipynb)

Imported: **data_pars_1_150.pickle**, **data_pars_151_300.pickle**, **clin_df_1_300.pickle**

- Total: **246 cases** with ventilator data available (with >15 minutes recording time)
- Clinical data were not available for **4 cases** 
- Appropriate ventilator and clinical data are available for **242 cases**

Exported: dictionaries containing ventilation data as **data_pars_measurements_1_300.pickle,  data_pars_settings_1_300.pickle, data_pars_alarms_1_300.pickle**


[ventilator_data_processing_301_600](ventilator_data_processing_301_600.ipynb)

Imported: **data_pars_301_450.pickle**, **data_pars_451_600.pickle**, **clin_df_301_600.pickle**

- Total: **255 cases** with ventilator data available (with >15 minutes recording time)
- Clinical data were not available for **38 cases** 
- Appropriate ventilator and clinical data are available for **217 cases**

Exported: dictionaries containing ventilation data as **data_pars_measurements_301_600.pickle,  data_pars_settings_301_600.pickle, data_pars_alarms_301_600.pickle**


[ventilator_data_processing_601_665](ventilator_data_processing_601_665.ipynb)

Imported: **data_pars_601_674.pickle**, **clin_df_1_665.pickle**

- Total: **67 cases** with ventilator data available (with >15 minutes recording time)
- Clinical data were not available for **15 cases** 
- Appropriate ventilator and clinical data are available for **52 cases**

Exported: dictionaries containing ventilation data as **data_pars_measurements_601_665.pickle,  data_pars_settings_601_665.pickle, data_pars_alarms_601_665.pickle**


### 5. Further processing of recordings with mechanical ventilation


[ventilator_data_processing_1_300_ventilated](ventilator_data_processing_1_300_ventilated.ipynb)

This notebook ventilator data to keep only periods of mechanical ventilation. Recordings have also been inspected and trimmed _manually_ to remove periods when the ventilator was working but the patient was not connected.

Imported: **data_pars_measurements_1_300.pickle,  data_pars_settings_1_300.pickle, data_pars_alarms_1_300.pickle**, **clin_df_1_300.pickle**

- Total: **242 cases**
- Containing >15 minutes of mechanical ventilation: **146 cases remaining**
- After removing periods when the patient was not connected, containing >15 minutes of mechanical ventilation: **145 cases**

Exported: 
**data_pars_measurements_ventilated_1_300.pickle,  data_pars_settings_ventilated_1_300.pickle, data_pars_alarms_ventilated_1_300.pickle, 
vent_modes_1_300.pickle, vent_modes_ventilated_1_300.pickle, 
ventilation_modes_1_300.xlxs, ventilation_modes_ventilated_1_300.xlsx**


[ventilator_data_processing_301_600_ventilated](ventilator_data_processing_301_600_ventilated.ipynb)

This notebook ventilator data to keep only periods of mechanical ventilation. Recordings have also been inspected and trimmed _manually_ to remove periods when the ventilator was working but the patient was not connected.

Imported: **data_pars_measurements_301_600.pickle,  data_pars_settings_301_600.pickle, data_pars_alarms_301_600.pickle**, **clin_df_301_600_pickle**

- Total: **217 cases**
- Containing >15 minutes of mechanical ventilation: **114 cases**
- **8 cases** removed as there was no flow sensor used (and hence no tidal volume measurement), **106 cases remaining**
- After removing periods when the patient was not connected, containing >15 minutes of mechanical ventilation: **106 cases**

Exported: **data_pars_measurements_ventilated_301_600.pickle,  data_pars_settings_ventilated_301_600.pickle, data_pars_alarms_ventilated_301_600.pickle, vent_modes_301_600.pickle, vent_modes_ventilated_301_600.pickle, 
ventilation_modes_301_600.xlxs, ventilation_modes_ventilated_301_600.xlsx**


[ventilator_data_processing_601_665_ventilated](ventilator_data_processing_601_665_ventilated.ipynb)

This notebook ventilator data to keep only periods of mechanical ventilation. Recordings have also been inspected and trimmed _manually_ to remove periods when the ventilator was working but the patient was not connected.

Imported: **data_pars_measurements_601_665.pickle,  data_pars_settings_601_665.pickle, data_pars_alarms_601_665.pickle**, **clin_df_1_665_pickle**

- Total: **52 cases**
- Containing >15 minutes of mechanical ventilation: **22 cases**
- **1 case** removed as there was no flow sensor used (and hence no tidal volume measurement), **21 cases remaining**
- After removing periods when the patient was not connected, containing >15 minutes of mechanical ventilation: **21 cases**

Exported: **data_pars_measurements_ventilated_601_665.pickle,  data_pars_settings_ventilated_601_665.pickle, data_pars_alarms_ventilated_601_665.pickle, vent_modes_601_665.pickle, vent_modes_ventilated_601_665.pickle, 
ventilation_modes_601_665.xlxs, ventilation_modes_ventilated_601_665.xlsx**


### 6. Analysis of recordings containing mechanical ventilation


[analysis_ventilated_1_300](analysis_ventilated_1_300.ipynb)

Explorative data analysis of **145 ventilated cases** among recordings `AL000001 - AL000300`. 

- It calculates statistics on clinical details of ventilated cases and exports them as Excel files and as graphs. 
- It identifies ventilator modes, recordings with multiple ventilation modes and in those, the dominant ventilator mode; exports Excel files and graphs of these. 
- It calculates descriptive statistics on various ventilator parameters in the individual recordings and writes them to Excel files in different format (grouping).
- It produces time series graphs on various ventilator parameters and exports them.

Imported: **data_pars_measurements_ventilated_1_300.pickle,  data_pars_settings_ventilated_1_300.pickle, data_pars_alarms_ventilated_1_300.pickle, vent_modes_ventilated_1_300.pickle, clin_df_pickle_1_300.pickle**

Exported: 

- Excel files and graphs about clinical data and ventilator modes are exported to **/Users/guszti/ventilation_fabian/Analyses/analysis_ventilated_1_300** folder
- Time series graphs on ventilator parameters are exported to the **/Volumes/GUSZTI/data_dump/fabian/fabian_cases** folder into individual subfolders named after the recording
- **vent_modes_ventilated_1_300_plus.pickle** (additional data about multiple ventilator modes and dominant modes in in the DataFrame


[analysis_ventilated_301_600](analysis_ventilated_301_600.ipynb)

Explorative data analysis of **106 ventilated cases** among recordings `AL000301 - AL000600`

- It calculates statistics on clinical details of ventilated cases and exports them as Excel files and as graphs. 
- It identifies ventilator modes, recordings with multiple ventilation modes and in those, the dominant ventilator mode; exports Excel files and graphs of these. 
- It calculates descriptive statistics on various ventilator parameters in the individual recordings and writes them to Excel files in different format (grouping).
- It produces time series graphs on various ventilator parameters and exports them.

Imported: **data_pars_measurements_ventilated_301_600.pickle,  data_pars_settings_ventilated_301_600.pickle, data_pars_alarms_ventilated_301_600.pickle, vent_modes_ventilated_301_600.pickle, clin_df_pickle_301_600.pickle**

Exported: 

- Excel files and graphs about clinical data and ventilator modes are exported to **/Users/guszti/ventilation_fabian/Analyses/analysis_ventilated_301_600** folder
- Time series graphs on ventilator parameters are exported to the **/Volumes/GUSZTI/data_dump/fabian/fabian_cases** folder into individual subfolders named after the recording
- **vent_modes_ventilated_301_600_plus.pickle** (additional data about multiple ventilator modes and dominant modes in in the DataFrame


[analysis_ventilated_601_665](analysis_ventilated_601_665.ipynb)


Some explorative data analysis of **21 ventilated cases** among recordings `AL000601 - AL000665`

- It calculates statistics on clinical details of ventilated cases and exports them as Excel files and as graphs. 
- It identifies ventilator modes, recordings with multiple ventilation modes and in those, the dominant ventilator mode; exports Excel files and graphs of these. 

Imported: **data_pars_measurements_ventilated_601_665.pickle,  data_pars_settings_ventilated_601_665.pickle, data_pars_alarms_ventilated_601_665.pickle, vent_modes_ventilated_601_665.pickle, clin_df_pickle_601_665.pickle**

Exported: 

- Tables and graphs about clinical data and ventilator modes 
- **vent_modes_ventilated_601_665_plus.pickle** (additional data about multiple ventilator modes and dominant modes in the DataFrame).


### 7. Analysis of recordings from babies with hypoxic ischaemic encephalopathy (HIE)

1. [transport_HIE_for_paper](transport_HIE_for_paper.ipynb): Analysis of infants ventilated with HIE and undergoing therapeutic hypothermia in the first 24 hours life. Comparison of SIMV and SIMV-VG ventilation. 

Imported: 
**data_pars_measurements_ventilated_1_300.pickle,  data_pars_settings_ventilated_1_300.pickle, data_pars_alarms_ventilated_1_300.pickle, vent_modes_ventilated_1_300.pickle,
data_pars_measurements_ventilated_301_600.pickle,  data_pars_settings_ventilated_301_600.pickle, data_pars_alarms_ventilated_301_600.pickle, vent_modes_ventilated_301_600.pickle, 
data_pars_measurements_ventilated_601_900.pickle,  data_pars_settings_ventilated_601_900.pickle, data_pars_alarms_ventilated_601_900.pickle, vent_modes_ventilated_601_900.pickle, 
clin_df_pickle_601_665.pickle**

Exported: Tables and graphs as reported in the paper
