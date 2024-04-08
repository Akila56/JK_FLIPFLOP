# AIM
To simulate and synthesis of JK_flipflop using vivado 2023.2

# APPARATUS REQUIRED:

vivado 2023

# PROCEDURE:
STEP:1 Start the Xilinx navigator, Select and Name the New project.

STEP:2 Select the device family, device, package and speed. 

STEP:3 Select new source in the New Project and select Verilog Module as the Source type. 

STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it. 

STEP:5 Select the Behavioral Simulation in the Source Window and click the check syntax. 

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 Select the Implementation in the Sources Window and select the required file in the Processes Window. 

STEP:8 Select Check Syntax from the Synthesize XST Process. Double Click in the Floorplan Area/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained.

STEP:9 In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.

STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here. 

STEP:11 Load the Bit file into the SPARTAN 6 FPGA STEP:11 On the board, by giving required input, the LEDs starts to glow light, indicating the output
# JK_FLIPFLOP
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/094e9d55-5f30-4984-90b9-dd51d5297974)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/5b973ee8-9ee2-402d-8cba-1adfa2e4d5f2)
# PROGRAM
module jk_ff (q, q_bar, j,k, clk, reset);        
 input j,k,clk, reset;
 output reg q;
 output q_bar;
 always@(posedge clk) begin
 if(!reset)
        q <= 0;
 else 
 begin
    case({j,k})              
         2'b00: q <= q; // No change
         2'b01: q <= 1'b0; // reset
         2'b10: q <= 1'b1; // set
         2'b11: q <= ~q; // Toggle                       
      endcase
    end
 end
     assign q_bar = ~q;
 endmodule
# Truth Table
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/04d4ff52-ae20-4e08-bd70-58137b129890)
# OUTPUT
![image](https://github.com/Akila56/JK_FLIPFLOP/assets/164776026/d4098849-3059-4e33-b38f-c2af848627f3)
# RESULT
Thus the simulation and synthesis of JK_flipflop using vivado 2023.2 is successfully executed and verified.

