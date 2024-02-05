#### Analyzing Bangalore Traffic Congestion Pattern Based on Transit GPS data

<p align="justify">
In this study, we attempted to cluster or group the road segments based on the traffic patterns throughout the day. But collecting the data of all the traffic in metropolitan cities like Bangalore is not an easy task and analysing it is computationally not feasible. So, we assumed that patterns of the transit movement can be similar to that of traffic as they commute through all major routes in the cities and data will be relatively small. For this study, we considered the GPS data of the BMTC buses for one day.</p>

#### Dataset
<p align="justify">
The dataset comprises approximately 21.8 million GPS pings, including coordinates, time, and vehicle IDs. According to the GTFS data, BMTC operates a fleet of around 5600 buses on various routes. Additionally, we obtained BMTC stops data, encompassing 9,000 stops across different routes. Given the absence of a bus schedule, which includes the mapping of buses to routes or segments and their corresponding stopping points, the process of map matching or assigning segments to GPS pings becomes intricate and poses a bottleneck. To accurately represent buses as traffic entities, a substantial amount of pre-processing was undertaken. </p>

#### Pre-processing:
Since this is raw data, lot of preprocessing has been done for the model input. Some of the major preprocessing steps are:
1) Extracting the speed from the GPS data
2) Filtering GPS pings based on speed, location etc.,
3) Map Matching with segments from the Bangalore Graph
4) Extract the features for the road segments
5) Filtering the segments
6) Modelling

<p align="justify">
We explored various clustering algorithms like KMeans, Hierachical, GMM etc., and also applied dimension reduction techniques to enhance the model efficiency and for better visualization. </p>

#### Consclusion:
<p align="justify">
The consistent results from K-Nearest Neighbors (KNN) and Gaussian Mixture Models (GMM) affirm the robustness of clustering, revealing well-defined patterns in the dataset. Notably, Kernel PCA outperformed linear PCA in dimension reduction, signaling the presence of intricate non-linear relationships among variables. This suggests that certain features contribute significantly to the data’s variability, enhancing separation in reduced-dimensional space. The findings advocate for the exploration of non-linear techniques in future analyses to uncover specific features driving vements. Careful consideration of the balance between enhanced predictive capabilities and interpretability is crucial when leveraging non-linear methods. Overall, these insights offer a nuanced understanding of the dataset’s complexity and guide informed decision-making for subsequent analyses. </p>


