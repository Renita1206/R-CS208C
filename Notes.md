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








