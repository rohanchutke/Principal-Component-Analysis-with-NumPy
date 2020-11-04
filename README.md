# Principal-Component-Analysis-with-NumPy

# Task 1: Load the Data and Import Libraries
Load the dataset using pandas.
Import essential modules and helper functions from NumPy and Matplotlib.
Explore the pandas dataframe using the head() and info() functions.

# Task 2: Visualize the Data
Before starting on any task, it is often useful to understand the data by visualizing it.
For this dataset, we can use a scatter plot using Seaborn to visualize the data.

# Task 3: Data Standardization
With great power to reduce dimensionality, comes great responsibility.
One must take care to preprocess the input data appropriately.
Make sure to zero-out the mean from each feature (subtract the mean of each feature from the training set), and normalize the values if your features have differing units.
PCA is best used when the data is linear, because it is projecting it onto a linear subspace spanned by the eigenvectors.
This is an important step in many machine learning algorithms, and especially so in the case of PCA. We want the PCA algorithm to give equal weight to each of the features while making the projection.
If one or more features are in a different scale than the rest, those non-standardized features will dominate the eigenvalues and give you an incorrect result This is a direct consequence of how PCA works. It is going to project our data into directions that maximize the variance along the axes. 

# Task 4: Compute the Eigenvectors and Eigenvalues
There are two general ways to perform PCA. The more computationally effective way is to do something called Singular Value Decomposition or SVD.
It decomposes a matrix into the product of two unitary matrices (U, V*) and a rectangular diagonal matrix of singular values (S).
The mathematics of computing the SVD is a little complicated and out of the scope of this project. If you’re familiar with linear algebra, I highly encourage you to read about it on your own time.
Luckily for us, there is a numpy function that performs SVD on the input matrix, so we don’t really need to worry about the math for now.
We’re going to cover SVD in the next task.
Recall that PCA aims to find linearly uncorrelated orthogonal axes, which are also known as principal components (PCs) in the m dimensional space to project the data points onto those PCs. The first PC captures the largest variance in the data.
The PCs can be determined via eigen decomposition of the covariance matrix Σ. After all, the geometrical meaning of eigen decomposition is to find a new coordinate system of the eigenvectors for Σ through rotations.

# Task 5: Singular Value Decomposition (SVD)
Singular Value Decomposition or SVD is a computationally efficient method to perform PCA.
It decomposes a matrix into the product of two unitary matrices (U, V*) and a rectangular diagonal matrix of singular values (S). The mathematics of computing the SVD is a little complicated and out of the scope of this project.

# Task 6: Selecting Principal Components Using the Explained Variance
The use of PCA means that the projected data can be analyzed along axes of principal variation.
Plot the cumulative explained variance against the number of principal components.
Rank components according to the explained variance each component contributes to the model.

# Task 7: Project Data Onto Lower-Dimensional Linear Subspace
Utilize principal component analysis to decompose high dimensional data into two or three dimensions so that each instance can be plotted in a scatter plot.
