# Data-Mining-via-Data-Reduction

Explanation of the code implementation:
First, we imported the necessary libraries that will be used in the code.
“numpy” is a library for numerical operations in Python.
“matplotlib” is a library for creating visualizations in Python.
“offsetbox” is a module within matplotlib that provides tools for creating annotated text and
images in plots.
“sklearn” is a library that provides a set of tools for machine learning and data analysis,
including manifold, datasets, decomposition, and discriminant_analysis.
We then load the “digits” dataset from “sklearn.datasets”, which is a set of images of
handwritten digits with corresponding labels.
“X” is set to the data attribute of the digits dataset, which contains the features for each image.
“y” is set to the target attribute of the digits dataset, which contains the corresponding labels for
each image.
“n_samples” and “n_features” are set to the number of samples and number of features in the X
matrix, respectively
We have then defined a function embedding_plot in which the function first normalizes X to be
between 0 and 1 by subtracting the minimum value from each column and dividing by the range
of each column.
Then, it creates a scatter plot of the first two columns of X, where the color of each point is
determined by its corresponding label in y.
The function also adds annotations to the plot, which are images of the handwritten digits
corresponding to each point. The shown_images variable keeps track of which images have
already been shown so that duplicate images are not displayed.
Finally, the function sets the x and y axis ticks to be empty and sets the title of the plot to title.
Note that this function does not actually display the plot; it only sets it up. To display the plot,
you would need to call plt.show() after calling this function.
The first Dimensionality Reduction technique used in this assignment, Principal Component
Analysis (PCA), is as follows:
X_pca = decomposition.PCA(n_components=2).fit_transform(X)
The above line applies Principal Component Analysis (PCA) to the X data using sklearn's
decomposition.PCA class, with the argument n_components=2 indicating that we want to
reduce the data to two dimensions. The resulting transformed data is stored in X_pca.
We then call the embedding_plot function that we defined earlier, passing in X_pca as the first
argument and the string "PCA" as the second argument. This creates a scatter plot of the
PCA-transformed data with the handwritten digit images as annotations. And then we display
the data.
