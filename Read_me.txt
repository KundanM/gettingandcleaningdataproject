This file describes how run_analysis.R script works.

It works on the manually unzipped and extracted data folder "UCI HAR Dataset".
Make sure the run_analysis.R script is in the data folder "UCI HAR Dataset" too.
Execute the  source("run_analysis.R") command in RStudio.
Two output files are generated in the current working directory:
merged_data.txt (7.9 Mb): it contains a data frame called cleanedData with 10299*68 dimension.
data_with_means.txt (220 Kb): it contains a data frame called result with 180*68 dimension.
Finally, use data <- read.table("data_with_means.txt") command in RStudio to read the file. 