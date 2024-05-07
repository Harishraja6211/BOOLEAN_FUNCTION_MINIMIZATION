# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module ex01san(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule
```

Developed by:harish.e 
register no;212223220031

**RTL realization**
![316319712-dee09fd9-6b44-40ef-afbf-d6ab2e627d53](https://github.com/Harishraja6211/BOOLEAN_FUNCTION_MINIMIZATION/assets/154001429/5a6a1d27-46ef-447c-8c80-35b0c01a44bc)

**Truth Table**
![316319842-96ebeb42-3093-489e-b6ab-688e9a11d038](https://github.com/Harishraja6211/BOOLEAN_FUNCTION_MINIMIZATION/assets/154001429/5b0c46ba-2a85-40dc-b41a-97b292e3f1b5)

**Timing Diagram**
![319933239-4e9caee5-196e-49c4-8caf-a081849bc641](https://github.com/Harishraja6211/BOOLEAN_FUNCTION_MINIMIZATION/assets/154001429/8eca5e03-685a-495c-b6b3-f1c815b2ff88)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
