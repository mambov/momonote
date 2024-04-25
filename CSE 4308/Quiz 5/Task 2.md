# Task 2  
## Question

| Class | A  | B  | C  |
|-------|----|----|----|
| X     | 25 | 24 | 31 |
| X     | 22 | 14 | 24 |
| X     | 28 | 22 | 25 |
| X     | 24 | 13 | 30 |
| X     | 26 | 20 | 24 |
| Y     | 20 | 31 | 17 |
| Y     | 18 | 32 | 14 |
| Y     | 21 | 25 | 20 |
| Y     | 13 | 32 | 15 |
| Y     | 12 | 27 | 18 |

We want to build a decision tree (which thresholding) that determines whether a certain pattern is of type X or type Y. The decision tree can only use tests that are based on attributes A, B, and C. We have the 10 training examples, shown on the table (each row corresponds to a training example). Which attribute threshold combination achieves the highest information gain at the root? For each attribute try the thresholds of 15, 20 and 25.

## Answer  

Before split,  
x=5, y=5  
H = -(5/10)log2(5/10)-(5/10)log2(5/10)  

### Consider A, 15  
A<15, x=0, y=2
H{A<15} = -(0/2)log2(0/2)-(2/2)log2(2/2)=0

A>=15, x=5, y=3  
H{A>=15}=-(5/8)log2(5/8)-(3/8)log2(3/8)=0.9544  

I{A,15}=1-(2/10)(0)-(8/10)(0.9544) = 0.2365  

### Consider A, 20  
A<20, x=0, y=3  
H{A<20} = -(0/3)log2(0/3)-(3/3)log2(3/3)=0  

A>20, x=5, y=2  

H{A>=20}=-(5/7)log2(5/7)-(2/7)log2(2/7)=0.8631  

I{A,20} = 1-(3/10)(0) - (7/10)(0.8631) = 0.3958  

### Consider A, 25  
A<25, x=2, y=5  
H{A<25} = -(2/7)log2(2/7)-(5/7)log2(5/7)=0.8631  

A>=25, x=3, y=0  

H{A>=25}=-(3/3)log2(3/3)-(0/3)log2(0/3)=0  

I{A,25}=1-(7/10)(0.8631)-(3/10)(0)=0.3958  

### Consider B, 15  

B<15, x=2, y=0  
H{B<15} = -(2/2)log2(2/2)-(0/2)log2(0/2)=0  

B>=15, x=3, y=5  
H{B>=15} = - (3/8)log2(3/8)-(5/8)log2(5/8)=0.9544  

I{B, 15} = 1-(2/10)(0)-8/10(0.9544) = 0.2365  

### Consider B, 20  
B<20, x=2, y=0  
H{B<20} = 0  

B>=20, x=3, y=5  
H{B>=20} = 0.9544  
I{B,20} = 0.2365  

### Consider B, 25  
B<25, x=5, y=0  
H{B<25} = 0  
B>=25, x=0, y=5  
H{B>=25} = 0  

I{B,25} = 1-(5/10)(0)-(5/10)(0) = 1  

B with the threshold of 25, lies the highest possible information gain, and so is the best attribute.