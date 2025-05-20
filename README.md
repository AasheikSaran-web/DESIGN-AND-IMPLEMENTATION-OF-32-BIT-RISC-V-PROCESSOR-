 32-bit Single-Cycle RISC-V Processor on FPGA

 Authors
- **Aasheik Saran S**, CeNSE, IISc Bangalore – [aasheiks@iisc.ac.in](mailto:aasheiks@iisc.ac.in)  
- **Hariram P**, DESE, IISc Bangalore – [hariramp@iisc.ac.in](mailto:hariramp@iisc.ac.in)



 Overview

This project presents the **design and implementation of a 32-bit single-cycle RISC-V processor**, compliant with the RV32I ISA. The processor is implemented on a **Digilent BASYS3 FPGA** board using **Verilog HDL**. It includes support for:
- Arithmetic and logical instructions
- Load/store operations
- Branching
- LUI (Load Upper Immediate)
- Direct-mapped **instruction cache** for performance enhancement

 Instructions like `JALR`, `AUIPC`, and `ECALL` are not supported to simplify design.

---

 Features

- **Single-cycle execution** of each instruction
- **RV32I ISA subset** support
- **Direct-mapped instruction cache** (4-word block size)
- **Custom Verilog implementation**
- **Simulation & on-chip validation** using Xilinx Design Suite
- Programs compiled with **RISC-V GCC toolchain**

---

 Architecture Diagram

![Block Diagram](images/processor_block_diagram.png)  
*Fig: Single-Cycle RISC-V Processor Block Diagram*

---

 Components

- **ALU**
- **Register File**
- **Control Unit**
- **Immediate Generator**
- **Instruction Memory**
- **Data Memory**
- **Instruction Cache**

---

 FPGA Implementation

- **FPGA Board:** Digilent BASYS3  
- **Chipset:** Xilinx Artix-7 (XC7A35T-CPG236C)  
- **Language:** Verilog HDL  
- **Toolchain:** Xilinx Vivado, RISC-V GCC

 Workflow
1. Write program in C
2. Compile using RISC-V GCC
3. Convert binary to memory initialization file
4. Load into FPGA via Vivado
5. Validate functionality using simulation and LEDs/switches

---

Validation

- Simulation done using **ModelSim** or Vivado Simulator
- Programs tested on-chip for instruction compliance
- Results displayed via LEDs/register readout

 Example Waveform

![Simulation Waveform](images/simulation_waveform.png)  
*Fig: Instruction Execution Simulation*

---

 Motivation

- **Open-source CPU design** platform for academia and embedded systems
- RISC-V’s modularity and openness is ideal for **custom architecture development**
- **Single-cycle architecture** makes learning and debugging simpler
- Instruction cache introduces **real-world performance considerations**

---

 Future Work

- Add pipelining stages
- Support more instructions (`JALR`, `AUIPC`, `ECALL`)
- Introduce **data cache**
- Implement **hazard detection and forwarding logic**
- Multi-core or multi-level cache experiments

---

Demo Snapshots

 Processor Running DFS (Demo Code)

![DFS Output](images/demo_dfs_output.png)


License

This work is intended for **academic and educational** purposes.

---

## 📞 Contact

For questions, feel free to reach out:
- aasheiks@iisc.ac.in
- hariramp@iisc.ac.in
