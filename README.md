# RS_Analyst_Technical_Assignments
Technical assignments for candidates of Natural State's Remote Sensing Analyst position.

Below are three technical assignments. Each one tests basic abilities related to core responsibilities of the position: carbon modeling, vegetation monitoring, and vegetation structural analyses. To complete the assignment, fork this repository. When complete, ensure your forked repository is publicly available and notify Matt Rogan either through email (mrogan@naturalstate.org). Contact him with any questions or issues.

The results of your analyses are secondary to more general questions of how you frame the problems, how effectively you use software tools, and how clearly you communicate your work. For that reason, do not choose complex, time-consuming methods. Straightforward methods that are well established in the scientific literature are appropriate for this work.

Submissions will still be considered even if not all assignments can be completed.

## Assignment 1: Predictive modeling of soil organic carbon

The folder *soc* contains a CSV file called *SOC_samples.csv* within the *data*. It contains estimates of soil organic carbon stocks from 80 sites in the rangelands north of Mount Kenya. Assume the samples were collected between March 1, 2023 and February 29, 2024. The spreadsheet has the following five columns:
- **plot_no**: String. A sample site identifier.
- **MgC_per_ha**: Numeric. Estimated tonnes of carbon (MgC) per hectare, centred to have a mean of 0.
- **MgC_SE**: Numeric. The standard error of the estimate. Estimates are derived from four soil cores, aggregated across three depth profiles.
- **longitude**: The longitude of the sample location in the WGS84 datum.
- **latitude**: The latitude of the sample location in the WGS84 datum.

Define a modeling domain around the sample locations and fit a predictive model of relative SOC stocks using software of your choosing. Evaluate the model's performance. You may use any predictive method but if you use a model with predictor variables, include no more than five. You will not be judged on model performance as we are not interested in the result. So if your model performs poorly, do not waste time trying to improve it but rather focus in the outputs on why you think it performs poorly and how it might be improved. Note that you may want to do this assignment in conjunction with #2 as there could be some redundancies. To complete the assignment, provide the following outputs:
- Reproducible code for training and evaluating your model. Carefully annotate your code. Any additional data needed to fit the model should be saved into the *soc/data* folder.
- A document that briefly describes your methods and interprets the results of your model evaluation. Make sure to explain why you chose your modeling method, how you defined the modeling domain, and how you measured model performance. Visually present any patterns of interest in the distribution of SOC stocks or in the model's bias. In particular, explain in 100-200 words whether you think your model would be useful for monitoring change in SOC as part of a carbon credit.
- A map (it may be embedded in the written document) that shows predicted SOC stocks across your modeling domain.

## Assignment 2: Monitoring vegetation patterns
Within the modeling domain used in Assignment 1, use freely available satellite remote sensing products tocompare the phenology and productivity of the herbaceous vegetation between the following two time periods: 1 March 2022 - 28 February 2023 and 1 March 2023 - 29 February 2024. The only restriction is that your analysis cannot rely solely on NDVI. We want to see more originality than that. Provide the following outputs in a folder called *vegetation_monitoring*:
- One or more reproducible scripts (preferably in notebooks such as in google colab or jupyter) for acquiring, processing and analysing the datasets. Carefully annotate your code.
- A document that briefly explains how you measured phenology and productivity and summarises your results. Include a map that shows changes between the two time periods.

## Assignment 3: Vegetation structural metrics
[This link](https://naturalstate3030-my.sharepoint.com/:u:/g/personal/mrogan_naturalstate_org/EYdf2YP_pZlOt4LVaQm2x6IBwFhVj-Ci5irJ-5rpmTMt6g?e=k6JY2J) will let you access a lidar point cloud (.las) for a small plot of land. Using the lidar data, choose 3-5 metrics that you think best describe the structure of the vegetation. Consider both vertical and horizontal heterogeneity. You may geographically subset the data for computational efficiency. Provide the following outputs in a folder called *structural_metrics*:
- a reproducible script for processing the lidar data and deriving the metrics you choose. Carefully annotate your code.
- A document that briefly summarises in a few hundred words the metrics you chose and the results of your analysis. Proivde links to any sources you used to choose your metrics. Include at least one map of horizontal structural heterogeneity/complexity and at least one map of vertical structure.


