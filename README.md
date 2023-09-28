# AI Master Thesis Mitchell D. Lobbes
------
*A good decision is based on knowledge and not numbers - plato*

-------
### Environment Creation
The run the code in this repository a virtual environment needs to be created:
- Run the following command in the terminal: conda create -n Environment_1 python=3.10.12
- Follow this up by installing the needed libraries using: pip install -r requirements.txt

### Repository Structure
The structure of the repository is organized as follows:

1. **Code Folder**: Contains the preprocessing and model notebooks
2. **Data Folder**: Contains and stores all the data used in this repository. Data is divided in Client, Location and Model data


### Run order to replicate results


1.  (OPTIONAL) Use **Environment_1** to retrieve the location data and store it by running the following notebooks in order:
    - Code/Preprocessing/Location_data_parser.ipynb
    - Code/Preprocessing/Client_location_data_merger.ipynb (Not available to run due to privacy constraints)

2. Due to privacy constraints the anonymized location data is already merged with the client data and anonymized. The dataset can be found here:
    - Data/Model/Model_data.csv

3. (REQUIRED) Use **Environment_1** to run the following notebook to perform the explanatory analysis and generate the cleaned dataset that will be used for training the machine learning models:
    - Code/Preprocessing/Explanatory_Analysis.ipynb

4. (REQUIRED) Use **Environment_1** to train and evaluate the following models:
    - Code/Model/DecisionTree/M2.ipynb
    - Code/Model/RandomForest/M2.ipynb
    - Code/Model/XGBoost/M2.ipynb
    - Code/Model/LightGBM/M2.ipynb