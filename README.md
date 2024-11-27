# Program 1: Newton Raphson method

<br>

## Date: 

<br>

## Question:

<br>

   Find a positive real root of $$x^3$$ − 𝒙 − 𝟐 = 𝟎 using Newton-Raphson method.

<br>

## Aim:

<br>

   To find a positive real root of $$x^3$$ − 𝒙 − 𝟐 = 𝟎 by using Newton-Raphson method.

<br>

## Algorithm:

<br>

   Step 1: Define the function $$f(x) = x**3 - x - 2$$

<br>

   Step 2: Define the function $$f_1 = 3* x **2 - 1$$

<br>

   Step 3: Get the value of $$X_0\$$

<br>

   Step 4: for i = 1 to 9

$$
X_n = X_0 - \frac{f(X_0)}{f^1(X_0)}
$$

<br>

$$
X_0 = X_n
$$

   Step 5: Print the value of $$X_n$$

<br>

## Program:

<br>

```
def f(x):
 return x**3-x-2
def f1(x):
 return 3*x**2-1
xo=float (input ("Enter the initial approximation: "))
for i in range (1,10):
 xn=xo-f(xo)/f1(xo)
 xo=xn
print ("The approximate root using Newton-Raphson method is %.4f"%xn)
```

<br>

## Output:

<br>

Enter the initial approximation: 1

<br>

The approximate root using Newton-Raphson method is 1.5214

<br>

## Result:

<br>

The real root of the given non linear equation is obtained

<br>

# Program 2: Gauss-Seidal method

<br>

## Date:

<br>

## Question:

<br>

 Solve the system of equations $$𝟒𝒙 + 𝒚 + 𝒛 = 𝟏; 𝒙 + 𝟑𝒚 + 𝒛 = 𝟐; 𝒙 + 𝒚 + 𝟓𝒛 = 𝟑,$$ using Gauss-Seidal method.

<br>

## Aim:

<br>

 To find the solution of given system of equations by using Gauss-Seidal method.

<br>

## Algorithm:

<br>

  Step 1: Assign $$X_0 = 0, Y_0 = 0, Z_0 = 0$$

<br>

  Step 2: for i = 1 to 9

<br>

  Step 3: Compute $$X = \frac{1}{4} * (1 - Y_0 - Z_0)$$

<br>

  Step 4: Assign $$Y_0 = Y$$

<br>

  Step 5: Compute $$Y = \frac{1}{3} * (2 - X_0 - Z_n)$$

<br>

  Step 6: Assign $$Y_0 = Y$$

<br>

  Step 7: Compute $$Z = \frac{1}{5} * (3 - X_0 - Y_0)$$

<br>

  Step 8: Assign $$Z_0 = Z$$

<br>

  Step 9: Print the value of $$X,Y,Z$$

<br>

## Program:

<br>

```
x0=0; y0=0; z0=0
for i in range (1,10):
 x=1/4*(1-y0-z0)
 x0=x
 y=1/3*(2-x0-z0)
 y0=y
 z=1/5*(3-x0-y0)
 z0=z
print ("The approximate solution of x = %.4f, y= %.4f, z=%.4f"% (x, y,
z))
```

<br>

## Output:

<br>

The approximate solution of x = 0.0000, y= 0.5000, z=0.5000

<br>

## Result:

<br>

The approximate solution is obtained by using Gauss-Seidal method

<br>

# Program 3: Lagrange's Interpolation method

<br>

## Date:

<br>

## Question:

<br>

Using Lagrange interpolation formula, find the value corresponding to 𝒙 = 𝟏𝟎 from the following table 

| x   | 0  | 1  | 2  | 4  | 5  | 6  |
| --- | -- | -- | -- | -- | -- | -- |
| y   | 1  | 14 | 15 | 5  | 6  | 19 |


<br>

## Aim:

<br>

To find the interpolating functional value of y at x = 10 by using Lagrange's method.

<br>

## Algorithm:

<br>

Step 1: Get the value of x

<br>

Step 2: Get the value of y

<br>

Step 3: for i = 0 to 6

<br>

Step 4: for j = 0 to 6

$$
\text{if } i != j
$$


<br>

$$
prod = prod * ( S - n [j])/(x [i] - n[j])
$$

<br>

$$
Sum = sum + pred * y[i]
$$

Step 5: Print the value of y

<br>

## Program:

<br>

```
x= [0,1,2,4,5,6]
y= [1,14,15,5,6,19]
s=float (input ("Enter the value of x to be in: "))
sum=0
for i in range (0,6):
 prod=1
 for j in range (0,6):
 if i!=j:
 prod=prod*(s-x[j])/(x[i]-x[j])
 sum=sum+prod*y[i]
print ("The functional value is %.4f"%sum) 
```

<br>

## Output:

<br>

Enter the value of x to be in: 10

<br>

The functional value is 311.0000 

<br>

## Result:

<br>

The interpolated value of y is obtained

<br>

# Program 4: Trapezoidal rule

<br>

## Date:

<br>

## Question:

<br>

Evaluate $$\int_0^1 \frac{dx}{1 + x^2} $$ using the trapezoidal rule with $$h = 0.2$$.

<br>

## Aim:

<br>

To compute given definite integral by using trapezoidal rule

<br>

## Algorithm:

<br>

Step 1: Define the function $$f(x) = 1 / (1 + x ** 2)$$ 

<br>

Step 2: Define the values of a,b,h.

<br>

Step 3: Compute n = $$(b - a) / h$$

<br>

Step 4: Assign Sum = 0

<br>

- for i = 1 to n
      
- $$Sum = sum + f(a + i$$ x $$h)$$
      
- $$trep = h/2 * ( f(n) + f(b) + 2 * sum)$$

<br>

Step 5: Print the integral value

<br>

## Program:

<br>

```
def f(x):
 return 1/(1+x**2)
a=float (input ("Enter the lower limit: "))
b=float (input ("Enter the upperlimit: "))
h=float (input ("Enter the step size: "))
n=int((b-a)/h)
sum=0
for i in range (1, n):
 sum=sum+f(a+i*h)
trap=h/2*(f(a)+f(b)+2*sum)
print ("The Integral value is %.5f"%trap)
```

<br>

## Output:

<br>

Enter the lower limit: 0

<br>

Enter the upperlimit: 1

<br>

Enter the step size: 0.2

<br>

The Integral value is 0.78373 

<br>

## Result:

<br>

The value of given definite integeral is obtained

<br>

# Program 5: Runge Kutta method of fourth order

<br>

## Date:

<br>

## Question:

<br>

Find $$y(0.2)$$, given that $$\frac{dx}{dy} = x + y^2$$ , $$y(0) = 1$$ , using Runge-Kutta fourth order method.

<br>

## Aim:

<br>

To find approximate colution of the first order differential equation by using Runge-Kuttan Method

<br>

## Algorithm:

<br>

Step 1: Define the function $$f(x,y) = x + y ** 2$$

<br>

Step 2: Get the values of $$x_0, y_0, h$$

<br>

Step 3: Compute $$K_1 = h * f (x_0, y_0)$$

<br>

Step 4: Compute $$K_2 = h * f (x_0 + \frac{h}{2} , y_0 + \frac{K_1}{2})$$

<br>

Step 5: Compute $$K_2 = h * f (x_0 + \frac{h}{2} , y_0 + \frac{K_2}{2})$$

<br>

Step 6: Compute $$K_4 = h * f (x_0 + h , y_0 + K_3)$$

<br>

Step 7: Compute $$y = \frac{y_0 + ( K_1 + 2 * K_2 + 2 * K_3 + K_4 )}{6}$$

<br>

Step 8: Print the value of y.

<br>

## Program:

<br>

```
def f (x, y):
 return x+y**2
x0=float (input ("Enter initial point of x: "))
y0=float (input ("Enter initial point of y: "))
h=float (input ("Enter step value h: "))
k1=h*f (x0, y0)
k2=h*f (x0+h/2, y0+k1/2)
k3=h*f (x0+h/2, y0+k2/2)
k4=h*f (x0+h, y0+k3)
y=y0+(k1+2*k2+2*k3+k4)/6
print ("The value of y using RK method is %.4f"%y) 
```

<br>

## Output:

<br>

Enter initial point of x: 0

<br>

Enter initial point of y: 1

<br>

Enter step value h: 0.2

<br>

The value of y using RK method is 1.2735 

<br>

## Result:

<br>

The solution of first order equation is obtained by using Runge-Kutta method.

<br>

# Program 6: Adam's predictor and corrector method

<br>

## Date:

<br>

## Question:

<br>

Find $$y(1.4)$$ , given that $$\frac{dy}{dx} = x^2 (1 + y) , y(1) = 1 , y(1.1) = 1.233 , y(1.2) = 1.548$$ , and $$y(1.3) = 1.979$$ using Adam’s predictor and corrector method.

<br>

## Aim:

<br>

To find approximate solution of first order differential equation by using Adam's predictor and corrector method

<br>

## Algorithm:

<br>

Step 1: Define the function $$f(x,y) = (x * * 2 ) * ( 1 + y )$$

<br>

Step 2: Get the values of $$x_0, y_0, x, y, x_2, y_2, x_3$$ and $$y_3$$

<br>

Step 3: Compute $$h = x_1 - x_0$$

<br>

Step 4: Compute $$y_{4}^{(p)} = y_3 + \frac{h}{24} * (55f (x_3, y_3) - 59f(x_2, y_2) + 27f(x_1, y_1) - 9f (x_0, y_0))$$

<br>

  - $$x_4 = x_3 + h$$

<br>

Step 5: Compute $$y_{4}^{(c)} = y_3 + \frac{h}{24} * (9f(x_4, y_{4}^{(p)} + 19f (x_3, y_3) - 5f(x_2, y_2) + f(x_1, y_1))$$

<br>

Step 6: Print the value of $$y_{4}^{(c)}$$

<br>

## Program:

<br>

```
def f (x, y):
 return x**2*(1+y)
x0=float (input ("Enter x0: "))
y0=float (input ("Enter y0: "))
x1=float (input ("Enter x1: "))
y1=float (input ("Enter y1: "))
x2=float (input ("Enter x2: "))
y2=float (input ("Enter y2: "))
x3=float (input ("Enter x3: "))
y3=float (input ("Enter y3: "))
h =0.1
y4p=y3+(h/24) *(55*f (x3, y3)-59*f (x2, y2) +37*f (x1, y1)-9*f (x0,
y0))
x4=x3+h
y4c=y3+(h/24) *(9*f (x4, y4p) +19*f (x3, y3)-5*f (x2, y2) +f (x1, y1))
print ("Approximate soln is %0.4f"%y4c) 
```

<br>

## Output:

<br>

Enter x0: 1

<br>

Enter y0: 1

<br>

Enter x1: 1.1

<br>

Enter y1: 1.233

<br>

Enter x2: 1.2

<br>

Enter y2: 1.548

<br>

Enter x3: 1.3

<br>

Enter y3: 1.979

<br>

Approximate solution is 2.5749 

<br>

## Result:

<br>

The solution of first order differential equation is obtained by using Adam's predictor and corrector method.
