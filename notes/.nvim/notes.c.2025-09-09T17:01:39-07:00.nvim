// OS STACK: layers of services, each buildering on lower layer
// SYSTEMS PROGRAMMING: low-level programming that directly interacts with
// hardware or the OS often using the syscall interface
//
// TWO fundemental components in computing
// 1. computations: handled by the CPU
// 2. data: handled by memory (RAM)
//
// von Neumann architecture = modern day computers
// - fetch data from memory to provide to CPU
//
// HARDWARE COMPONENTS: CPU, memory, I/O devices
//
//        Problem:
// - CPU was getting faster, so memory access had to get faster too
// - but speed of memory access is limited! (by memory chip speed)
//
//
//        How to solve the issues:
// REGISTERS: very small memory inside a CPU; holds data items from
// memory. (also very close to CPU -> faster to access data
//
// CACHE: larger in size than registers, smaller than memory though
//
// goal: we want CPU to feel like it has access to a HUGE amoutn of
// CHEAP fast memory
//
// Trade offs: 1.cost, 2.distance and access speed, 3.persistence
//(aka if power goes off, what data is retained), 4.reliaability
//(wear and tear)
//
// INSTRUCTION SET ARCHEITECTURE (ISA): defines a set of instructions theCPU can
// perform.
//
//-> the 32-bit vs 64-bit determines the REGISTER size!!
//
//- all pointers are the same size regardless of data type
//-> register size = pointer variable size
//-> address space size: pointer size controls the size of memory
// address space
//
//--> house analogy ABCD ans: C) 1,000,000
//
//- each byte has an address
//
//--> ABCD pointer values ans: D)
//--> ABCD memory Q1 ans: C)
//--> ABCD memory Q2 ans: B)
//
//- why are most computers 64-bit? ans: lets us address 2^64 bytes mem
//--> ABCD why 64-bits ans: C)
//
//-------------------------------------------------------------
// OPERATING SYSTEM (OS) = centeral softwware managing the comps resourcs
//    includes...
// KERNAL: main part that actively manages resources
// SUPPORTING TOOLS: (eg. GUI, CMD line
//
// KERNAL ROLES: resource management, program control, protection
// 1. resource management: mediates access which programs run rn
// 2. program control: kernal controls program running, stopping, etc
// 3. protection: eg. users cant access eachother data
//
// When does the kernel work? kernel is event driven (responds to things)
// 1. Hardware interrupts: mouse clicks
// 2. Syscalls: applications call to kernel
// 3. software interrupts announces an event to process
//
// PRIVILEGE MODE (of CPU execution): kernel mode runs the OS kernel,
// allows full privilege + access to hardware
//-> USER MODE CANNOT execute "priviliged instructions
//- each core will be runnining in either one of these modes (switches)
//
//--> ABCD user mode vs kernel mode ans: A) cuz privilige mode cannot do
// instructions outside of certain programs
//
//-> ROOT USERS CANNOT access kernel memory OR protected instructions
//
//      System
// DEVICE DRIVES: every device needs device driver to control it.
//(eg. network card device driver talks to hardward to send/recieve data to and
// from the physical network.
//
// PROCESSING: proccess, threads, synchronizations, and scheduling
// MEMORY: virutal memory (like your browser having access to memmory), physical
// memory, paging
//
// Virtual File Sys (VFS): data structers and operations that a file sys should
// support. (eg read + write). they are dynamically generated too (not actual
// saved anywhere)
//
//--> ABCD kernel ans: D)
//
//    2 majors ways to run a program:
// 1. Compilations (eg C, C++)
// 2. Interpretation (eg. Python, Bash)
//
// Performance vs Portabilites tradeoff:
// Compliation has better performance
// Compliation NOT portable.
//
// POSIX = Portable Operating System Interface
// ABI = Application Binary Interface
//- is at code level
//- code calls or access the functions for API (such as library)
//- an interface for binary (executable) that OS defines
//
//
