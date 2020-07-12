 Predicting Immunization Drop-outs
==============================

#### Walkthrough: [/reports](main)


Although vaccination rates have increased globally over the last twenty years - largely due to efforts to ensure vaccines are stocked at convenient points of care even in remote locations - they have plateaued in the last decade. This is largely attributable to children who drop out of their vaccination schedule, i.e. do not receive all of their required vaccines, despite access. In this project, I used data on patient profiles and vaccination histories to train a model that will predict patients at-risk of dropping out of their vaccination schedules. This model is useful in determining which patients will need early intervention to ensure they receive all their vaccinations. This project involved cleaning messy and limited tabular data and feature engineering. The final model trained was a random forests model and the accuracy achieved was XX%.

Project Organization
------------

    ├── README.md                   <- Description of project and context, overview of project and workflow.
    ├── /main                       <- Scripts/notebooks to clean and explore data.
    │   ├── /processed_data         <- The final, and intermediate data sets for modeling.
    │   └── /raw_data               <- The original, immutable data dump.
    │   └── /figures                <- Scripts for generated graphics and figures to be used in reporting.
    │   └── make_dataset.py         <- Script to clean data.
    │   └── RabiyaN-predict-immunization-dropouts.ipynb     <- Summary report.
    │
    │
    ├── references         <- Take-home challenge explanatory materials given.
    │
    |__ requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
                              generated with `pip freeze > requirements.txt`

Note: Jupyter notebooks naming convention is a number (for ordering), and a short `-` delimited description, e.g. `1.0-initial-data-exploration`.

--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

<p><small>Workflow was also inspired by Chip Huyen's book <a target="_blank" href="https://github.com/chiphuyen/machine-learning-systems-design"> Machine Learning Systems Design </a> </small></p>
