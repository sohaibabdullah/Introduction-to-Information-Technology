# CSE 5000 – Information to Information Technology  
## Lecture 2: Computer Hardware, OS, and Performance  
**Module:** Digital Infrastructure & Computing Foundations  
**Duration:** 1 hour 20 minutes  

---

## 1. Looking Inside the Computer Systems: Hardware
If we were to take apart our computer or cell phone and look deep inside, we would find the following parts: 
![](./hwarchitecture.png)
So we can say computer hardware devices fall into one of **four** categories:
1.	Processor
2.	Memory
3.	Input and output
4.	Storage (secondary memory)
### Processor
* **Processor** is like the brain of the computer. It organizes and carries instructions that come from either the user or the software. A personal computer processor usually consists of one or more specialised chips, called a microprocessor, which are slivers (splinters) of silicon or other material etched with many tiny electronic circuits. The term Central Processing Unit (or CPU) refers to a computer’s processor.
Every CPU includes the following **three** components (Control Unit, Arithmetic Logic Unit [ALU] and Registers):

  * The **Control Unit** manages the flow of data through the CPU. It directs data to and from the other components within the CPU.

  * **The Arithmetic Logic Unit (ALU)** component does the actual processing. It receives data and instructions and delivers a result. Because all computer data is stored as numbers, much of the processing involves comparing numbers or performing mathematical operations. In addition to establishing and changing ordered sequences, the computer can perform two types of operations: arithmetic and logical. Arithmetic operations include addition, subtraction, multiplication, and division. Logical operations include comparisons, such as determining whether one number is equal to, greater than, or less than another number. Also, every logical operation has an opposite. For example, in addition to “equal to” there is “not equal to.”
  * Many instructions carried out by the control unit involve simply moving data from one place to another—from memory to storage, from memory to the printer, and so forth. When the control unit encounters an instruction that involves arithmetic or logic, however, it passes that instruction to the second component of the CPU, the arithmetic logic unit, or ALU. The ALU actually performs the arithmetic and logical operations described earlier.
  * The ALU includes a group of registers—high-speed memory locations built directly into the CPU that are used to hold the data currently being processed. Registers are holding areas for both data and instructions. We can think of the register as a scratchpad. The ALU will use the register to hold the data currently being used for a calculation. For example, the control unit might load two numbers from memory into the ALU's registers. Then it might tell the ALU to divide the two numbers (an arithmetic operation) or to see whether the numbers are equal (a logical operation). The answer to this calculation will be stored in another register before being sent out of the CPU. That means there are many different registers, each with its own special purpose.
  * **Multi-core CPU:** Most modern CPUs have multiple cores, so they can complete multiple tasks simultaneously, as if they were physically more than one CPU. A core consists of a separate set of essential processor components (control unit, ALU, and registers). Most Intel Core i7 (11th generation) processors typically have eight cores, for example. All the CPU’s cores are located on the same chip.
  * **Hyper-threading:** CPUs now also support hyper-threading which implements the concept **Simultaneous Multithreading (SMT)** Where a single core will present itself as multiple logical cores to a computer’s operating system.
  * Every microcomputer has a **system clock**. Like most modern wristwatches, the clock is driven by a quartz crystal. When electricity is applied, the molecules in the crystal vibrate millions of times per second, a rate that never changes. The computer uses the vibrations of the quartz in the system clock to time its processing operations. In theory, the CPU can execute a function on every tick of the system clock (a clock cycle). However, in practice, the CPU is sometimes idle because there is a delay between the request to retrieve data from memory and its delivery. A delay caused by waiting for another component to deliver data is called **latency**. The clock speed is measured in GHz. GHz is the number of operations a CPU can perform per second (in billions). 1.94 GHz = 1.94 billion operations per second.
  * To help minimize latency, CPUs have **caches**. A cache is a small amount of very fast memory located near (or within) the CPU. Data that the CPU has recently used or is predicted to need soon is placed in the cache for temporary storage. That way, if the CPU requests the data, it’s more readily available, with less delay.
   * Since the late 1980s, most PC CPUs have had cache memory built into them. This CPU-resident cache is often called the level-1 cache, or **L1 cache**.
   * To add even more speed to modern CPUs, an additional cache is added to CPUs. This cache is called Level-2 cache, or **L2 cache**. This cache used to be found on the motherboard. However, Intel and AMD found that placing the L2 cache on the CPU greatly increased CPU response. L2 cache is slower than L1 cache, but bigger in size.
   * In addition to the cache memory built into the CPU, cache is also added to the motherboard. This motherboard-resident cache is now called Level-3 cache or **L3 cache**. L3 cache is the largest cache memory unit, and also the slowest one.
   * L1, L2, and L3 all speed up the CPU, although in different ways. L1 cache holds instructions that the CPU core is currently using or will need immediately. L2 acts as a secondary, larger buffer to store data that couldn't fit in the L1 cache but is still likely to be needed soon. L3 serves as a "last resort" cache before hitting main memory (RAM). It is designed to hold larger datasets and shared data, minimizing the need to access the slow RAM. In all cases, the cache memory is faster for the CPU to access, resulting in quicker program execution.
     
  * **Virtualization** enabled in the CPU (often labeled as Intel VT-x or AMD-V in BIOS) allows a single physical processor to act as multiple, independent virtual CPUs. This crucial feature enables efficient running of virtual machines (VMs), emulators (like BlueStacks), containers (Docker), and security features like Windows Sandbox or Hyper-V, significantly enhancing resource utilization and flexibility. 

### Memory
* Memory is one or more sets of chips that store data and/or program instructions, either temporarily or permanently. PC use several different types of memory, but the two most important are called Main Memory or RAM and ROM.
 * **RAM:** The Main Memory or RAM (Random Access Memory) is used to store information that the CPU needs in a hurry.  RAM holds data and program instruction while while CPU works with them. When a program is launched it is loaded and run from memory. As program needs data, it is loaded into the memory for fast access. The main memory is nearly as fast as the CPU. But the information stored in the main memory vanishes when the computer is turned off. That’s why RAM is called volatile.
  * RAM has tremendous impact on the speed and power of a computer. Generally more 	RAM a computer has, the more it can do and the faster it can perform tasks. The most 	common measurement unit for describing a computer’s memory is the byte – the amount 	of memory it takes to store a single character such as a letter or a numeral. When 	referring to computer’s memory the numbers are often so large that it is helpful to use 	term such as kilobyte (KB), gigabyte (GB), and terabyte (TB) to describe the values.
 * **ROM:** Read-only Memory (ROM) stores its data permanently. It holds instructions that 	the computer needs to operate. Whenever the computer’s power is turned on, it checks 	ROM for directions that help it start up, and for information about its hardware device.
 * **The Secondary Memory or storage** is also used to store information, but it is much slower than the main memory. The advantage of the secondary memory is that it can store information even when there is no power to the computer. Examples of secondary memory or storage are Hard Disk Drive (HDD), solid-state drive (SSD) or flash memory.
 * We may think storage as **electronic file cabinet** and RAM as an **electronic worktable**. When data needed computer locates it in the file cabinet and puts a copy on the table. After finishing work it is put back into file cabinet.
 * **Comparison between storage and RAM** can be made in the following ways:
   * There is more in storage than in memory, just as there is more room in a file cabinet than there is on a tabletop
   * Contents are retained in storage when the computer is turned off, whereas program or the data in memory disappear when we shut down the computer.
   * Storage device operate much slower than memory chips, but storage is much cheaper than memory.
     
*	The **Input and Output Devices** are simply those that allow us to interact with the computer. Input devices accept data, for example: Keyboard, mouse. Output devices deliver data, for example: monitor, printer, and speaker. Some devices can both accept input and deliver output, for example: touch screens.
* These days, most computers also have a Network Connection to retrieve information over a network. We can think of the network as a very slow place to store and retrieve data that might not always be "up". So in a sense, the network is a slower and at times unreliable form of Secondary Memory.




