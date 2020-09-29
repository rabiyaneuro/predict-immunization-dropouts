 Predicting Immunization Drop-outs
==============================

#### Walkthrough: [/reports](main/RabiyaNoori-PredictDropouts.ipynb)

Summary:
Although vaccination rates have increased globally over the last twenty years - largely due to efforts to ensure vaccines are stocked at convenient points of care even in remote locations - they have plateaued in the last decade. This is largely attributable to children who drop out of their vaccination schedule, i.e. do not receive all of their required vaccines, despite access. In this project, I used data on patient profiles and vaccination histories to train a model that will predict patients at-risk of dropping out of their vaccination schedules. This model is useful in determining which patients will need early intervention to ensure they receive all their vaccinations. This project involved cleaning messy and limited tabular data and feature engineering. The final model trained was a random forests model and the accuracy achieved was XX%.

==============================

#### Problem Context:
Although vaccination rates have increased globally over the last twenty years - largely due to efforts to ensure vaccines are stocked at convenient points of care even in remote locations - they have plateaued in the last decade. This is largely attributable to children who drop out of their vaccination schedule, i.e. do not receive all of their required vaccines,despiteaccess. In addition, delayed vaccination also puts many children at risk and often requires costly vaccination campaigns to resolve.

#### Problem Statement: 
Imagine you are working with an organization that runs health clinics in Botswana. They want to be able to send health workers to follow-up with children who have not yet received all 4 doses of OPV and 3 doses of DPT at 4 months of life. They cannot individually follow-up with all children, so your job is to help them target their intervention by predicting which children will not become vaccinated by 6 months without intervention. Therefore, you can use all information, for example which vaccines the child has received, up until 4 months after the child is born. Below are some examples of scenarios when health care workers would and would not intervene:

- Child A has received 4 doses of OPV and 3 doses of the DPT vaccine by 4 months of life. Because this child already received all their vaccinations, the health care worker would not intervene.
- Child B received 2 doses of OPV and 1 dose of DPT by 4 months of life. At 5.5 months, Child B received 1 more dose of OPV and 1 more dose of DPT, and then no more vaccinations until 8 months. Because the child was still undervaccinated at 6 months, the model should tell the health care worker would intervene at 4 months.
- Child C received 3 doses of OPV and 2 doses of DPT by 4 months of life, and then no further vaccinations. As the child never completed their vaccinations, a health care worker would intervene.

Data Dictionary: patients_db.csv

- pat_id: The unique ID of the child.
- dob: The date of birth of the child.
- gender: The gender of the child.
- fac_id: The unique ID of the health facility the child received the vaccination.
- lat: The latitude of the facility.
- long: The longitude of the facility.
- district: The geographical district that the facility is located in.

Data Dictionary: immunizations_db.csv

- pat_id: The ID of the child.
- vaccine: The abbreviated name of the vaccine the child attempted to receive.
- im_date: Immunization date, i.e. the date the child received the vaccine.
- successful: Whether or not the vaccination was successful.
- reason_unsuccesful: If the vaccination was unsuccessful, the selected reason why.


Below is also the WHO infant immunization schedule for your reference:

OPV (oral polio vaccine):
- Dose 1: birth
- Dose 2: 6 weeks
- Dose 3: 10 weeks,
- Dose 4: 14 weeks*

DTP (diphtheria, tetanus, pertussis):
- Dose 1: 6 weeks
- Dose 2: 10 weeks
- Dose 3: 14 weeks*

\* Although the final doses of these vaccines are supposed to occur just after 3 months, health care workers often allow a grace period of a few weeks to allow children who were slightly off schedule to catch up before followingup with children who are still unvaccinated. Therefore, we chose to use 4 months instead of 14 weeks as the initial cut-off.













<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

<p><small>Workflow was also inspired by Chip Huyen's book <a target="_blank" href="https://github.com/chiphuyen/machine-learning-systems-design"> Machine Learning Systems Design </a> </small></p>
