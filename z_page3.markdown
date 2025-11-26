---
layout: page
title: cas
permalink: /cas/
---

<h1> SageMath </h1>

To install the SageMath software, visit the <a href="https://doc.sagemath.org/html/en/installation/index.html" target="_blank"> installation guide</a> or use the <a href="https://sagecell.sagemath.org/" target="_blank">sage cell server</a>. For a comprehensive tutorial, visit <a href="https://doc.sagemath.org/html/en/tutorial/" target="_blank"> docs.sagemath.org</a>. 

<p align="center"><img src="../img/site/mvc.png" border="0"> </p>

<center> <iframe src="../sage/index.html" width="100%" border="0"> </iframe> </center>

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


<br> <br>

<h1> Wolfram Mathematica </h1>
<details>

<summary> <strong>Wolfram Mathematica Labs for Single and Multivariable Calculus</strong></summary> <br>
[Originally created with <a href="https://www.wolfram.com/mathematica/" target="_blank">Mathematica 8.0</a>]  * denotes AP Calculus BC only <br>
<p align="center"><img src="../img/site/koch.png" border="0"> </p>

01:  Investigating Limits 
<a href="../docs/labs/calculus/01_Limits.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/01_Limits.nb" target="_blank">[  .nb  ]</a><br>
02:  Rates of Change
<a href="../docs/labs/calculus/02_Rates_of_change.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/02_Rates_of_change.nb" target="_blank">[  .nb  ]</a><br>
03:  The Derivative 
<a href="../docs/labs/calculus/03_The_Derivative.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/03_The_Derivative.nb" target="_blank">[  .nb  ]</a><br>
04:  Derivatives Graphically
<a href="../docs/labs/calculus/04_Derivatives_Graphically.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/04_Derivatives_Graphically.nb" target="_blank">[  .nb  ]</a><br>
05:  Higher Derivatives
<a href="../docs/labs/calculus/05_Higher_Derivatives.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/05_Higher_Derivatives.nb" target="_blank">[  .nb  ]</a><br>
06:  Extrema
<a href="../docs/labs/calculus/06_Extrema.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/06_Extrema.nb" target="_blank">[  .nb  ]</a><br>
07:  Inflection Points
<a href="../docs/labs/calculus/07_Inflection_Points.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/07_Inflection_Points.pdf" target="_blank">[  .nb  ]</a><br>
08:  Implicit Differentiation
<a href="../docs/labs/calculus/08_Implicit_Differentiation.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/08_Implicit_Differentiation.nb" target="_blank">[  .nb  ]</a><br>
09:  Differential Equations
<a href="../docs/labs/calculus/09_Differential_Equations.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/09_Differential_Equations.nb" target="_blank">[  .nb  ]</a><br>
10:  Integrals
<a href="../docs/labs/calculus/10_Integrals.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/10_Integrals.nb" target="_blank">[  .nb  ]</a><br>
11: Riemann Sums
<a href="../docs/labs/calculus/11_Riemann_Sums.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/11_Riemann_Sums.nb" target="_blank">[  .nb  ]</a><br>
12: Improper Integrals*
<a href="../docs/labs/calculus/12_Improper_Integrals.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/12_Improper_Integrals.nb" target="_blank">[  .nb  ]</a><br>
13: Accumulating Functions
<a href="../docs/labs/calculus/13_Accumulating_Functions.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/13_Accumulating_Functions.nb" target="_blank">[  .nb  ]</a><br>
14: Sequences and Series*
<a href="../docs/labs/calculus/14_Sequences_and_Series.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/14_Sequences_and_Series.nb" target="_blank">[  .nb  ]</a><br>
15: Dot Product<a href="../docs/labs/calculus/15_Dot_Product.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/15_Dot_Product.nb" target="_blank">[  .nb  ]</a><br>
16: Cross Product
<a href="../docs/labs/calculus/16_Cross_Product.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/16_Cross_Product.nb" target="_blank">[  .nb  ]</a><br>
17: Lines and Planes
<a href="../docs/labs/calculus/17_Lines_Planes.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/17_Lines_Planes.nb" target="_blank">[  .nb  ]</a><br>
18: Curvature, T(t),N(t), B(t)
<a href="../docs/labs/calculus/18_Curvature_TNB.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/18_Curvature_TNB.nb" target="_blank">[  .nb  ]</a><br>
19: Multivariable Functions
<a href="../docs/labs/calculus/19_Multivariable_Functions.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/19_Multivariable_Functions.nb" target="_blank">[  .nb  ]</a><br>
20: Partial Derivatives
<a href="../docs/labs/calculus/20_Partial_Derivatives.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/20_Partial_Derivatives.nb" target="_blank">[  .nb  ]</a><br>
21: The Chain Rule
<a href="../docs/labs/calculus/21_Chain_Rule.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/21_Chain_Rule.nb" target="_blank">[  .nb  ]</a><br>
22: The Gradient
<a href="../docs/labs/calculus/22_Gradient.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/22_Gradient.nb" target="_blank">[  .nb  ]</a><br>
23: Lagrange Multiplier
<a href="../docs/labs/calculus/23_Lagrange_Multiplier.pdf" target="_blank">[  .pdf  ]</a>
<a href="../docs/labs/calculus/23_Lagrange_Multiplier.nb" target="_blank">[  .nb  ]</a><br>
00: Taylor Series with Mathematica 
<a href="../docs/labs/calculus/Taylor-Series-Shubleka.nb.zip" target="_blank"> [ .zip ] </a> <br><br>
</details>

<details>
<summary> <strong> Interactive Demonstrations: Calculus Concepts </strong></summary> <br>
[ <a href="https://www.wolfram.com/cdf-player/" target="_blank">Download Mathematica Player (free)</a> ]

<table width="100%"  border="0">
        <tr valign="top">
          <td><a href="https://demonstrations.wolfram.com/TheTangentLineProblem/" target="_blank"><img src="https://demonstrations.wolfram.com/TheTangentLineProblem/thumbnail_174.jpg" border="0" alt="&quot;The Tangent Line Problem&quot; from the Wolfram Demonstrations Project" title="&quot;The Tangent Line Problem&quot; from the Wolfram Demonstrations Project" /></a><strong><br>
          The Tangent Problem</strong></td>
          <td><a href="https://demonstrations.wolfram.com/TheQuotientRule/" target="_blank"><img src="https://demonstrations.wolfram.com/TheQuotientRule/thumbnail_174.jpg" border="0" alt="&quot;The Quotient Rule&quot; from the Wolfram Demonstrations Project" title="&quot;The Quotient Rule&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>The Quotient Rule</strong></td>
          <td><a href="https://demonstrations.wolfram.com/Discontinuity/" target="_blank"><img src="https://demonstrations.wolfram.com/Discontinuity/thumbnail_174.jpg" border="0" alt="&quot;Discontinuity&quot; from the Wolfram Demonstrations Project" title="&quot;Discontinuity&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Discontinuity</strong></td>
        </tr>
        <tr valign="top">
          <td>
        <p align="left"><strong><strong><a href="https://demonstrations.wolfram.com/MeanValueTheorem/" target="_blank"><img src="https://demonstrations.wolfram.com/MeanValueTheorem/thumbnail_174.jpg" border="0" alt="&quot;Mean Value Theorem&quot; from the Wolfram Demonstrations Project" title="&quot;Mean Value Theorem&quot; from the Wolfram Demonstrations Project" /></a> <br>
          Mean Value Theorem</strong></strong></p></td>
          <td><p align="left"><strong><a href="https://demonstrations.wolfram.com/SqueezeTheorem/" target="_blank"><img src="https://demonstrations.wolfram.com/SqueezeTheorem/thumbnail_174.jpg" border="0" alt="&quot;Squeeze Theorem&quot; from the Wolfram Demonstrations Project" title="&quot;Squeeze Theorem&quot; from the Wolfram Demonstrations Project"/></a><br>
          Squeeze Theorem
            </strong></p>
          </td>
          <td><strong><a href="https://demonstrations.wolfram.com/TheFundamentalTheoremOfCalculus/" target="_blank"><img src="https://demonstrations.wolfram.com/TheFundamentalTheoremOfCalculus/thumbnail_174.jpg" border="0" alt="&quot;The Fundamental Theorem of Calculus&quot; from the Wolfram Demonstrations Project" title="&quot;The Fundamental Theorem of Calculus&quot; from the Wolfram Demonstrations Project" /></a><br>
          The Fundamental Theorem of Calculus</strong></td>
        </tr>
        <tr valign="top">
          <td><strong><a href="https://demonstrations.wolfram.com/AverageValueOfAFunction/" target="_blank"><img src="https://demonstrations.wolfram.com/AverageValueOfAFunction/thumbnail_174.jpg" border="0" alt="&quot;Average Value of a Function&quot; from the Wolfram Demonstrations Project" title="&quot;Average Value of a Function&quot; from the Wolfram Demonstrations Project" /></a><br>
          Average Value of a Function</strong></td>
          <td><a href="https://demonstrations.wolfram.com/ExtremeValueTheorem/" target="_blank"><img src="https://demonstrations.wolfram.com/ExtremeValueTheorem/thumbnail_174.jpg" border="0" alt="&quot;Extreme Value Theorem&quot; from the Wolfram Demonstrations Project" title="&quot;Extreme Value Theorem&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Extreme Value Theorem</strong></td>
          <td><a href="https://demonstrations.wolfram.com/IntegralMeanValueTheorem/" target="_blank"><img src="https://demonstrations.wolfram.com/IntegralMeanValueTheorem/thumbnail_174.jpg" border="0" alt="&quot;Integral Mean Value Theorem&quot; from the Wolfram Demonstrations Project" title="&quot;Integral Mean Value Theorem&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Integral Mean Value Theorem</strong></td>
        </tr>
        <tr valign="top">
          <td><a href="https://demonstrations.wolfram.com/IntermediateValueTheorem/" target="_blank"><img src="https://demonstrations.wolfram.com/IntermediateValueTheorem/thumbnail_174.jpg" border="0" alt="&quot;Intermediate Value Theorem&quot; from the Wolfram Demonstrations Project" title="&quot;Intermediate Value Theorem&quot; from the Wolfram Demonstrations Project" /></a><br> <strong>Intermediate Value Theorem</strong></td>
          <td><a href="https://demonstrations.wolfram.com/IntegrationByRiemannSums/" target="_blank"><img src="https://demonstrations.wolfram.com/IntegrationByRiemannSums/thumbnail_174.jpg" border="0" alt="&quot;Integration by Riemann Sums&quot; from the Wolfram Demonstrations Project" title="&quot;Integration by Riemann Sums&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Riemann Sums: Integration</strong></td>
          <td><a href="https://demonstrations.wolfram.com/AreaBetweenCurves/" target="_blank"><img src="https://demonstrations.wolfram.com/AreaBetweenCurves/thumbnail_174.jpg" border="0" alt="&quot;Area Between Curves&quot; from the Wolfram Demonstrations Project" title="&quot;Area Between Curves&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Area Between Curves</strong></td>
        </tr>
        <tr valign="top">
          <td><a href="https://demonstrations.wolfram.com/VolumesUsingTheDiscMethod/" target="_blank"><img src="https://demonstrations.wolfram.com/VolumesUsingTheDiscMethod/thumbnail_174.jpg" border="0" alt="&quot;Volumes Using the Disc Method&quot; from the Wolfram Demonstrations Project" title="&quot;Volumes Using the Disc Method&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Disk Method</strong></td>
          <td><a href="https://demonstrations.wolfram.com/SolidsOfKnownCrossSection/" target="_blank"><img src="https://demonstrations.wolfram.com/SolidsOfKnownCrossSection/thumbnail_174.jpg" border="0" alt="&quot;Solids of Known Cross Section&quot; from the Wolfram Demonstrations Project" title="&quot;Solids of Known Cross Section&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Solids of Known Cross Sections</strong></td>
          <td><a href="https://demonstrations.wolfram.com/VolumesOfRevolutionUsingCylindricalShells/" target="_blank"><img src="https://demonstrations.wolfram.com/VolumesOfRevolutionUsingCylindricalShells/thumbnail_174.jpg" border="0" alt="&quot;Volumes of Revolution Using Cylindrical Shells&quot; from the Wolfram Demonstrations Project" title="&quot;Volumes of Revolution Using Cylindrical Shells&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Shell Method</strong></td>
        </tr>
        <tr valign="top">
          <td><a href="https://demonstrations.wolfram.com/PlotOfAGeometricSequenceAndItsPartialSums/" target="_blank"><img src="https://demonstrations.wolfram.com/PlotOfAGeometricSequenceAndItsPartialSums/thumbnail_174.jpg" border="0" alt="&quot;Plot of a Geometric Sequence and Its Partial Sums&quot; from the Wolfram Demonstrations Project" title="&quot;Plot of a Geometric Sequence and Its Partial Sums&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Geometric Sequence</strong></td>
          <td><a href="https://demonstrations.wolfram.com/GraphsOfTaylorPolynomials/" target="_blank"><img src="https://demonstrations.wolfram.com/GraphsOfTaylorPolynomials/thumbnail_174.jpg" border="0" alt="&quot;Graphs of Taylor Polynomials&quot; from the Wolfram Demonstrations Project" title="&quot;Graphs of Taylor Polynomials&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>Taylor Polynomials</strong></td>
          <td><a href="https://demonstrations.wolfram.com/LHospitalsRuleFor00Forms/" target="_blank"><img src="https://demonstrations.wolfram.com/LHospitalsRuleFor00Forms/thumbnail_174.jpg" border="0" alt="&quot;L'Hospital's Rule for 0/0 Forms&quot; from the Wolfram Demonstrations Project" title="&quot;L'Hospital's Rule for 0/0 Forms&quot; from the Wolfram Demonstrations Project" /></a><br>
            <strong>L'Hopital's Rule 0/0</strong></td>
        </tr>
  
</table>
</details>