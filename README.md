# Load-Digits-PCA-Model
Articulately loaded and visualized data from the 'load_digits' library. Applied a manual, nuanced Principal Component Analysis (PCA)  using covariance metrics, eigen vectors, and values. Crafted an insightful decision tree model for data analysis.

## Summary of "Load_Digits_PCA.ipynb":
1. **Data Loading and Exploration**:
   - The code loads the Digits dataset, which consists of images of handwritten digits.
   - It displays the shape of the dataset, showing it has 1797 samples with 64 features each.
   - The code snippet plt.imshow(digits.images[1], cmap=plt.cm.gray) displays an image of a handwritten digit from the dataset.
   - It then creates a Pandas DataFrame data1 containing the digit data using pd.DataFrame(digits.data).
   - The data1.head() command displays the first few rows of the DataFrame, showing the structure of the data.

2. **Data Visualization**:
   - The code visualizes a subset of the dataset, displaying images of handwritten digits along with their corresponding labels.

3. **Data Preprocessing**:
   - Standardization: The code standardizes the features of the dataset using the StandardScaler from scikit-learn.

4. **Data Splitting**:
   - The code `x = digits.data` and `y = digits.target` separates the features (x) and target labels (y) from the dataset.

5. **Data Standardization**:
   - The code snippet `X_std = StandardScaler().fit_transform(x)` standardizes the feature data to have zero mean and unit variance.
   - It reshapes the standardized data for further processing.

6. **Covariance Matrix Calculation**:
   - The code calculates the covariance matrix of the standardized data using `cov_mat = np.cov(X_std.T)`.
   - This matrix represents the relationships between different features in the dataset.

7. **Eigen Decomposition**:
   - The code performs eigen decomposition on the covariance matrix to obtain eigenvectors and eigenvalues.
   - These eigenvectors represent the principal components of the dataset.

8. **Explained Variance**:
   - The code snippet calculates the explained variance ratio for each principal component, providing insights into the importance of each component.

9. **Principal Component Analysis (PCA)**:
   - Covariance Matrix Calculation: It computes the covariance matrix of the standardized dataset.
   - Eigen Decomposition: The code performs eigen decomposition on the covariance matrix to obtain eigenvalues and eigenvectors.
   - Explained Variance: It calculates the explained variance ratio for each principal component.

## Algorithms and Techniques Applied:
- **PCA (Principal Component Analysis)**: Used for dimensionality reduction by transforming the data into a lower-dimensional space while preserving the variance.
- **StandardScaler**: Applied to standardize the features of the dataset before PCA.
- **Covariance Matrix**: Calculated to understand the relationships between different features.
- **Eigen Decomposition**: Used to find the principal components (eigenvectors) and their importance (eigenvalues).

## Code Explanation:
- **Data Loading**: The code loads the Digits dataset.
- **Data Visualization**: It displays images of handwritten digits.
- **Data Preprocessing**: Standardizes the dataset.
- **PCA Implementation**: Computes the covariance matrix, performs eigen decomposition, and calculates explained variance.

This file serves as a comprehensive guide for implementing PCA on the Digits dataset, showcasing data preprocessing, visualization, and dimensionality reduction techniques. It can be used as a detailed reference for understanding PCA and its application in machine learning projects.
