# 利用KDTree近邻搜索

k-d树（k-dimensional树的简称），是一种分割k维数据空间的数据结构。主要应用于多维空间关键数据的搜索（如：范围搜索和最近邻搜索）。K-D树是二进制空间分割树的特殊的情况。

索引结构中相似性查询有两种基本的方式：一种是范围查询（range searches），另一种是K近邻查询（K-neighbor searches）。范围查询就是给定查询点和查询距离的阈值，从数据集中找出所有与查询点距离小于阈值的数据；K近邻查询是给定查询点及正整数K，从数据集中找到距离查询点最近的K个数据，当K=1时，就是最近邻查询（nearest neighbor searches）。

PCL中类`pcl::KdTree<PointT>`是kd-tree数据结构的实现。并且提供基于FLANN进行快速搜索的一些相关子类与包装类。

* **pcl::search::KdTree<PointT>**

`pcl::search::KdTree<PointT>`是`pcl::search::Search< PointT >`的子类，是`pcl::KdTree<PointT>`的包装类。
