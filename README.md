M2N
===
The experiments are divided in two steps. The first is related to the base-level and the second to the meta-level performance. To run the experiments we need some R packages and the DCoL library. 

### Technical Requirements

R version 3.1.0 -- "Spring Dance"

DCoL Library: http://dcol.sourceforge.net/ 

Packages: CORElearn, e1071, FNN, foreign, infotheo, rpart, R.utils, rrcov and mvpart.

Install the packages:

```

install.packages(c("CORElearn", "e1071", "FNN", "foreign", "infotheo", 
"rpart", "R.utils", "rrcov", "mvpart"))

```

### Set the experiments

Before start to run the measures we need the binary of the DCoL library. Download the code of DCoL Library at http://dcol.sourceforge.net/ and follow the instructions to compile the code in the README file. After that, put the executable dcol in the directory ~/measures/

### Run the measures

Load the source codes:

```
# load the complexity measures
source("complex.r")

```

```
# load the characterization measures
source("characterization.r")

```

Run the functions with the data set as parameter:

```
# characterization measures
characterization(iris);

# complexity measures
complex(iris);
```

### Contact

Luis Paulo Faina Garcia - lpfgarcia [at] gmail.com

University of São Paulo - Campus São Carlos


### References

[1] K. Bache, M. Lichman, UCI machine learning repository, http://archive.ics.uci.edu/ml (2013).

[2] A. Orriols-Puig, N. Maciá, T. K. Ho, Documentation for the data complexity library in C++, Tech. rep., La Salle - Universitat Ramon Llull (2010).

[3] M. Reif, A comprehensive dataset for evaluating approaches of various meta-learning tasks, in: First International Conference on Pattern Recognition and Methods (ICPRAM), 2012.

[4] R Core Team, R: A Language and Environment for Statistical Computing, R Foundation for Statistical Computing, Vienna, Austria (2014). URL http://www.r-project.org/
