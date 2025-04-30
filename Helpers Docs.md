
## Helpers Documentation

#### save_state(state, path='state.txt')
saves state to file in path via pickle 

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `state` | `Object` | **Required**. Object to save |
| `path` | `string` | **Optional**. File path to save to |

#### load_state(path='state.txt')
returns state saved in path via pickle

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `path` | `string` | **Optional**. File path to load from |

#### visualize_importances(importances)
presents a bars graph of the importances of the 40 most important features
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `importances` | `list` | **Required**. List of floats representing the texts_X_train's features' importances. Must be of length of texts_X_train's features.|

#### visualize_confusion(cm)
presents a diagram of the confusion matrix cm

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `cm` | `ndarray` | **Required**. Output of sklearn.metrics.confusion_matrix (meant for this specific use case)|

#### visualize_correlation(X, y, sampled_columns=None, visualize=True, correlationMatrix=None)
By default, calculate correlation matrix of DataFrame: [X,y], visualize it and return the correlation matrix. If correlationMatrix is not None don't calculate correlation matrix and just use it. If visualize is False don't visualize. If sampled_columns is not None visualize only this subset of features.

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `X` | `pd.DataFrame` | **Required**. Dataset with features of type float|
| `y` | `pd.DataFrame` | **Required**. Label column (binary)|
| `sampled_columns` | `list` | **Optional**. Subset of the columns of X|
| `visualize` | `Boolean` | **Optional**. If True, visualize the correlation matrix|
| `correlationMatrix` | `pd.DataFrame` | **Optional**. Output of pd.DataFrame.corr(method='pearson') or of visualize_correlation.|

#### visualize_clf(clf, X, Y, title, xlabel, ylabel, marker_size=50, grid_length=300, linewidths=None):
Visually demonstrate the decision boundaries of a binary classifier, showing how it classifies data points in a 2D feature space only.

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `clf` | `` | **Required**. Classifier with predict method|
| `X` | `pd.DataFrame` | **Required**. Dataset containing in columns ONLY xlabel and ylabel|
| `Y` | `pd.DataFrame` | **Required**. Binary column with size of X.shape[0]|
| `title` | `string` | **Required**. Title of the diagram|
| `xlabel` | `string` | **Required**. One of the 2 features in X.columns|
| `ylabel` | `string` | **Required**. The other feature of the 2 features in X.columns|
| `marker_size` | `float` | **Optional**|
| `grid_length` | `float` | **Optional**|
| `linewidths` | `float` | **Optional**|