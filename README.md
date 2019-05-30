# Day1--5.28

## Turtle learning

<font face="Times new roman" > 
  
Graphics base：turtle    
Main usage：painting   
Some tips:  

- use dir(third base) can get all function in third base
- use help(third base) can get the introduction to third base
- use help(third base.function)can get the use of function

For example:   

- dir(turtle)
- help(turtle)
- help(turtle.back)
         

Practice project:one pig who name is peiqi
</font>

### Turtle Function

<font face="Times new roman" >

1. pensize(1-10) : the pen size  

2. hideturtle(): hide the pen  

3. colormode(1 or 255) : select mode of color divide 1 or 255 in r,g,b the three basic color  

4. color('type' or 'number-r,g,b') : which can use two style and can mix with two color  

5. setup(width = ,height = ,startx = ,starty = ) : set canvas size and the pen where to start  

6. speed(0-10) : from 1 to 10 begin very fast and 0 is the fastest  

7. penup() | pu  | up : all represent no drawing when pen start to move  

8. pendown() | pd  | down : all represent put the pen down in canvas  

9. setpos(x,y) | setpostion | goto : get the pen to specific location x and y both are number  

10. setheading(angle) | seth : to adjust the angle of pen  

11. begin_fill() | end_fill : fill the color in painting  

12. left(angle) | lf : left some angle while painting  

13. forward(number) | fd : move pen forward some distance  

14. circle(r,angle,step） :  to painting circle 'r' is radius 'angle' is circle length 'step' is calculate numbers  

    </font>

### Turtle steps

<font face="Times new roman" > 
  
first：set pensize | canvas size | speed | colormode before color  
second: penup | pendown | setpostion  
third: setheading | left | forward | circle | begin_fill | begin_end  
four: mainloop
</font>
