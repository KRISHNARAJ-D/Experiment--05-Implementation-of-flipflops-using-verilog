# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:
– PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED: 
Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
1. Open Quartus II and select new project and choose the file location.
2. Module Declaration. Module should have the file name.
3. Declare Inputs and outputs.
4. Use assign declaration and wire to define the functionality of logic circuits.
5. End the program with endmodule.
6. Run the program and choose RTL viewer to get RTL realization.

### PROGRAM 
```
Program for flipflops  and verify its truth table in quartus using Verilog programming.

Developed by: Krishnaraj D
RegisterNumber: 212222230070
```

```
i] SR flipflops
module flipflops(S,R,Q,Qbar,clk);
input S,R,clk;
output reg Q,Qbar;
initial Q = 0;
initial Qbar = 1;
always @(posedge clk)
begin
Q = S|((~R)&Q);
Qbar = R|((~S)&(~Qbar));
end
endmodule
```
```
ii] JK flipflops
module JK(J,K,Q,Qbar,clk);
input J,K,clk;
output reg Q,Qbar;
initial Q = 0;
initial Qbar = 1;
always @(posedge clk)
begin
Q = (((~K)&Q)|(J&(~Q)));
Qbar = ((~J)&Qbar)|((~K)&(~Qbar)); 
end
endmodule
```
```
iii] D flipflop
module Dflipflop(D,Q,Qbar,clk);
input D,clk;
output reg Q,Qbar;
initial Q = 0;
initial Qbar = 1;
always @(posedge clk)
begin
Q = D;
Qbar = ~D;
end
endmodule
```
```
iv] T flipflop
module Tflipflop(T,Q,Qbar,clk);
input T,clk;
output reg Q,Qbar;
initial Q = 0;
initial Qbar = 1;
always @(posedge clk)
begin
Q = ((T&(~Q))|((~T)&Q));
Qbar = ((~T)&Qbar)|(T&(~Qbar));
end
endmodule
```



## RTL LOGIC FOR FLIPFLOPS 
### SR flipflpos
![SR](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/d70734c2-7784-42f6-a12c-7a2ce0e020d4)


### JK flipflop
![JK](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/3160ec65-3c98-49b9-a6ff-e78e63ae5933)


### D flipflop
![D](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/10cf977f-0a6b-42c4-b45c-de40f319c61b)


### T flipflop
![T](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/ecf6a3a8-6a74-480a-b5fe-1294a0f1714a)


## TIMING DIGRAMS FOR FLIP FLOPS 
### SR flipflop
![SR TIMING](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/a3583a97-3d2b-4c66-abd0-d39d7755eab9)


### JK flipflop
![JK TIMING](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/5effee10-4481-4022-a830-e9b1f1017bd9)


### D flipflop
![D TI](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/12d64479-e357-4965-b072-93e4ee0b0226)


### T flipflop
![T TI](https://github.com/KRISHNARAJ-D/Experiment--05-Implementation-of-flipflops-using-verilog/assets/119559695/05b14037-de9f-4bc2-a33f-94117f4ebfef)


## RESULTS 
All the flipflops are implementde using verilog and their functionality has been validated using their functional tables.
