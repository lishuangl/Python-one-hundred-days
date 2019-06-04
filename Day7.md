
# Learing python data structure

- - -
Practice project

- Print cycle string
- Print verification code
- Find specific element
- Find max and min number
- Calculate day
- Print yanhui triangle
- Select double color balls
- Joseph ring

## Practice


```python
import random

def pr_cy():
    x=input('Please input a string :')
    t=1
    while t<10:
        x=x[1:]+x[0]
        print(x)
        t+=1
    
def pr_ve():
    x=int(input('Please input a number :'))
    y='0123456789qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM'
    for i in range(0,x):
        for j in range(0,4):
            z=random.randint(0,62)
            code=y[z]
            print(code,end='')
        print('')
        
def fi_sp():
    x=input('Please in put what you want element you want find : ')
    y='0123456789qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM'
    print(y.find(x))
    
def fi_ma():
    x=input('Please input a number list :')
    min = 9
    max = 0
    y = len(x)
    for i in range(0,y):
        t=int(x[i])
        if t < min:
            min = t
        if t> max:
            max = t
    print('min = ',min,' max = ',max)
    
def ca_da():
    x = int(input('Please input year : '))
    y = int(input('Please input month : '))
    z = int(input('Please input day : '))
    day = 0
    for i in range(x+1,2018):
        if i % 4 == 0 and i % 100 !=0 or i %400 ==0:
            day += 366
        else:
            day += 365
    a = [31,28,31,30,31,30,31,31,30,31,30,31]
    b = [31,29,31,30,31,30,31,31,30,31,30,31]
    if x % 4 == 0 and x % 100 !=0 or x %400 ==0:
        for j in range(y,12):
            day += b[j]
        day += b[y-1]-z
    else:
        for j in range(y,12):
            day += a[j]
        day += a[y-1]-z
    day += 184
    print(day)
    
def pr_ya():
    x=int(input('Please input a number : '))
    a=[[]]*x
    for i in range(0,x):
        a[i]=[None]*(i+1)  #give initial values
        print('  '*(x-i),end='')
        for j in range(0,i+1):
            if j == 0 or j == i:
                a[i][j]=1
            else:
                a[i][j]=a[i-1][j-1]+a[i-1][j]
            print(a[i][j],end='   ')
        print()

def se_do():
    x = int(input('Please input a number : '))
    for i in range(x):
        y = random.sample(range(1,34),6)
        z = random.randint(1,16)
        for i in range(6):
            print('%02d'%y[i],end=' ')
        print(' | ','%02d'%z)
            
def jo_ri():
    x=int(input('Please input the long ring : '))
    y=int(input('Please input a number : '))
    z=int(input('Where to start : '))
    w=int(input('Where to end : '))
    a=[True]*x
    b = 0
    c = 0
    e = z-1
    while b < w:
        if a[e]:
            c += 1
            if c == y:
                a[e] = False
                c = 0
                b += 1
        e += 1
        e %= x #promise it not more x
    print(a)
        

        
if __name__=='__main__':
    pr_cy()
    pr_ve()
    fi_sp()
    fi_ma()
    ca_da()
    pr_ya()
    se_do()
    jo_ri()
```

    Please input a string :abcdef
    bcdefa
    cdefab
    defabc
    efabcd
    fabcde
    abcdef
    bcdefa
    cdefab
    defabc
    Please input a number :5
    RB3G
    62j4
    2BA4
    XQTB
    nBia
    Please in put what you want element you want find : e
    12
    Please input a number list :24856
    min =  2  max =  8
    Please input year : 1998
    Please input month : 5
    Please input day : 3
    7366
    Please input a number : 5
              1   
            1   1   
          1   2   1   
        1   3   3   1   
      1   4   6   4   1   
    Please input a number : 30
    07 23 21 22 13 20  |  14
    18 33 08 16 04 32  |  09
    32 27 13 18 17 24  |  05
    06 07 21 20 16 25  |  12
    28 16 07 22 20 24  |  01
    13 02 07 18 12 27  |  14
    23 08 07 19 05 09  |  03
    18 17 31 23 09 33  |  05
    28 16 02 06 14 20  |  12
    21 23 07 18 01 31  |  01
    15 30 03 10 32 16  |  12
    14 15 26 17 24 29  |  10
    20 09 05 24 08 32  |  04
    31 02 19 01 20 25  |  11
    08 19 07 30 09 18  |  16
    10 29 26 33 19 21  |  15
    28 21 06 17 16 15  |  09
    24 30 33 08 28 20  |  06
    12 14 31 24 01 26  |  12
    11 18 14 22 16 26  |  08
    19 08 04 18 16 02  |  15
    08 18 01 23 06 04  |  15
    04 12 25 05 13 09  |  10
    25 26 10 15 32 22  |  08
    26 20 30 10 14 25  |  12
    09 05 30 11 21 27  |  02
    17 26 33 14 09 31  |  03
    32 16 11 06 03 09  |  11
    04 21 26 07 12 03  |  11
    07 12 15 09 20 03  |  07
    Please input the long ring : 30
    Please input a number : 5
    Where to start : 3
    Where to end : 10
    [True, False, True, True, True, True, False, False, True, True, True, False, True, False, True, True, False, True, True, False, True, False, True, True, True, False, False, True, True, True]
    
