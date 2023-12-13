# Setting up a MAGNET Digital Twin Container

This repository contains all the files needed to create a DeepLynx container with data relevant to the MAGNET digital twin. Please follow the instructions below.

## Instructions

1. Ensure DeepLynx is up and running. 
2. Login to the DeepLynx Web App and select `Create New Container`.
3. Provide a name and description. (Example: 'Demo Container' and 'This is a demo container with the MAGNET digital twin data')
4. Select the `diamond.owl` file from this repository (in the `Experiment` folder) for the `.owl File`. Leave the other `URL to .owl` file field blank and Ontology Versioning unchecked. The `Standard` and `Timeseries` data source types should be enabled.
5. Click `Save`.
6. Select the `Container Administration` menu and `Import Container`.
7. Select the checkboxes for `Data Sources` and `Type Mappings and Transformations`. Then in the `Container export (.json) file` selection, choose the `Demo Container Export.json` file from this repository.
8. Click `Import From File`. You should see a message after the process is complete indicating a successful container import.
9. Select the `Data Management` menu and `Type Mappings`.
10. Choose the `Graph Source` data source from the drop down.
11. Select the `Enabled` checkbox for the type mapping that was imported. You can see what Classes and Relationships will be created from this type mapping. More details can be seen by selecting the edit (pencil) icon under actions and selecting the view (eye) icon for the transformations listed.
12. Select the `Data Sources` page under the `Data Management` menu.
13. Click the slider for `Graph Source` to activate it. Select the `Timeseries` header and do the same for both timeseries data sources. Note that you can see the configuration for the timeseries data sources by selecting the edit (pencil) icon, or view any data by selecting the view (eye) icon. There should not be any data to view yet.
14. Select the `Import Data` page under the `Data Management` menu.
15. Under the `Data Sources` tab, select `Graph Source` in the drop down menu and then click `Import Data`. Select the `graph_input.json` file from this repository and click `Upload`.
16. Select the `Timeseries Data Sources` tab and choose the `Heat Pipe Data` data source. Click `Import Data` and select the `MAGNET_Heat_Pipe_2022-03-30.csv` file under the path `Experiment/Single_File` in this repository. Click `Upload.`
17. Now select the `Machine Learning Data` data source and do the same process for the `ML_MAGNET_2022-03-30.csv` file under the path `Machine_Learning/Single_File` in this repository.
18. Select the `Data Viewer` menu to see your graph data. You should see a `Heat Pipe` node named `MAGNET` surrounded by `Thermocouple`, `Cartridge Heater`, and `Structure` nodes. If you click on a node you can see its properties. Selecting the `Timeseries Data` menu on the `MAGNET` node will show the two timeseries data sources. Click on the view (eye) icon to view their data. You can also get to timeseries data by going to the data source page as described earlier. Unselect the `date_time` column from the `Heat Pipe Data` viewer before selecting the `Search` button. This shows the sensor readings over the duration of the experiment. The `Machine Learning Data` data source contains multiple machine learning predictions for a single time index, as predictions were made for the next 10 minutes every time new data came in (every few minutes). You can increase the limit to see more results for each data source.