# Beyond diamond: Interpretable machine learning reveals design principles for quantum defect host materials
This repository contains all the data used or were generated as a part of the work, [Beyond diamond: Interpretable machine learning reveals design principles for quantum defect host materials](https://journals.aps.org/prmaterials/accepted/10.1103/bt3b-hp18).


> — Submitted to Phys Rev Materials, 2025

---

## Document Structure:
### File descriptions:
- [predictions.csv](./predictions.csv) - Predictions made by the models and the Ensemble model on the materials project
    data
- [ALE_ens.pkl](./ALE_ens.pkl) - Accumulated local effects of the Ensemble model
- [featurized_data.pkl](./featurized_data.pkl) - Data used in training and evaluating the models
- [models_PFI.pkl](./models_PFI.pkl) - Permutation feature importance of the base estimators
- [PFI_ens](PFI_ens) - Permutation feature importance of the Ensemble Model
- [ens_90](ens_90), [ens_95](ens_95) - Ensemble model predictions at 0.90 and 0.95 confidence
- [predictions.tex](./predictions.csv) - Predictions and their corresponding materials project
    database entries queried with conditions mentioned in the paper.
- [Isotopic_Nuclear_Spin_info_df.csv](./Isotopic_Nuclear_Spin_info_df.csv) - Nuclear spin
    information webscrapped from [easyspin's isotope table](https://easyspin.org/documentation/isotopetable.html)


Some files are stored in [pickle](https://docs.python.org/2/library/pickle.html) format to preserve the
data type. To access them use,
~~~
import pickle
path = './' # Path where the file is located
with open(path + 'filename', 'rb') as f:
    data = pickle.load(f)

~~~

Or with pandas

```
import pandas as pd

data = pd.read_pickle(path + 'filename')
```

Some files are stored in [pickle](https://docs.python.org/2/library/pickle.html) to preserve the
data type. To access them use,
