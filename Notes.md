### What is R?
- object oriented programming environment
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
- x <<- 3; It forces x to be global

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
- as.numeric()
- The POSIXct class stores date/time values as the number of seconds since January 1, 1970.
- The POSIXlt class stores them as a list with elements for second, minute, hour, day, month, and year, among others
- difftime(d1,d2,units='weeks')
- seq(as.Date('1976-7-4'),by='days',length=10)
- To extract the components of the dates, the weekdays, months, days or quarters functions can be used.
- thedate = ISOdate(2005,10,21,18,47,22)
        format(thedate,'%A, %B %d, %Y %H:%M:%S')


### Statistic Functions
- mean(x)
- median(x)
- sd(x)
- var(x)
- cor(x, y)
- cov(x, y)
- floor(2.13)


## Functions
f <- function(n,p) sqrt(p*(1-p)/n)

## Reading Input
- name <- readline(prompt="Enter your name: ")
- w<-read.table("path.csv", header = FALSE, sep=",")
        head(w)
        tail(w)
        View(w)
- readLines(), source() and load()

- writeLines(), dump(), save() and serialize()
- write.table(w,"Path")

## If condition
if (test_expression) {
statement
}

## For loop
for(i in 1:10) {
table=num*i;
print(table);
}

## While loop
while (i < 6) {
print(i)
i = i+1
}

## Jump statements
- break
- next
- repeat

## Strings
paste("Everybody", "loves", "stats.", sep="")
cat("The zero occurs at", 2*pi, "radians.", "\n")

## Debugging
- traceback() - call stack, lists out function calls
- debug(function name) - flagged for debugging, line by line, n,c,q and where
- trace - to make minor modifications without modifying funtions and re-sourcing, to track down errors
   trace(func_name, code to insert, at=x, print=F)
        optimiztion routines - nlm, optim
        optim(100000, nLL, method = "BFGS", x = pp) -> minimize -ve log likelihood
- warnings() - display warnings
- browser() - suspend execution so user can browse local environment
- recover() - suspend execution of a function in one location but then browse a previous function

## Combinations and samples
- choose(n,k) - to select k out of n 
- combn(items,k) - combination of n items taken k at a time
- to select random numbers - 
        - runif(1, min=-1, max=100)
        - rnorm(1, mean=10, sd=10)
        - rbinom(1, size=10, prob=0.5)
        - rpois(1, lambda=10)
        - rexp(1, rate=0.1)
        - rgamma(1, shape=2, rate=0.1)
- set.seed(1) 
- sample(vector, n) - generate a sample of n elements
- sample(set, n, replace=TRUE) - generate a random sequence from given set
- sample(vector) - provides permutations

## Probability Distributions for Discrete Variable
- dbinom(7, size=10, prob=0.5) simple probability
- pbinom(7, size=10, prob=0.5) cumulative probabiliy
        => for right tail - lower.tail = FALSE
- dgeom(x, prob)
- dpois(x, lambda)

## Probability Distribution for Continous Variables
- pnorm(66, mean, sd)

## Probability to Quantiles
- qnorm(0.025)
- qbinom(p, size, prob)
- qgeom(p, prob)
- qpois(p, lambda)
- others - qt, qexp, qgamma, qchisq

## Plotting Graphs
- plot(x, dnorm(x))
- plot(x, dunif(x,min=2,max=4), main="title",type='l', lty="twodash", ylim=ylim, ylab="y axis title", xlab="x axis title")
- hist, bosxplot, curve, qqnorm 
- low-level graphic functions - points, lines, abline, segments, polygon, text
- plot(Petal.Length, Petal.Width, pch=as.integer(Species))
- legend(x, y, labels)
- coplot(y ~ x | f) - conditioning plot
- confidence intervals in bar plots
>library(gplots)
> barplot2(x, plot.ci=TRUE, ci.l=lower, ci.u=upper, col=colors)
- par(mfrow=c(2,2))


## Regression Line
> m <- lm(y ~ x)
> plot(y ~ x)
> abline(m)

## PCA
- Principal component analysis is an unsupervised learning technique and it is used to reduce the dimension of the data with minimum loss of information
- prcmp(dataframe, scale)
- without prcmp
        matrix = matrix(C(x,y,z)) where x=csv$col_name-mean(x)/sd(x)
        > m = cov(matrix_form)
        > eigenV = eigen(m)

## Eigen values
- e<-eigen(A)



->environments, null hypothesis to testing two samples for same distribution (9.5 to 9.20)