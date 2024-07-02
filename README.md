## AbstractParser
<div align="center">
  <img src="https://github.com/HassanKhalil321/PubmedAbstractParser/blob/main/assets/model_work.jpg" width="1000"/>
</div>


## Introduction
Welcome to PubMed Abstract Parser, a project focused on extracting and organizing information from PubMed abstracts using advanced natural language processing techniques. This tool aims to make biomedical literature more accessible and manageable for researchers and healthcare professionals, enhancing the efficiency of information retrieval and analysis
## Dataset

The **PubMed_200k_RCT_numbers_replaced_with_at_sign** dataset consists of 200,000 abstracts sourced from PubMed, where numerical values have been anonymized by replacing them with "@" symbols. This curated collection is tailored for natural language processing tasks within the biomedical field, facilitating research in text mining, information extraction, and the development of machine learning models.


## Model Overview

**Input Handling:**
After receiving a medical abstract as input, the model divides it into two components: the statements within the abstract and their corresponding line numbers. Each component is processed through separate pathways in the model.

**Statements Input Processing:**
- The statements are first passed through text vectorization and embedding layers.
- They are then processed through two 1D convolutional layers.
- Finally, the output is passed through a flattening layer for feature extraction.

**Statement Line Number Input:**
- The line numbers are processed through a dense layer to provide positional context.

**Concatenation and Final Output:**
- The outputs from both pathways (statements and line numbers) are concatenated.
- This concatenated output is processed to produce parsed text.
- The final output categorizes the text into sections such as background, methods, results, conclusion, or objectives.


## Loss
<div align="center">
  <img src="https://github.com/HassanKhalil321/PubmedAbstractParser/blob/main/assets/CCE.jpg" alt="Gesture Recognition" width="600"/>
</div>
