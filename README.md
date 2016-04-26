# PHYS227 CW 10

**Author(s):** Michael Seaman, Taylor Patti, Austin Ayers, Chinmai Raman, Andrew Malfavon


**Due date:** 2016/04/26

## Specification

For each of the following integration methods, discuss together on the white board to understand how they work for solving a first-order ordinary differential equation (ODE) $$u'(t) = f[t, u(t)]$$ on a discretized grid $(t_0, t_1, t_2, ..., t_N)$ with points $u_k = u(t_k)$ and grid spacing $\Delta t = t_{k+1} - t_k$. Write a joint notebook ```cw10.ipynb``` that summarizes your conclusions and details what each method is doing.

1. Euler's Method: 
   
   $u_{k+1} = u_k + \Delta t\, f[t_k, u_k]$ 
1. Leapfrog (Midpoint) Method: 
   
   $u_{k+1} = u_{k-1} + 2\Delta t\, f[t_k, u_k]$  
   
   (How do you compute $u_1$?)
1. Heun's (Trapezoid) Method: 
   
   $\tilde{u}_{k+1} = u_k + \Delta t\, f[t_k, u_k]$, 
   
   $u_{k+1} = u_k + (\Delta t/2)(f[t_k, u_k] + f[t_{k+1}, \tilde{u}_{k+1}])$  
   
   (Note the two steps - what is each doing?)
1. 2nd-order Runge-Kutta Method: 
   
   $u_{k+1} = u_k + K_1$, 
   
   $K_1 = \Delta t\, f[t_k, u_k]$, 
   
   $K_2 = \Delta t\, f[t_k + \Delta t/2, u_k + K_1/2]$  
   
   (How does this differ from Heun's method?)
1. 4th-order Runge-Kutta Method: 
   
   $u_{k+1} = u_k + (K_1 + 2K_2 + 2K_3 + K_4)/6$, 
   
   $K_1 = \Delta t\,f[t_k,u_k]$, 
   
   $K_2 = \Delta t\, f[t_k + \Delta t/2, u_k + K_1/2]$, 
   
   $K_3 = \Delta t\, f[t_k + \Delta t/2, u_k + K_2/2]$, 
   
   $K_4 = \Delta t\,f[t_k + \Delta t, u_k + K_3]$  
   
   (Note that final increment is a weighted average of four different increments - what is each doing? Why do you suppose the middle increments are more heavily weighted?)

In practice, the 4th-order Runge-Kutta method is the most popular method for integrating ODEs, since it nicely balances the precision per time step with the total number of required computations.

## Assessment

Good times.

## Honor Pledge

I pledge that all the work in this repository is my own with only the following exceptions:

* Content of starter files supplied by the instructor;
* Code borrowed from another source, documented with correct attribution in the code and summarized here.

Signed,

Michael Seaman, Taylor Patti, Austin Ayers, Chinmai Raman, Andrew Malfavon
