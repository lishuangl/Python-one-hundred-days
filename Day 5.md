
# Day1 and day4 review

Practice project:

- Money buy chicken
- Gambling in casino
- Print fibonacci sequence
- Guess number
- Print narcissistic number
- Print palindrome number
- Print perfect number
- Print prime number
- Print multiplication table

## Practice


```python
import random

def mo_by():
    x=int(input('Please input your money : '))
    y=int(input('Please input your demand : '))
    t=0
    for i in range(0,y):
        for j in range(0,y):
            for k in range(0,y):
                if(5*i+3*j+k==x and t < 5):
                    print('Big chicken : ',i,'Middle chicken ：',j,'Small chicken :',k)
                    t=t+1

def ga_ca():
    x=int(input('Please input your money : '))
    t=0
    while x > 0 :
        t=t+1
        y1=random.randint(1,7)+random.randint(1,7)
        if y1 == (7 or 11):  #win
            x = x + 100
        elif y1 == (2 or 3 or 12):
            x = x - 100
        else:
            z = 0
            while z == 0:
                y=random.randint(1,7)+random.randint(1,7)
                if y == y1:
                    x = x +100
                    z = 1
                elif y == 7:
                    x = x - 100
                    z = 1
                else:
                    z =0
        #print(t,x)
    print('You have play ',t,'to lose all your money')

def pr_fi():
    x=int(input('Please input long sequence : '))
    a ,b = 0 ,1
    for i in range (0,x):
        c = a
        a = b
        b = a + c
        print(a,' ',end='')
        
def gu_nu():
    y = random.randint(0,100)
    x = 0
    t = 0
    while x != y:
        t = t + 1
        x = int(input('Please input your guess bumber :'))
        if x > y :
            print('Above the exact number.')
        elif x < y:
            print('Below the exact number.')
        else :
            print('You have guess ',t,'times')

def pr_na():
    x = int(input('Please input a number : '))
    print('Narcissistic number : ',end='')
    for i in range(1,x+1):
        a=i
        sum=0
        for j in range(1,5):
            z=a % 10
            sum = sum + z**3
            a=a//10
        if sum == i:
            print(i,' ',end='')
            
def pr_pa():
    x=int(input('Please input a number : '))
    y=x
    z=0
    while y>0:
        t=y%10
        z=z*10+t
        y=y//10
    if z == x:
        print('This is palindrome number.')
    else :
        print('This is not palindrome number.')

def pr_pe():
    x=int(input('Please input a number : '))
    print('This is perfect number : ',end='')
    for i in range (1,x+1):
        sum = 0
        for j in range(1,i):
            if i % j ==0:
                sum+=j
        if sum == i:
            print(i,' ',end='')

def pr_pr():
    x=int(input('Please input a number : '))
    print('Prime number is : ',end='')
    for i in range(2,x+1):
        y=0  #more important and must inside to do
        for j in range(2,i):
            if i % j == 0:
                y = 1
                break
        if y==0:
            print(i,' ',end='')
            
def pr_mu():
    x=int(input('Please input a number : '))
    for i in range(1,x+1):
        for j in range(1,i+1):
            print(j,'*',i,'=',i*j,'  ',end='')
        print()

mo_by()
ga_ca()
pr_fi()
gu_nu()
pr_na()
pr_pa()
pr_pe()
pr_pr()
pr_mu()
```

    Please input your money : 100
    Please input your demand : 100
    Big chicken :  0 Middle chicken ： 1 Small chicken : 97
    Big chicken :  0 Middle chicken ： 2 Small chicken : 94
    Big chicken :  0 Middle chicken ： 3 Small chicken : 91
    Big chicken :  0 Middle chicken ： 4 Small chicken : 88
    Big chicken :  0 Middle chicken ： 5 Small chicken : 85
    Please input your money : 300
    You have play  19 to lose all your money
    Please input long sequence : 20
    1  1  2  3  5  8  13  21  34  55  89  144  233  377  610  987  1597  2584  4181  6765  Please input your guess bumber :55
    Below the exact number.
    Please input your guess bumber :80
    Below the exact number.
    Please input your guess bumber :90
    You have guess  3 times
    Please input a number : 10000
    Narcissistic number : 1  153  370  371  407  Please input a number : 121
    This is palindrome number.
    Please input a number : 100
    This is perfect number : 6  28  Please input a number : 200
    Prime number is : 2  3  5  7  11  13  17  19  23  29  31  37  41  43  47  53  59  61  67  71  73  79  83  89  97  101  103  107  109  113  127  131  137  139  149  151  157  163  167  173  179  181  191  193  197  199  Please input a number : 9
    1 * 1 = 1   
    1 * 2 = 2   2 * 2 = 4   
    1 * 3 = 3   2 * 3 = 6   3 * 3 = 9   
    1 * 4 = 4   2 * 4 = 8   3 * 4 = 12   4 * 4 = 16   
    1 * 5 = 5   2 * 5 = 10   3 * 5 = 15   4 * 5 = 20   5 * 5 = 25   
    1 * 6 = 6   2 * 6 = 12   3 * 6 = 18   4 * 6 = 24   5 * 6 = 30   6 * 6 = 36   
    1 * 7 = 7   2 * 7 = 14   3 * 7 = 21   4 * 7 = 28   5 * 7 = 35   6 * 7 = 42   7 * 7 = 49   
    1 * 8 = 8   2 * 8 = 16   3 * 8 = 24   4 * 8 = 32   5 * 8 = 40   6 * 8 = 48   7 * 8 = 56   8 * 8 = 64   
    1 * 9 = 9   2 * 9 = 18   3 * 9 = 27   4 * 9 = 36   5 * 9 = 45   6 * 9 = 54   7 * 9 = 63   8 * 9 = 72   9 * 9 = 81   
    
