<p align="center"> # Hi, I'm Jethro and this is my portfolio. 
![My Image](fermilabDAS.png)
# Descriptions and links to relevant projects </p>

## Migration of CERN CMS's Beyond Standard Model - 3rd Generation experimental group data analysis framework
**Framework description:** The BSM-3G Analyzer is the main data analysis framework used by the Beyond Standard Model - 3rd Generation group at CERN's Compact Muon Solenoid (CMS) experiment. This group focuses on newly theorized particle and dark matter searches and is responsible for over 20 publications in top peer-reviewed physics journals. This analysis framework has multi-tiered functionality -- mining from a database where 100,000 particle collisions are registered per second, cleaning and filtering good events according to collaboration standards, and analyzing/plotting said data. 
The framework is primarily written in C++, with heavy use of the [ROOT](https://root.cern/) library.
**My role:** Every so often, the CMS collaboration updates their data structures to refelct latest hardware-level calibrations, implement more efficient storage, or generate collections for special use cases. My job was to migrate our analysis framework to handle the "Ultralegacy" tree-structure update, which was a collaboration-wide requirement for any future, publishable analysis. My work on this project in a nutshell:

- Adapting functionality to handle new raw data format
- Updating data filters and corrections/weights
- Implementing updated ML-based algorithms for particle reconstruction and identification 
- Functional testing of updated framework

**Link to framework:** [BSM-3G Ultralegacy Analyzer](https://github.com/BSM3G/NanoAOD_Analyzer_UL) (note: most relevant code in `\src` dir.)

## Update to parallelization, cluster submission, and data intergration framework
**Program description:** Due to the large quantity of particle collision information to be stored, the data is seperated into many ROOT-formatted files each containing ~10 million events. The data analyzer framework described above runs on one file at a time and produces a ROOT file as output. This workflow requires running hundreds of files for a given collection of relevant data. We automate the parallelization, submission to a computing cluster, and integration of outputed data via a Python program and the open-source [HTCondor](https://htcondor.org/) software suite. The migration to the Ultralegacy data format required a corresponding update to this parallelization/submission/intergration framework. My work on this project in a nutshell:

- Updating back end functionality for updated config. file format and user end usage
- Evaluating/Adjusting grid requirements for job submission
- Enhancing error handling and resubmission upon run failures

** Links: [submission framework](https://github.com/BSM3G/NanoAOD_Submission), [ROOT file combining program](https://github.com/BSM3G/NanoAOD_Analyzer_UL/blob/master/add_root_files_2016.py]




