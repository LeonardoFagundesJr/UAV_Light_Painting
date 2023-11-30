# UAV_Light_Painting
Creating long exposure photographs by controlling a UAV through gesture-based teleoperation.

# Explanation of the database

The classification procedure implemented in this study is based on comparing the sample data under analysis with the reference standards associated with each class. This evaluation determines whether the sample is contained in a specific ellipsoid linked to a distinct class. 

The structure of the database adopted consists of a three-dimensional matrix of dimensions $C x (2+Ns) x 3$, where C represents the number of rows in the matrix, equivalent to the number of classes; (2+Ns) indicates the number of columns, the first two of which represent the mean and standard deviation of the samples in each class, while the subsequent Ns columns contain the mean of each sample used to calculate the class mean and standard deviation. The last dimension, 3, stores the spatial coordinates (x, y, z) of each element in the matrix.

As an example, when creating an ellipsoid to classify a sample of the "Land" class, it would be necessary to access the information on the mean and standard deviation of this class on the x, y and z axes, located at positions 2 x 1 and 2 x 2, respectively. To make changes to the ellipsoid, you would first need to replace one of the samples in the class, for example, 2 x 4 (representing the second sample stored in the base, considering that the first two columns indicate the mean and standard deviation, while from the 3rd column onwards the samples are stored). Subsequently, it would be necessary to recalculate and update the mean and variance of the respective class.
