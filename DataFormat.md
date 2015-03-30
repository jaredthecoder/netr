# General information #
  * the target variables (classes) have to be enumerated consecutively, starting by zero (libsvm format is an exception)

# Formats #
netr supports following ASCII data formats:
  * CSV
    * target variable have to be placed in first column
    * you can specify the used delimiter
    * no missing values allowed
  * libsvm sparse format
    * only suitable for two-class-problems with labels "-1" and "+1"
    * sparse format: only non-zero values, e.g. "+1 0:1 2:1 3:1 5:1"
    * missing values are assumed to be zero
  * jf (see also http://www-i6.informatik.rwth-aachen.de/~keysers/usps.html)
    * everything is space separated
    * header: first line contains two integers: <number of classes> and <number of attributes (features)>
    * next N lines contain N data samples with target values in the first column
    * footer: last line must consist of the string "-1" only
    * no missing values allowed

# gzip #
netr supports reading from gzipped files. gzip is used if filename ends with ".gz".