## NAME:SHYAM SUJIN U
## REG NO.212223040201

# EXP 09-T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**
STEP 1:Type the program in Quartus software.
STEP 2:Compile and run the program.
STEP 3:Generate the RTL schematic and save the logic diagram.
STEP 4:Create nodes for inputs and outputs to generate the timing diagram.
STEP 5:For different input combinations generate the timing diagram.
**PROGRAM**
```
/*Program for logic gates and verify its truth table in quartus using Verilog programming.

module tflipflop( input clk, rst_n, input t,
output reg q,
output q_bar
);
always@(posedge clk) 
begin 
if(!rst_n)
q<=0;
else 
begin
q<=(t?~q:q);
end
end
assign q_bar = ~q;
endmodule

Developed by:SHYAM SUJIN U
RegisterNumber:212223040201
```
*/

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/Shyamsujin/T-FLIPFLOP-POSEDGE/assets/144870449/a21c55cc-0627-4973-b98c-413d5deef163)


**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/Shyamsujin/T-FLIPFLOP-POSEDGE/assets/144870449/cdfa63af-3e50-459e-8a87-c4b82932faaf)


**RESULTS:**
Thus the program to implement a T-FLIPFLOP-POSEDGE using verilog and validating their functionality using their functional tables is successfully completed.
