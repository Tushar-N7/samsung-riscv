### *Project Summary: RISC-V Core Simulation*

1. *Downloaded the Necessary Files*  
   I started by downloading the required files for the project, which included the *RISC-V core Verilog netlist* (iiitb_rv32i.v) and the *testbench* (iiitb_rv32i_tb.v). These files are essential for simulating and testing the RISC-V processor core.

2. *Updated the Testbench*  
   I then focused on updating the *testbench* (iiitb_rv32i_tb.v). I added key elements to the testbench:
   - *Clock generation*: I implemented a clock signal (clk) with a period of 6 time units (3 high, 3 low).
   - *Reset signal*: I applied a reset (RN) to the core for 5 time units and deasserted it afterward.
   - *Waveform dumping*: I included $dumpfile("iiitb_rv32i.vcd"); and $dumpvars(0, iiitb_rv32i_tb); commands to generate a VCD file for waveform visualization in *GTKWave*.

3. *Compiled the Verilog Files*  
   After updating the testbench, I compiled the Verilog files using *Icarus Verilog. This step created the **compiled simulation file* (simulation_output.vvp), which I could then execute.

4. *Ran the Simulation*  
   I executed the compiled simulation, which generated the *waveform file* (iiitb_rv32i.vcd), containing the signal transitions for the simulation.

5. *Visualized the Waveforms*  
   With the *waveform file* in hand, I used *GTKWave* to open and inspect the simulation results. I analyzed the waveforms of various signals such as clk, RN, NPC, and WB_OUT to verify the functionality of the RISC-V core.

6. *Debugged and Verified Outputs*  
   Based on the waveforms, I confirmed whether the clock, reset, and other signals were behaving as expected. If there were any issues, I identified them by inspecting the transitions of these signals.


---

### *Final Outcome*

By completing these steps, I was able to:
1. Successfully simulate the *RISC-V core* with a *testbench*.
2. Verify the core's functionality using the generated waveforms.
