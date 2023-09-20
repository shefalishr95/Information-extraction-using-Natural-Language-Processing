# Data folder

The data directory contains the analyzed data. This output is obtained after execution of [Text_processing_and_info_extraction](doc/Text_processing_and_info_extraction.ipynb) file. The data contains extracted 'action phrases', their unique identifier and other relevant characteristics (such as demographic data,reflection period etc.). The variables are:

- **hmid (int)**: Happy moment ID
- **Root_Object_Phrase or action_phrase (str)**: The action performed by an individual (phrases); extracted from the text using dependency matching.
- **Sentence (str)**: Setences from responses (single hmid may have multiple sentences).
- **cleaned_hm (str)**: Cleaned happy moment
- **Starts with I or Verb (str)**: Binary variable depicting whether the sentence linked to the action phrase starts with 'I' or a verb (to identify moments which were user-led i.e., "I ran" or "Got a job").
- **wid (int)**: Worker ID
- **reflection_period (str)**: Reflection period used in the instructions provided to the worker (3m or 24h)
- **predicted_category (str)**: Happiness category label predicted by our classifier (check [paper](https://arxiv.org/pdf/1801.07746.pdf) for reference)
- **age (float)**: Age
- **country (str)**: Country of residence (follows the ISO 3166 Country Code)
- **gender (str)**: {Male (m), Female (f), Other (o)}
- **marital (str)**: Marital status {single, married, divorced, separated, or widowed}
- **parenthood (str)**: Parenthood status {yes (y) or no (n)}

While all demographic categories were not utilized for visualizations in this project, they are present in the data for future analyses.