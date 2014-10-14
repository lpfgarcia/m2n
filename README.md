M2N
===
The experiments are divided in two steps. The first is related to the base-level and the second to the meta-level performance. To run the experiments we need some R packages and the DCoL library. 

### Technical Requirements

R version 3.1.0 -- "Spring Dance"

DCoL Library: http://dcol.sourceforge.net/ 

Packages: CORElearn, FNN, infotheo, kknn, rpart, R.utils, rrcov and mvpart.

### Set the experiments

Before start to run the measures we need the binary of the DCoL library. Download the code of DCoL Library at http://dcol.sourceforge.net/ and follow the instructions to compile the code in the README file. After that, put the executable dcol in the diretory ~/measures/

### Run the measures

Load the files and run the funcions with the data as parameter:


```
# characterization measures
feature(data);

# complexity measures
complex(data);
```
