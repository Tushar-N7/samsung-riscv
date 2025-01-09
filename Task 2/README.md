I tried using the **Spike RISC-V simulator** with the **proxy kernel (pk)** to emulate RISC-V architecture. Running `spike -d pk` simulates the RISC-V environment in debugging mode, providing detailed execution output. I experimented with optimization flags like `-O1` for balanced performance and stability, and `-Ofast` for more aggressive optimizations that prioritize speed over correctness. This setup allows for testing and performance tuning of RISC-V code without needing physical hardware.

I wrote a simple C program that adds two integers and prints the result. 
The program was compiled using **RISC-V GCC** with two optimization levels: `-O1` and `-Ofast`. I used a **Makefile** to automate the process and generated object dumps with `riscv64-unknown-elf-objdump` to compare the machine code.
 `-O1` applies basic optimizations, while `-Ofast` uses aggressive optimizations for better performance.
 Finally, I used **SPIKE** to simulate the program's execution. 
This process allowed me to analyze the impact of different optimization levels on the compiled code.
