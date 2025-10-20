# Cheatsheet R
```
x <- c(1,2,3) - vector (1,2,3)
logs <- vector("logical", length=5)
1:3 - range
seq(1,15,3) - sequence (start, finish, step)
rep(3,5) - p prints 3 5 times
rm(x) - deletes x
```
### indexing
```
v <- c(10, 21, 32, 47)
v[1] # 10 will be printed
v[-4] # 10 21 32
v[c(2, 3)] # 21 32
v[-c(2, 3)] # 10 47
v[v > 25] # 32 47
```
### funcs
```
length(v) # 4
sort(x) # 10 21 32 47
ifelse(<logical expression>, <'yes' case result>, <'no' case result>)
any(...)
all(...)
```
### aggregating funcs
```
min(v) # 10
max(v) # 47
diff(v) # 11 11 15
sum(v) # 110
cumsum(v) # 10 31 63 110
```
### sequences
```
rep(5, times=8) # 5 5 5 5 5 5 5 5
rep(c(2, 6), each=5) # 2 2 2 2 2 6 6 6 6 6

seq(from=1, to=10, by 2) # 1 3 5 7 9
seq(from=0, to=1, length.out=4) # 0.000 0.3333 0.666667 1.000
```
### matrixes
```
M <- rbind(c(1, 2, 3, 4), c(5, 6, 7, 8))
M <- cbind(c(1, 2, 3, 4), c(5, 6, 7, 8))

M[c(3, 1), ] # prints the third and first row as a matrix
M[order(M[, 1]), ]
M[order(M[, 1], M[, 2]), ]

M <- matrix(c(1:16), nrow=8, ncol=2)
M <- matrix(c(1:16), nrow=8, ncol=2, byrow=TRUE)

A <- matrix(c(1, 5, -3, 3.4, 0, -2), nrow=3, ncol=2)
rownames(M) <- c("row1", "row2", "row3")
colnames(M) <- c("col1", "col2")
```
### simulations
```
sample(range, size, replace = F) - generates size random elements from range without repetitions
sample(vector, size, replace = T) - generates size random elements choosing from vector with repetitions
sample(vector, size, replace = T, prob = vector) - generates elements according to probability vector with same length

replicate( times, func) - executes func <times> times and returns vector with the results 
table(vector) - makes table with the different elements and how many times they are seen in the vector
sum(vector==value) - returns the sim of all the elements with value <value> in the vector

length(vector) - number of elements
duplicated(vector) - returns true for each element if it is duplicated in the vector
any(bool array) - returns true if at least one of the elements is true
unique(vector) - returns vector with the unique elements of the vector

all(bool array) - returns true if all the elements are true
c(vector1, vector2) - concatenates the two vectors
c(1,2,3) %in% c(1,2,3) - returns true/false for each element if the elements of the first vector are in the second vector
which(vector == value) - returns the indexes where elements are equal to value
```
