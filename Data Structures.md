# R-learning
## five data structures
### 1. vector
a <- c(1,2,3,4)  a[1] = 1
### 2. matrix
m <- matrix(1:20, nrow=5, ncol=4)

c <- c(1,2,3,4)  m <- matrix(c, nrow=2, ncol=2)
### 3. array
dim1 <- c(1,2)  dim2 <- c(1,2,3) dim3 <- c(1,2,3,4)

z <- array(1:24, c(2,3,4), dimnames = list(dim1,dim2,dim3))
### 4. data frame
patientdata <- data.frame(c1,c2,c3,c4)

it is the most common data structure, including rows' and columns' names.

**factor**: nominal and ordered nonminal variables are called factors. For nominal variables: diabetes <- factor(diabetes); for ordered nonminal variables: status <- factor(status, oreder = TRUE). Then those vairables will be mapped to different levels.
### 5. list
