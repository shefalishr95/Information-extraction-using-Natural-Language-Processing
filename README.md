# What made you happy? An analysis of common actions linked to happy moments 
## Fall 2023
### This project was completed as a aprt of the Applied Data Science course @ Columbia University.



### [Project Description](doc/Proj1_desc.md)

> *"Happiness is not something ready-made. It comes from your own actions"* - Dalai Lama


There is no dearth of research on what is happiness and how can one achieve it. Several researchers have attempted to theorize of emperically identify how happy are people, what happy people do, theory behind happiness and factors related to joy - to name a few. This project aims to add to that research by using crowd-sourced collection of 100,000 happy moments ('HappyDB' database) to extract actions performed by individuals (self-reported) that made them happy in the past 24 hours or 3 months. 

The aim of the project is not to predict what actions lead to happiness - that causal inference requires more robust approaches, which is outside the scope of this project. The analyses done aims to extract 'action phrases', or strings of verbs that describe self-initiated activities or undertakings that are linked to their joyful moments. In simple words, this is a prelimniary analysis of things people do that make them happy. 


**Data:** The project uses open-source HappyDB data corpus (available on their [website](happydb/data)) for analysis. The 'doc' folder in this repository has Python scripts for analysis and visualization of data, while the 'data' folder has the processed data 'final_df.csv'). Description of HappyDB raw data can be found on the linked repository. 

**Method:** The data was analyzed using a popular NLP package 'spaCy'. The technique used was 'DependencyMatching', which parsed dependencies (from Universal Dependencies) is extracted using pre-defined patterns. The steps followed for analysis are as follows:

![image](figs/steps_for_analysis.png)

Detailed step-wise descriptions and code is available in the [Text_processing_and_info_extraction] (doc/Text_processing_and_info_extraction.ipynb) file. 

**Visualization:** As the pattern match is done for 'action phrases', the extracted outputs has more accurate and contextual description of actions performed by individuals. However, a drawback to this is restrictions of text visualizations. Most commonly used text-data visualizations utilize 'frequency' or value counts to present data. As action phrases are contextualized, their frequency distribution is sparse. 
With the above caveat in mind, the following visualizations were generated:
+ Word Clouds
+ Barplots for common actions


This project folder is organized as follows.

```
proj/
├── data   
│    ├── README.md
│    ├── final_df.csv
├── data/
├── doc/
├── figs/
└── output/
```

```
happydb
└── lib
    ├── cleaned_hm.csv
    ├── demographic.csv
    ├── original_hm.csv
    ├── senselabel.csv
    ├── topic_dict
    │   ├── entertainment-dict.csv
    │   ├── exercise-dict.csv
    │   ├── family-dict.csv
    │   ├── food-dict.csv
    │   ├── people-dict.csv
    │   ├── pets-dict.csv
    │   ├── school-dict.csv
    │   ├── shopping-dict.csv
    │   └── work-dict.csv
    └── vad.csv
```


Please see each subfolder for a README file.
