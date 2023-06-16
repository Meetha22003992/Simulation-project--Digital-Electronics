# AIM:
To design and stimulate a 3 mod synchronous counter with JK flip-flop using Verilog

# THEORY
1. Create a new project in Quartus|| Software.
2. .Name the project as upc for JK flip=flop
3. Within that file write the program for mod 3 synchronous counter using JK flip-flop
4. After that run the program and give the clock pulse value as 50 in timing diagram and run
the program.

# PROGRAM
```
module upc(clk,A);
input clk;
output reg[0:3]A;
always@(posedge clk)
begin
A[0]=((((A[1])&(A[2]))&A[3])^A[0]);
A[1]=(((A[2])&(A[3]))^A[1]);
A[2]=((A[3])^A[2]);
A[3]=1^A[3];
end
endmodule
DOWNCOUNTER:
module downc(clk,A);
input clk;
output reg[0:3]A;
always@(posedge clk)
begin
A[0]=((((~A[1])&(~A[2]))&A[3])^A[0]);
A[1]=(((A[2])&(A[3]))^A[1]);
A[2]=((A[3])^A[2]);
A[3]=1^A[3];
end
endmodule
```
# OUTPUT:

TIMING DIAGRAM:

![image](https://github.com/Meetha22003992/Simulation-project--Digital-Electronics/assets/119401038/e7a33c2d-fbf2-49d8-b6a3-37e595951c7e)

RTL VIEWER:

![image](https://github.com/Meetha22003992/Simulation-project--Digital-Electronics/assets/119401038/a33b4ceb-b68e-4a9e-9b75-d32edf5ee2af)

# RESULT:
