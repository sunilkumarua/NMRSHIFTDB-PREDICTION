**Abstract**
This project focuses on developing a workflow for predicting nuclear magnetic resonance (NMR) chemical shifts using data derived from the NMRShiftDB database. The repository presents a sequential modeling pipeline implemented through Jupyter Notebooks, encompassing data analysis, curation, descriptor generation, mapping, model training, and performance evaluation. The goal is to establish a reproducible framework for chemical shift prediction through structured data processing and machine learning methodologies.

**Introduction**
NMR spectroscopy is a fundamental analytical technique used to determine the structure and electronic environment of molecules. Accurate prediction of NMR chemical shifts from molecular structure remains a valuable task in computational chemistry and cheminformatics. The NMRSHIFTDB-PREDICTION project addresses this challenge by creating a modular workflow that processes raw NMRShiftDB data into a machine learning ready format and applies predictive models to estimate NMR chemical shifts.
The repository implements each stage of the workflow as an independent Jupyter Notebook, allowing systematic exploration and refinement of each stage. Although the repository does not include explicit documentation of algorithmic details or performance metrics, its structure provides an organized basis for reproducible NMR prediction research.

**Objectives**
1.	To curate and preprocess NMR data derived from the NMRShiftDB database.
2.	To generate molecular descriptors relevant to NMR chemical shift prediction.
3.	To align and map data between chemical environments and numerical descriptors.
4.	To train and compare predictive models for estimating NMR chemical shifts.
5.	To evaluate workflow performance across different nuclei and descriptor sets.

**Materials and Methods**

**Data Source**
The dataset used originates from NMRShiftDB, a public repository of experimentally measured NMR chemical shifts and molecular structures. The data files referenced within the notebooks indicate that this dataset was used as the primary source for training and validation.

**Data Preprocessing and Curation**
The initial data exploration and curation were performed through two notebooks:
•	eda_raw_data_analysis.ipynb
•	phase1_data_curation.ipynb
These stages include examination of raw data integrity, removal of incomplete or inconsistent entries, and formatting into a structured tabular representation suitable for further analysis.

**Descriptor Generation**
The second stage, implemented in phase2_descriptor_generation.ipynb, focuses on creating numerical representations of molecular structures. The notebook likely extracts molecular descriptors such as atomic environments, topological indices, or physicochemical properties, although specific descriptor types are not explicitly defined in the repository.

**Mapping and Alignment**
The mapping and alignment process is documented in phase3_mapping_alignment.ipynb. This stage ensures proper correspondence between the chemical shift data and the generated descriptors, allowing the predictive models to associate each atomic environment with its experimental shift value.

**Model Training and Optimization**
Model development and optimization are carried out through several notebooks, including:
•	phase4_model_training.ipynb
•	phase4_model_train_FULL2.ipynb
•	phase4b_train_per_nucleus.ipynb
•	phase4c_model_optimization.ipynb
•	phase4d_Hydrogen_finetune.ipynb
•	phase4d_descriptor_refinement.ipynb
•	phase4e_RF_vs_XGB.ipynb
These notebooks cover model training, comparison across atomic types (e.g., hydrogen, carbon), hyperparameter optimization, descriptor refinement, and evaluation of different machine learning algorithms. The filenames suggest comparisons between Random Forest and XGBoost regressors, as well as specialized fine-tuning for hydrogen nuclei.

**Results and Discussion**
The repository does not include explicit performance results, visualizations, or summary metrics. However, the notebook structure implies that model performance was assessed through training and testing datasets, and optimization experiments were conducted to improve accuracy.
The progression of files demonstrates a coherent and modular approach to model development, aligning with best practices in cheminformatics research. The inclusion of dedicated notebooks for per-nucleus training and model comparison suggests systematic experimentation to identify optimal algorithms and feature sets for specific atomic environments.

**Conclusion**
The NMRSHIFTDB-PREDICTION project establishes a structured computational framework for predicting NMR chemical shifts using data from NMRShiftDB. Its modular notebook-based design enables transparent, reproducible processing of chemical data and model development.
Future work should include detailed reporting of model performance, feature importance analyses, and comparative evaluations with existing NMR prediction tools. (Still in devolopment and optimization)
