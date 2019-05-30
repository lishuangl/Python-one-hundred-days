
<font face="Times new roman" > 

# Learning python basic grammar

Three project :
- The temperature transformation
- Calculate circle perimeter and area
- Judge leap year

Some tips :

- All the input are string type , it need to tranfer float or double
- Control print type need to use % to control

## Practice
</font>


```python
import math

def tem_tran():
    x=input('Please input celsius :')
    x=float(x)
    y=1.8*x+32
    print(y,'F')

def cir_cal():
    x=float(input('Please input radius :'))
    y=2*math.pi*x
    z=math.pi*x**2
    print('perimeter: %.2f'%y,'area: %.2f'%z)

def ju_le():
    x=int(input('Please input year :'))
    if (x % 4 == 0 and x % 100 != 0 or x %400 == 0):
        print('Is leap year')
    else:
        print('Not leap year')
    
tem_tran()
cir_cal()
ju_le()
```

    Please input celsius :32
    89.6 F
    Please input radius :2
    perimeter: 12.57 area: 12.57
    Please input year :2019
    Not leap year



