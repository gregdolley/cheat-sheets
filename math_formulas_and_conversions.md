# Math Formulas & Conversions Cheat Sheet

This is a **WIP** and **not complete yet**...

## Equation Templates

<div style="text-align: justify">
The following sections contain formulas and/or equations for different mathematical constructs and how to convert from one type to another - such as how to go from this (center-point form  circle equation):
</div>

$$
\left(x - {h}\right)^2 + \left(y - {k}\right)^2 = {r}^2 \quad \begin{cases}
    \left(h,\space k\right)\text{= coordinates of the center of the circle}& \\
    {r}\text{ = circle's radius}
\end{cases}
$$

And convert it into standard polynomial form:

$$
ax^2+ay^2+bx+cy+d = 0 \quad \begin{cases}
    \text{where} \space a \ne 0
\end{cases}
$$

<div style="text-align: justify">
TODO: when using Latex math formulas that contain "\begin{cases}" and "\end{cases}" that are also embedded within a Markdown table layout - this seems to confuse Github's Markdown parser and it just displays the Latex code itself instead of the actual formatted math renderings. This bug doesn't exist in any of the VS Code Markdown viewer extensionas (at least the couple that I've used). Try another way of making the tables (perhaps plain embedded HTML) and see if Github's viewer renders things correctly.
</div>  

## Lines

|Type|Equation Form|Notes|
|:---|:---|:---|
|Slope intercept|$y = mx+b$|$\begin{cases}m = \text{slope}& \\b = \text{y-intercept of line over y-axis.}\end{cases}$|
|Standard|$ax+by = c$|$\begin{cases}a, b = \text{the (x,y) components (a=x,b=y) of the line's normal vector}\end{cases}$|
 

TODO: put conversion.

## Circles


|Type|Equation Form|Notes|
|:---|:---|:---|
|Center-point|$\left(x - {h}\right)^2 + \left(y - {k}\right)^2 = {r}^2$|$\begin{cases}\left(h,\space k\right)\text{= coordinates of the center of the circle (h = x, k = y)}& \\{r}\text{ = circle's radius}\end{cases}$|
|Standard|$ax^2+ay^2+bx+cy+d = 0$|$\begin{cases}\text{where} \space a = 1\end{cases}$|

In the case of a real circle (i.e. not an ellipse), the $a$ through $d$ coefficient terms would equal the following:

* a = 1
* b = $2h$
* c = $2k$
* d = $h^2+k^2-r^2$


## Ellipses

TODO...

## Parabolas

TODO...

## Hyperbolas

TODO...

## Conic Sections (non-Parabola/Hyperbola Conics)

TODO...

## Planes

TODO...

## Spheres

TODO...
