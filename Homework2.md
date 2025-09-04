## Question 1

Three ways to assign the value of 25 to y:
```R
y<-25
```
```R
y<<-25
```
```R
y=25
```

## Question 2
He said, “I’m Garth Marenghi. Author. Dreamweaver. Visionary. Plus actor.” In R including the quoation marks: 
```R
'He said, ”I’m Garth Marenghi. Author. Dreamweaver. Visionary. Plus actor.”'
#this works in R becuase of the curly quotes
```

## Question 3
He said, “I’m Garth Marenghi. Author\Dreamweaver\Visionary. Plus actor.” would be:

```R
'He said, “I’m Garth Marenghi. Author\\Dreamweaver\\Visionary. Plus actor.”'

#double blackslash to indicate one backslash. Includes the single "'" becuase of the curly quotation marks
```

## Question 4
```R
c(1,2,3)
```
or 
```R
x <- 1:3
print (x)
```

## Question 5
R calls mathematical functions like + and - operators. R calles sin() and c() functions. Finally, "<-" would be conisdered an assignmnet opperator. 

## Question 6
The difference between these two loops is that:
in the while() loop, the function happens until the condiiton expressed is true. Therefore, starting at 0, x+1 is evaluated until x is 3 and R returns the answer to that final evalauation: 3+1=4.
In the for() loop, the function is evaluated for each value in the vector provided, changing the value of y each time it evalutaes. When the loop is finished in returns the answer using the last value assigned to the varaiable: 3+1=4.

## Question 7
``` R
a<-3
b<-4
c<-sqrt(a^2+b^2)
print(c)
```

Output: 
[1] 5

## Question 8
```R
?sin
```

 ## Question 9
 Counter 2 works in this situation becuase the "<<-" assignment operator changes the assignment of "val" in the global environment. Therefore, unlike in counter 1, which states "val <- val + step" instead of "val <<- val + step", counter 2 acutally allows old_val to be evaluated as val+step instead of just step. By changing the meaning of val in the global environment, this is used to analyze and evaluate the expression despite what comes before the command. 

 ## Question 10 
 ```R
library(dplyr)

cars_summary <- cars %>%
  group_by(Make) %>%
  summarise(across(c(Volume,Weight,CO2), mean)) %>%  
  arrange(desc(Volume))

cars_summary
```

## Question 11
```R
fibonacci <- function () {
  x<-0
  y<-y
  function () {
     old_x <- x
     nextstep<-x+y
     x<<-y
     y<<-nextstep
     old_x
  }
}
fib_gen <- fibonacci()
sapply (1:7, function(x) fib_gen())
```
