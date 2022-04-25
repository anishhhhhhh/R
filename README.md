# R

### `Aggregate`
data = data.frame (subjects = c("java", "python", "java", "java", "php", "php"),</br> 
id = c(1, 2, 3, 4, 5, 6), </br> 
names = c("manoj", "sai", "mounika", "durga", "deepika", "roshan"), </br> 
marks = c(89, 89, 76, 89, 90, 67))</br> 

print (data)</br> 
print (aggregate (data$marks, list (data$subjects), FUN=sum))</br> 
print (aggregate (data$marks, list (data$subjects), FUN=min))</br> 
print (aggregate (data$marks, list (data$subjects), FUN=max))</br> 

### `Factorial`
n =as.integer(readline(prompt = "Input : "))</br> 

fact=1</br> 

if(n<0){</br> 
    print("Fact of -ve does not exist")</br> 
}else if(n==0){</br> 
    print(0)</br> 
}else{</br> 
    for(i in 1:n){</br> 
      fact=fact*i</br> 
    }</br> 
}</br> 

print(fact)</br> 

### `Fibo With Recursion`
n=as.integer(readline(prompt = "Input : "))</br>
fibo <- function(n){</br>
  if(n<=1){</br>
    return(n)</br>
  }else{</br>
    return(fibo(n-1)+fibo(n-2))</br>
  }</br>
}</br>
if(n<=0){</br>
  print("Invalid Input")</br>
}else{</br>
  print("Fibonacci Series")</br>
  for(i in 0:(n-1)){</br>
    print(fibo(i))</br>
  }</br>
}</br>

### `Exp 8`
values=iris</br>

minn=min(values$Sepal.Length)</br>
print(minn)</br>

maxx=max(values$Sepal.Length)</br>
print(maxx)</br>

r=range(values$Sepal.Length)</br>
print(r)</br>

mean=mean(values$Sepal.Length)</br>
print(mean)</br>

median=median(values$Sepal.Length)</br>
print(median)</br>

q= quantile(values$Sepal.Length)</br>
print(q)</br>

q1=quantile(values$Sepal.Length, 0.25)</br>
print(q1)</br>

sd=sd(values$Sepal.Length)</br>
print(sd)</br>

variance = var(values$Sepal.Length)</br>
print(variance)</br>

iqr=IQR(values$Sepal.Length)</br>
print(iqr)</br>

s=summary(values)</br>
print(s)</br>

vect= c(12,4,10,9,3,8,20,18,24)</br>
hist(vect)</br>
hist(vect, col="blue",border="Green")</br>

plot(vect)</br>
plot(vect,type="o")</br>

### `Calculator`
add <- function(x,y){</br>
  return(x+y)</br>
}</br>

subtract <- function(x,y){</br>
  return(x-y)</br>
}</br>

multiply <- function(x,y){</br>
  return(xy)</br>
}</br>

divide <- function(x,y){</br>
  return(x/y)</br>
}</br>

print("Select Operation")</br>
print("1.Addition 2.Subtract 3.Multiplication 4.Division")</br>

choice=as.integer(readline(prompt = "Enter Choice: "))</br>
x=as.integer(readline(prompt = "No 1: "))</br>
y=as.integer(readline(prompt = "No 2: "))</br>

operator <- switch(choice, "+", "-", "", "/")</br>
result <- switch(choice, add(x,y),subtract(x,y),multiply(x,y), divide(x,y))</br>
print(paste(x, operator,y,"=",result))</br>

### `Matrix Creation`

rows=as.integer(readline(prompt = "Enter number of rows: "))</br>
columns=as.integer(readline(prompt = "Enter number of columns: "))</br>

values=readline(prompt = "Enter numbers of matrix: ")</br>

values=strsplit(values," ")</br>
values=as.integer(values[[1]])</br>

vect=c(Values)</br>
print("Your Matrix")</br>
print(matrix(values, nrow=rows, ncol=columns))</br>

### `Armstrong`
n = as.integer(readline(prompt = "Input : "))</br>

sum = 0</br>
temp = n</br>

while(temp > 0){</br>
    digit = temp %% 10</br>
    sum = sum + (digit^3)</br>
    temp = floor(temp / 10)</br>
}</br>

if(n == sum){</br>
    print(paste(n, " is Armstrong"))</br>
}else{</br>
    print(paste(n, " is not Armstrong"))</br>
}</br>

### `Exp 7`

student_marks =c(12,88,77,90,67,58,95,81,70,85)</br>
names(student_marks)=c("Pratibha","Krutika","Pratibha","Purva","Siddhi","Jigna","Vinayak","Aditya","Shaan","Rahul")</br>

pie(student_marks, labels=names(student_marks),col="green",main="Pie Chart", radius=1,col.main="red")</br>

barplot(student_marks, xlab="Students", ylab="Marks", col="lightblue",col.axis="darkgreen",col.lab="black", border="black")</br>

boxplot(student_marks~names(student_marks))</br>
boxplot(student_marks, xlab="Box Plot", ylab="Age",col.axis = "darkgreen", col.lab = "darkgreen")</br>

hist(student_marks, main = "Histogram", xlab = "Marks", col.lab = "darkgreen", col.main = "darkgreen", col = "yellow")</br>

plot(student_marks, type= "o", col = "green", xlab = "Students", ylab = "Marks", main = "Line Graph")</br>
plot(x = student_marks, y= NULL, xlab = "Students", ylab = "Marks",main="ScatterPlot", col.lab = "darkgreen", col.main = "darkgreen", col.axis = "darkgreen")</br>
