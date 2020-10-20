# Simplex-Method
Solve the Linear Programing Problem using Simplex Method in Python 


Write a program to solve an LPP using simplex method.
Example 1: Max Z=3x1+4x2
such that x1+2x2 <=4
          3x1+2x2<=6
          x1, x2 >=0
Introducing x3 and x4 slack variable in equation 1 and 2.

                    Cj    3      4      0      0      b/aj
CB     B     XB     b     a1     a2     a3     a4     minRatio     Operation

0      a3    x3     4     1      2      1      0      4/2=2

0      a4    x4     6     3      2      0      1      6/2=3

Zj-Cj               0    -3     -4      0      0



                    Cj    3      4      0      0      b/aj
CB     B     XB     b     a1     a2     a3     a4     minRatio     Operation

4      a2    x2     2     1/2     1     1/2    0      2/1/2=4      R1'=R1/2

0      a4    x4     2     2      2      0      -1     2/2=1        R2'=R2-2R1'

Zj-Cj               8    -1      0      2      0



                    Cj    3      4      0      0      b/aj
CB     B     XB     b     a1     a2     a3     a4     minRatio     Operation

4      a2    x2     3/2   0      1      3/4    -1/4     

3      a1    x1     1     1      0      -1/2    1/2      6/2=3

Zj-Cj               9     0      0      3/2      1/2


Max Value Z=9 and x1=1, x2=3/2
