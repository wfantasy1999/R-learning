# R learning
## Data Input
### 1. From keyboard
mydata <- data.frame(age = numeric(0), gender = character(0), weight=numeric(0))

mydata <- edit(mydata)

**Invoke the text editor**

*Why R use <- instead of =?*


*It can make difference between variables in functions. ep: A <- list(title = mylist, ...)*

## 2. From text file
mydata <- read.table(file, header = logical_value, sep = "\t", row.names = "name")

header can indicate whether the first row is variable names. row.names is an optional parameter to represent row indentifiers.

## 3. From Excel file
install.package("RODBC")

library(RODBC)

channel <- odbcConnectExcel("myfile.xls")

mydata <- sqlFetch(channel, "mysheet")

odbcClose(channel)

## 4. From SPSS
instal.package("Hmisc")

library(Hmisc)

mydata <- spss.get("mydata.sav", use.value.labels = TRUE)

## 5. From DBMS

library(RODBC)

myconn <- odbcConnect("mydsn", uid = "...", pwd = "...")

crimedata <- sqlFetch(myconn, Crime)

pundata <- sqlQuery(mycoon, "select * from Punishment")

close(myconn)
