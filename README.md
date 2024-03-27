# BOOLEAN_FUNCTION_MINIMIZATION

# AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

# EQUIPMENT REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# THEORY:

# Boolean Function Minimization Techniques
**1. Algebraic Minimization**

Explain algebraic manipulation techniques for Boolean function minimization. Cover methods like absorption, consensus theorem, and simplification using Boolean laws. Provide examples illustrating algebraic minimization.

**2. Karnaugh Maps (K-Maps)**

Introduction to Karnaugh maps as a graphical method for Boolean function minimization. Explanation of grouping, adjacency, and prime implicants. Step-by-step procedure for minimizing Boolean functions using K-Maps. Examples demonstrating K-Map minimization.

**3. Quine-McCluskey Algorithm**

Overview of the Quine-McCluskey algorithm for exact minimization of Boolean functions. Explanation of prime implicants, essential prime implicants, and prime implicant charts. Step-by-step procedure for applying the Quine-McCluskey algorithm. Examples showcasing the application of the algorithm.

**4. Espresso Algorithm**

Introduction to the Espresso algorithm for heuristic minimization of Boolean functions. Description of the espresso heuristic and cover generation process. Explanation of the Espresso algorithm's iterative improvement approach. Illustrative examples of Espresso algorithm minimization.

**Comparison of Techniques**

Comparative analysis of algebraic minimization, K-Maps, Quine-McCluskey, and Espresso algorithm. Advantages and disadvantages of each technique. Scenarios where each technique is most suitable.

**Applications**

Practical applications of Boolean function minimization in digital logic design. 
Impact on circuit complexity, power consumption, and speed. 
Real-world examples demonstrating the importance of minimization.


# PROCEDURE

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


#   PROGRAM:
#   Developed by:SANJUSHRI.A
#   RegisterNumber:212223040187
```
module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
//type code for f2 as like f1
not(ydash,y);
and(s,x,y);
and(t,ydash,z);
and(u,w,y);
or(f2,s,t,u);
endmodule
```


# RTL REALIZATION:

# OUTPUT:
 ![Screenshot 2024-03-27 133101](https://github.com/Sanjushri13/BOOLEAN_FUNCTION_MINIMIZATION/assets/164732231/c6f2b780-4897-49a8-bd19-c78a23cff8e6)


# TIMING DIAGRAM
  ![Screenshot 2024-03-27 133000](https://github.com/Sanjushri13/BOOLEAN_FUNCTION_MINIMIZATION/assets/164732231/e5f991e7-60a6-4932-af95-46cacaf1f732)


# RESULT:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

