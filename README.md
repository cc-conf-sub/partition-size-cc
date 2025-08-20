### Data Format:

* Data files are stored in Data/\[name of data set]/graph.txt

  * All data sets are either publicly available or provided here
  * We provide data set samples to show the format for the various experiments

* Delimiter is hard-coded in driver files
* For K Correlation Clustering:

  * The first line of the file must contain the total number of nodes (anything that follows it on the line will be ignored)
  * Rest of file lists positive edges as \[node1] \[node2]

To Compile: javac \*.java
To Run: java \[DriverName] \[data set folder name]

* additional heap space may be needed for some experiments; increase the max heap size with the -Xmx flag

### Drivers

Hard coded parameters:

* delimiter for data set ("\\s" for whitespace)
* number of Pivot rounds, number of attributes used, etc.

RunKCorrelation.java

* Input: positive edge list
* Methods: Pivot, Vote (Heap)

RunKBlend.java, RunKLocalSearch

* Input: positive edge list, largest partition size
* Methods: Vote (Fast), LocalSearch

### Code Files

DNode.java

* Implementations of Vote

Helper.java

* Helper functions for reading data sets

Pair.java

* Custom data structure used for heap implementation

PKwik.java

* Pivot algorithm implementations

KLocalSearch.java

* LocalSearch implementations
