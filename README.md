# **Apriori Algorithm:**


The Apriori Algorithm produces frequent patterns by generating itemsets and discovering the most frequent itemset over a threshold “minimal support count”. 

It greatly reduces the size of the itemset in the database by one simple principle:
    If an itemset is frequent, then all of its subsets must also be frequent.


# **FP-Growth:**


FP-growth is an improved version of the Apriori Algorithm which is widely used for frequent pattern mining.
It is used as an analytical process that finds frequent patterns or associations from data sets.


However, the Apriori Algorithm has a major shortfall. Using Apriori required multiple scans of the database to check the support count of each item and itemsets. When the database is huge, this will cost a significant amount of disk I/O and computing power. Therefore the FP-Growth algorithm is created to overcome this shortfall. 

It only scans the database twice and used a tree structure(FP-tree) to store all the information. The root represents null, each node represents an item, while the association of the nodes is the itemsets with the order maintained while forming the tree. The FP-tree is concise and is used to directly generating large itemsets. Once an FP-tree has been constructed, it uses a recursive divide-and-conquer approach to mine the frequent itemsets.
