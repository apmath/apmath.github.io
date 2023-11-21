---
layout: page
title: sagemath
permalink: /sage/
---

On this page you'll find a few examples of sagemath. To install the SageMath software, visit the <a href="https://doc.sagemath.org/html/en/installation/index.html" target="_blank"> installation guide</a> or use the <a href="https://sagecell.sagemath.org/" target="_blank">sage cell server</a>. For a comprehensive tutorial, visit <a href="https://doc.sagemath.org/html/en/tutorial/" target="_blank"> docs.sagemath.org</a>. 

# basic functions

```python

# define a variable named x
x = var('x')

# define a function f(x)
f(x)=sin(x)

# evaluate f(x) at x=1 and store to a variable y
y = f(1)

# get a numerical approximation of y
n(y)

# plot f(x) over a given interval
plot(f(x), (x, -2*pi, 2*pi))

# plot two functions
plot((e^x, 4-x^2), (x, -3, 2))

# partial fractions
f = 1/(x^2-3*x+2)
f.partial_fraction(x)

``` 


# solving equations

```python

# declare a variable x and solve a quadratic equation x^2++5x+6=0
x = var('x')
solve(x^2 + 5*x + 6, x)


# solving the quadratic equation
a, b, c, x = var('a b c x')
solve([a*x^2 + b*x + c == 0],x)

# solving a system of two linear equations
x, y = var('x, y')
solve([2*x+y==6, 3*x-y==4], x, y)



``` 


# parametric and 3d plotting

```python

# parametric plot of the unit circle: <x(t), y(t)> = <cos(t), sin(t)>
t = var('t')
p = parametric_plot((cos(t),sin(t)),(t,0,2*pi),rgbcolor=hue(0.6))
# to add a title at a specific position (0.5, 1.1)
name = text("The Unit Circle", (0.5,1.1), rgbcolor=(1,0,0))
show(p+name)

# multiple parametric plots combined into 1 plotting window
t = var('t')
p1 = parametric_plot((sin(t),(sin(t))^2),(t,0,2*pi),rgbcolor=hue(0.2))
p2 = parametric_plot((cos(t),sin(t)^2),(t,0,2*pi),rgbcolor=hue(0.4))
p3 = parametric_plot((cos(t),sin(2*t)),(t,0,2*pi),rgbcolor=hue(0.6))
show(p1+p2+p3, axes=false)

# three-dimensional plot z = f(x, y)
x, y = var('x,y')
plot3d(x^2 + y^2, (x,-2,2), (y,-2,2))

# three-dimensional parametric plot z = f(x(u,v), y(u,v))
u, v = var('u, v')
f_x(u, v) = cos(u)
f_y(u, v) = sin(v)
f_z(u, v) = u^2 + u*v + v^2
parametric_plot3d([f_x, f_y, f_z], (u, -2, 2), (v, -2, 2))

# three-dimensional implicit plot: hyperboloid of one sheet
# x^2 + y^2 - z^2 = 1
x, y, z = var('x, y, z')
implicit_plot3d(x^2 + y^2 - z^2 - 1, (x,-3, 3), (y,-3, 3), (z,-3, 3))

```

# differentiation and integration

```python
# declare an independent variable t
t = var('t')

# differentiate an expression with respect to t
diff(sin(t) + e^(3*t), t)

# higher order derivative: the third derivative of cos(5x)
diff(cos(5*x), x, 3)

# partial differentiation
x, y = var('x,y')

# declare a function f in terms of x and y
f = 2*x^2 + 3*y^3

# differentiate f with respect to x
f.diff(x)

#differentiate f with respect to y
f.diff(y)

# an indefinite integral with respect to x
integral(x*sin(x^2), x)

# a definite integral with respect to x from x=-1 to 1
integral(1/(x^2+1), x, -1, 1)

```
