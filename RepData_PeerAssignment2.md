# Reproducible Research
Lamont Girton  
September 27, 2015  



#Synopsis

#Data Processing

Below is the script used to determine if the StormData.csv.bz2 archive exists in the current working directory, and if not, will download it over HTTPS at [Storm Data][Storm Data].  The data is read into a variable named _storm_ and this code chunk has it's _cache_ option set to TRUE to avoid reading this large dataset every time with document is weaved.


```r
url <- "https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2FStormData.csv.bz2"
if (!file.exists("StormData.csv.bz2")) {
    download.file(url, destfile = "StormData.csv.bz2", method = "curl")
}

storm <- read.csv("StormData.csv.bz2", stringsAsFactors = F)
```



```r
library(dplyr)
library(ggplot2)
```


#Results

[Storm Data]: https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2FStormData.csv.bz2

