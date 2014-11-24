M2N
===
The experiments are divided in two steps. The first is related to the base-level and the second to the meta-level performance. To run the measures we need some R packages and the DCoL library. 

## Technical Requirements

R version 3.1.0 -- "Spring Dance"

DCoL Library: http://dcol.sourceforge.net/ 

Packages: CORElearn, e1071, FNN, foreign, infotheo, rpart, R.utils, rrcov and mvpart.

Install the packages:

```

install.packages(c("CORElearn", "e1071", "FNN", "foreign", "infotheo", 
"rpart", "R.utils", "rrcov", "mvpart"))

```

## Set the experiments

Before start to run the measures we need the binary of the DCoL library. Download the code of DCoL Library at http://dcol.sourceforge.net/ and follow the instructions to compile the code in the README file. After that, put the executable (binary file) inside the m2n folder with the name "dcol".

Open the R inside the m2n folder.

## Base-level

In the base-level folder we have the datasets used in this work, the measures to characterize the datasets and some complementary information about the base-level.

### How to load the datasets?

The easiest way to load the datasets (arff files) is with the packages RWeka or foreign:

```
# load the iris dataset
require("foreign")
data = read.arff("base-level/database/iris.arff");

```

### How to run the measures?

Load the source codes:

```
# load the complexity measures
source("base-level/measures/complexity.r")

```

```
# load the characterization measures
source("base-level/measures/characterization.r")

```

Run the functions with the data set as parameter:

```
# characterization measures
characterization(iris);

# complexity measures
complexity(iris);
```

## Meta-level

In the meta-level folder we have the meta-datasets in the rand and pairwise folder and some complementary information about the base-level.

### How to load the datasets?

The easiest way to load the datasets (.RData files) is with the dget function:

```
# load the iris dataset with random noise
data = dget("meta-level/database/rand/iris.RData");

```

### Contact

Luis Paulo Faina Garcia - lpfgarcia [at] gmail.com

University of São Paulo - Campus São Carlos


### References

[1] K. Bache, M. Lichman, UCI machine learning repository, http://archive.ics.uci.edu/ml (2013).

[2] A. Orriols-Puig, N. Maciá, T. K. Ho, Documentation for the data complexity library in C++, Tech. rep., La Salle - Universitat Ramon Llull (2010).

[3] M. Reif, A comprehensive dataset for evaluating approaches of various meta-learning tasks, in: First International Conference on Pattern Recognition and Methods (ICPRAM), 2012.

[4] R Core Team, R: A Language and Environment for Statistical Computing, R Foundation for Statistical Computing, Vienna, Austria (2014). URL http://www.r-project.org/
