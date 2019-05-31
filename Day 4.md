
# Learning python for and while statement

Practice project:

- Prime judge
- Find factor and multiple
- Print triangle

## Practice


```python
def pr_ju():
    x=int(input('Please input a number :'))
    if x == 2:
        print('Is prime number.')
    else :
        for i in range(2,x-1):
            if(x % i == 0):
                t=1
                break
            else:
                t=0
        if t==1:
            print('Not prime number.')
        else:
            print('Is prime number.')

def fa_mu():
    x=int(input('Please input first number : '))
    y=int(input('Please input second number : '))
    for i in range(x,0,-1):
        if x %i ==0 and y %i ==0:
            print('factor :',i)
            print('multiple :',x * y // i)
            break
    
def pr_tr():
    x=int(input('Please input a number : '))
    for i in range(0,x):
        print(' '*2*(x-i),end='')
        for j in range(0,2*i+1):
            print('*',end=' ')
        print()

pr_ju()
fa_mu()
pr_tr()
```

    Please input a number :10
    Not prime number.
    Please input first number : 12
    Please input second number : 10
    factor : 2
    multiple : 60
    Please input a number : 5
              * 
            * * * 
          * * * * * 
        * * * * * * * 
      * * * * * * * * * 
    
