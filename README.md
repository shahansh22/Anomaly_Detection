DBScan is a nonlinear clustering method which splits all data into three points: Core point, Border point, Outliers/Noise
There are also 2 hyperparameters: Minimum number of points, epsilon(radius)
The split is done based on no. of data points within the radius of the selected data point:
Core: no. of neighbouring points > min no. of pts
Border: no. of neighbouring points < min no. of pts
Outlier: NO points in neighbouring area

Local Outlier Factor uses a different approach, it looks at outliers in two different ways:
Global outlier: A completely isolated data point
Local outlier: A data point which is isolated but is somewhat close to another cluster
LOF outlier detection uses KNN to determine the local density to the selected point and its 'k' nearest points.
If the density of nearest 'k' neighbours is higher than that of the actual point, the point can be considered to be a local outlier since the neighbours are
much closer packed with others than the point is to them.
