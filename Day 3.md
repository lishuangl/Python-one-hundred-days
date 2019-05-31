
<font face="Times new roman" > 
    
# Learning python if statement

Pactice project :

- Centimeter and inch transfer
- Use randint to express dice
- Grade and level transfer
- Calulate triangle perimeter and area
- Count individual income tax

## Pactice

</font>


```python
import math
import random

def cm_in():
    x=input('Please input length type : ')
    y=float(input('Please input number : '))
    if (x=='cm'):
        z=y/2.54
        print('%.1f'%z,'in')
    else :
        z=2.54*y
        print('%.1f'%z,'cm')

def ra_di():
    x=random.randint(1,6)
    if x==(1 or 2 or 3):
        print('I love you')
    else:
        print('I hate you')

def gr_tr():
    x=float(input('Please input '))
    if x >=90:
        print('A')
    elif x>=80 and x<90:
        print('B')
    elif x>=70 and x<80:
        print('C')
    else:
        print('D')
    
def ca_tr():
    x=float(input('side 1 ：'))
    y=float(input('side 2 ：'))
    z=float(input('side 3 ：'))
    if x+y>z and x+z>y and y+z>x:
        print('This is a triangle.')
        a=x+y+z
        p=0.5*(x+y+z)
        b=math.sqrt(p*(p-x)*(p-y)*(p-z))
        print('perimeter : %.1f'%a,'area : %.2f'%b)
    else:
        print('This is not a triangle')

def in_tax():
    x=int(input('Please input individual income :'))
    if x<5000:
        y=x
    elif x<8000:
        y=5000+0.97*(8000-x)
    elif x<17000:
        y=5000+0.97*3000+0.9*(17000-x)
    elif x<30000:
        y=5000+0.97*3000+0.9*9000+0.8*(30000-x)
    elif x<40000:
        y=5000+0.97*3000+0.9*9000+0.8*13000+0.75*(40000-x)
    elif x<60000:
        y=5000+0.97*3000+0.9*9000+0.8*13000+0.75*10000+0.7*(60000-x)
    elif x<85000:
        y=5000+0.97*3000+0.9*9000+0.8*13000+0.75*10000+0.7*20000+0.65*(85000-x)
    else:
        y=5000+0.97*3000+0.9*9000+0.8*13000+0.75*10000+0.7*20000+0.65*25000+0.55*(x-85000)
    print('real_income=%.2f'%y)
    
cm_in()
ra_di()
gr_tr()
ca_tr()
in_tax()
```

    Please input length type : cm
    Please input number : 10
    3.9 in
    I hate you
    Please input 99
    A
    side 1 ：12
    side 2 ：14
    side 3 ：16
    This is a triangle.
    perimeter : 42.0 area : 81.33
    Please input individual income :85200
    real_income=64270.00
    
