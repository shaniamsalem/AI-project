
# ML project for news classification README

This is a manual for the kaggle notebook. Before running anything run the cells under the following titles:
* Dependencies
* Helpers


### Final Model

#### Test the final model

    1. load dataset in 1 out of 3 options:
        a. prepare & load csv file with columns:
            'text' - contains the news to be classified
            'label' - the true classification of the news (optional) 
           Separate the 2 columns to 2 different DataFrames: X, y.
        b. run the cell under: Load Data to load our test data
        c. run the cell under: On IDF Press releases
    2. run the cell under: Feature Extraction
    3. run the cell under: Data Visualization
    4. run the cell under: Load Best Parameters
    5. run the cell under: Feature Selection -> Load Features
    6. run the cell under: Feature Selection -> Only WordCloud features
    7. run the cell under: Build the final model
    8. run the cell under: Load Final Model
    9. run the cell under: Test Final Model
    10. run function 'test' defined under: 'Test Final Model' on data X and labels y.

#### Fit the final model
    1. perform the previous steps: 1-7 of data loading
    2. run the cells under: Fit final model (except for saving the model) on data X and labels y.

### Experiments
First, run the cell under: Load Data

#### Tuning parameter experiment:
    1. find the title of the desired model and navigate to it
    2. run the cells under the tuning parameter title

#### Feature selection experiment:
    can be found under: Feature Selection. Under each sub title documentation can be found for the specific case.
    1. run the cell under: Data Visualization
    2. run the cell under: Load Best Parameters
    3. run the cell under: Feature Selection -> Train & Test Models
    4. run the cells under the desired feature selection method.

#### Combinations of feature selection methods experiment:
    can be found under: Different combinations of feature selection
    1. run the cell under: Feature Selection -> Load Features
    2. run the cell under: Feature Selection -> Train & Test Models
    3. run your desired combinations out of the 3 cells.


### Data processing stages
    1. perform the steps: 1-8 of data loading in "Test the final model"
    2. run: X = final_model.processing_texts(X) to process texts 
    3. run: X = final_model.calculate_features(X) to calculate features (step 2 must run beforehand)
    (X must exclusively contain 'text' column)

### Visualizations
First, run the cell under: Load Data
#### Correlation matrix of all features and label: (before feature selection)
    run the cells under: Feature Selection -> Features & target Correlation visualization
#### Visualize Word Clouds: 
    run the cell under Data Visualization

For any other experiment the visualizations can be found under the title of that specific experiment.