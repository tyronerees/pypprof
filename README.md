# pypprof
Generate performance profiles from the command line

pypprof reads in data from files containing performance data for some metric.
Each piece of software requires its own data file, and each
column of each file corresponds to one metric value 
representing the software's performance on a test problem.
Failures should be represented by negative values.
 
Because each line corresponds to a test problem, the
order of the problem values should be maintained across files.
The required arguments (of which there must be at least 3) are the
names of the data files, the column we're interested in (placed after the -c flag), 
and a label for the statistic being compared 
(e.g. "feval" could be used for function evaluations)
Type 
  ./pypprof --help
for the calling sequence, and the full range of options

Tyrone Rees, RAL, August 2016
(inspired by the shell script pprof by Nick Gould, 
 which uses the perl script newperf3 by Nick Gould,
 which in turn was an adaptation of the perl script perfneger by Liz Dolan)
