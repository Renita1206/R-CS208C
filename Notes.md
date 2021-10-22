### What is R?
- interpreted computer language  
- flexible graphical environment  
  
## Basic Data Types  
- Character ( “a”, ‘b’)
- Numeric/Double – (2, 15.5)
- Integer (2L, 99L)
- Logical (TRUE, FALSE)
- Complex (1+4i)
- Vectors  
- Matrices    -> Objects of same class  
- Lists       -> elements of different data types
- Data Frames -> tabular data

## Basics  
- class(z) returns type  
- print(a)   
- x <- 10 assigns value 10 to variable x
- %% for modulus

## Vectors  
- combine function -c()  
        x <- 1:5 
- sequence function - seq()
        x <- seq(1,5, by=1) 
- vector(mode="numeric", length=10) produces a vector of 0s of length 10 
- x[1], x[c(1,2)] gives 1 and 1 2 respectively  
- x[x>2] gives 3 4 5  
- x%*%x - product of vector  
- x%o%x - outer product of vector  
- as.vector(x, mode = "any") 
- is.vector(x, mode = "any")
- names(x) <- y basically makes y the column names


## Sequences  
- c(sequence(5),sequence(10)) = sequence(c(5,10)) returns 1 2 3 4 5 1 2 3 4 5 6 7 8 9 10  
- seq(1,5, by=1) returns 1 2 3 4 5
- seq(1,5,length.out=10) returns sequence of length 10  
- rep(10, times=5) returns 10 repeated 5 times  


## Missing Values  
- is.na(x) returns a logical list 
- anyNA(x) return TRUE/FALSE 
- mean(x, na.rm=TRUE) ignores NA values to calculate mean  

## Matrix  
- m<-matrix(c(1,2,3,4,5,6), nrow=2, ncol=3, dimnames = list(c("a","b"),c("A","B","C")))
- attributes(m) returns dimensions and column names of matrix
- cbind(l1,l2)  => column  bind
- rbind(l1,l2)  => row bind
- m[rownumber,columnnumber] to access element
- diag(m) returns diagonal
- rowSums(m) returns sum of elements in each row
- colSums(m) returns sum of elements in each row

## Dataframes
- d<-data.frame(id=l1,name=l2)
- names(d)<-c("columnname1","columname2")
- rownames(d) returns row names
- colnames(d) returns name of columns
- summary(d)
- d$id

## Lists
- l<-list("a",1,2,3)
- vector.a<-unlist(list.a)

## Some Useful Functions  
- length(obj) - number of elements
- str(object) - structure of object
- names(object) - names
- ls() - lists current objects
- rm(object) - delete an object

## Factors
- facts<-factor(data) 
- table(data) - unique values and number of occurrences
- summary(facts) - same as table
- nlevels(facts) - number of levels (unique values)

## Date

Code	Value
%d	Day of the month (decimal number)
%m	Month (decimal number)
%b	Month (abbreviated)
%B	Month (full name)
%y	Year (2 digit)
%Y	Year (4 digit)

- as.Date('22JUN01',format='%d%b%y')  
- To extract the components of the dates, the weekdays, months, days or quarters functions can be used.
- thedate = ISOdate(2005,10,21,18,47,22)
        format(thedate,'%A, %B %d, %Y %H:%M:%S')

### Functions, environments, dates
mean(x)
median(x)
sd(x)
var(x)
cor(x, y)
cov(x, y)


x <<- 3; It forces x to be global
f <- function(n,p) sqrt(p*(1-p)/n)
name <- readline(prompt="Enter your name: ")
w<-read.table("D:\\R Programming\\Class Materials\\DataSets\\wine.csv", header = FALSE, sep=",")
head(w)
tail(w)
View(w)
write.table(w,"Path")

if (test_expression) {
statement
}

for(i in 1:10) {
table=num*i;
print(table);
}

i <- 1
while (i < 6) {
print(i)
i = i+1
}

break
next
repeat







