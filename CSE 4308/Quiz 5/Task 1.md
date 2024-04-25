# Task 1 

## Question
| Class | A | B | C |
|-------|---|---|---|
| X     | 1 | 2 | 1 |
| X     | 2 | 1 | 2 |
| X     | 3 | 2 | 2 |
| X     | 1 | 3 | 3 |
| X     | 1 | 2 | 1 |
| Y     | 2 | 1 | 2 |
| Y     | 3 | 1 | 1 |
| Y     | 2 | 2 | 2 |
| Y     | 3 | 3 | 1 |
| Y     | 2 | 1 | 1 |

We want to build a decision tree that determines whether a certain pattern is of type X or type Y. The decision tree can only use tests that are based on attributes A, B, and C. Each attribute has 3 possible values: 1, 2, 3 (we do not apply any thresholding). We have the 10 training examples, shown on the table (each row corresponds to a training example). 
What is the information gain of each attribute at the root? 
Which attribute achieves the highest information gain at the root?

## Answer

Entropy before split,
x=5, y=5

H=(-5/10)log2(5/10)-(5/10)log2(5/10)=1

### Using A to split  
A=1
x=3, y=0

H{A1} = (-3/3)log2(3/3)-(0/3)log2(0/3) = 0

A=2
x=1, y=3 
H{A2} = (-1/4)log2(1/4)-(3/4)log2(3/4) = 0.8113

A=3
x=1, y=2
H{A3} = (-1/3)log2(1/3)-(2/3)log2(2/3) = 0.9183  

I{A} = H - (3/10) H{A1} - (4/10)H{A2} - (3/10)H{A3}  
I{A} = 0.4  

### Using B to split  
B=1  
x=1, y=3
H{B1} = (-1/4)log2(1/4)-(3/4)log2(3/4) = 0.8113  

B=2  
x=3, y=1  
H{B2} = (-3/4)log2(3/4)-(1/4)log2(1/4) = 0.8113  

B=3  
x=1, y=1  
H{B3}  = (-1/2)log2(1/2) - (1/2)log2(1/2) = 1 

I{B} = H - (4/10)H{B1} - (4/10)H{B2} - (2/10)H{B3} 
I{B} = 0.15096  

### Using C to split  

C=1  
x=2, y=3
H{C1} = (-2/5)log2(2/5)-(3/5)log2(3/5)
H{C1}=0.9709  

C=2  
x=2 y=2  
H{C2} = -(2/4)log2(4/4)-(2/4)log2(2/4) = 1  

C=3  
x=1, y=0  
H{C3} = -(1/1)log(1/1)-(0/1)log2(0/1) = 0  

I{C} = H-(5/10)H{C1} - (4/10)H{C2} - (1/10)H{C3}  
I{C} = 0.11455

So A is the best attribute