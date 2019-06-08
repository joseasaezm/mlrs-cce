<br>

This web-page contains complementary material to the research paper:

| <a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>| <a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|
|:---|:---|
|[<img src="icon-pdf.png" width="150">](https://ieeexplore.ieee.org/document/8715373)|José A. Sáez, Emilio Corchado. **A meta-learning recommendation system for characterizing unsupervised problems: on using quality indices to describe data conformations**. [IEEE Access](https://ieeeaccess.ieee.org/), vol. 7, pp. 63247-63263, 2019.|
| <a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>| <a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|

<br>

The web is organized according to the following summary:

1. [Abstract](#Abstract)
2. [Datasets](#Datasets)
3. [Performance results](#Performance)

<br>
 
## <a name="Abstract"></a> 1. Abstract
The clustering of a new *unsupervised problem* usually requires of knowing both if the samples may be separable in different groups and the number of these groups. This information, which has a great impact in the results obtained, is generally unknown beforehand. A wide explored research line in the literature proposes to use some metrics, known as *quality indices*, to determine the number of clusters in a dataset. However, they may lead to variable results depending on the metric chosen. This research analyzes the usage of a novel meta-learning system for determining the number of clusters in unsupervised data, called *Meta-Learning Recommendation System for Cluster Cardinality Estimation* (MLRS-CCE). It is based on the idea of using quality metrics not as a solution to the problem, but as a means to characterize the inner structure of each dataset and employing this information to detect when unsupervised data is not uniform and suggest additional information about the amount of clusters in the data. In order to achieve such goals a large collection of both real-world and synthetic datasets, in which the number of clusters is known *a priori*, are used to build the system and check its performance. The meta-learning system was successfully tested on such data, showing that it is accurate enough, both separating uniform data from non-uniform one and predicting cluster cardinality when it is compared to the results given by individual quality indices.

<br>
 
## <a name="Datasets"></a> 2. Datasets

<br>

### 2.1. Real-world datasets

30 real-world classification datasets are used as a basis to build the meta-learning recommendation system and another 24 are considered to validate its usefulness when characterizing unsupervised problems. In this way, different data structures from those of the datasets used in the building phase of the models are considered when validating the system. The following tables shows these datasets, along with their number of examples (*ex*), attributes (*at*) and classes (*cl*).

|<a href="#img1"><img src="bannercolor.jpg" width="450" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="450" height="10"></a>|
|:---:|:---:|
|**Training datasets**|**Validation datasets**|
|<a href="#img2"><img src="data-tra.jpg" width="450"></a>|<a href="#img2"><img src="data-val.jpg" width="450"></a>|
|<a href="#img1"><img src="bannercolor.jpg" width="450" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="450" height="10"></a>|

These datasets can be downloaded from the web-page of the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php).

<br>

### 2.2. Synthetic datasets

In the second scenario of study, instead of real-world datasets, synthetic data are used to build the meta-learning system. Thus, synthetic datasets with a different number of clusters (from 2 to 10) are created based on the random cluster generation algorithm proposed by Qiu and Joe (2006), in which the minimum degree of separation between a cluster and its nearest neighbor clusters is set by an user parameter. This proposal uses positive definite covariance matrices corresponding to different shapes, diameters and orientations of the clusters generated. Random noisy features and outliers are also considered when generating the synthetic datasets. The complete details about the cluster data generation method and the source code used to generate the synthetic data over the meta-learning system is built can be downloaded below:

|<a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>|
|:---|:---:|
|**Description** |**File**|
|Weiliang Qiu and Harry Joe. **Generation of random clusters with specified degree of separation**. *Journal of Classification*, 23(2):315–334, 2006.| [<img src="icon-pdf.png" width="50">](https://raw.github.com/joseasaezm/mlrs-cce/master/docs/2006-JC-Qiu.pdf)|
|Source code of the random cluster generation method of Qiu and Joe (2006)| [<img src="icon-method2.png" width="50">](https://cran.r-project.org/web/packages/clusterGeneration/index.html)|
|<a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>|

The parameter setup used with the above source code to genereate the synthetic dataset in this scenario is show in the following table:

<center>
<a href="#img2"><img src="data-syn.jpg" width="550"></a>
</center>

<br>

## <a name="Performance"></a> 3. Performance results

|<a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>|
|:---|:---:|
|**Distributions of quality indices** |**File**|
|&nbsp;&nbsp;&nbsp;**-** *Histograms for real-world datasets* | [<img src="icon-pdf.png" width="50">](https://raw.github.com/joseasaezm/mlrs-cce/master/docs/HIS-REAL.pdf)|
|&nbsp;&nbsp;&nbsp;**-** *Histograms for synthetic datasets* | [<img src="icon-pdf.png" width="50">](https://raw.github.com/joseasaezm/mlrs-cce/master/docs/HIS-SYNT.pdf)|
|<a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>|
|**Performance results of cluster cardinality estimation methods** |**File**|
|&nbsp;&nbsp;&nbsp;**-** *Performance for real-world datasets* | [<img src="icon-excel.png" width="50">](https://raw.github.com/joseasaezm/mlrs-cce/master/docs/PERF-REAL.xlsx)|
|&nbsp;&nbsp;&nbsp;**-** *Performance for synthetic datasets* | [<img src="icon-excel.png" width="50">](https://raw.github.com/joseasaezm/mlrs-cce/master/docs/PERF-SYN-ACC.xlsx)|
|&nbsp;&nbsp;&nbsp;**-** *Performance for data with two cluster cardinalities* | [<img src="icon-excel.png" width="50">](https://raw.github.com/joseasaezm/mlrs-cce/master/docs/PERF-SYN-PAIR.xlsx)|
|<a href="#img1"><img src="bannercolor.jpg" width="750" height="10"></a>|<a href="#img1"><img src="bannercolor.jpg" width="100" height="10"></a>|
