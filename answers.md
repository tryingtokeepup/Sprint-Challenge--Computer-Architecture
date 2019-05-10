# Potential Questions for Computer Architecture Sprint Challenge

**What are some examples of instructions handled by the CPU (as opposed to the ALU)?**
The CPU can do comparision checks, like with `CMP`, or jump to other parts of memory with `JMP`, `malloc` memory
for new variables and `free` them, and do everything required to smoothly take in instructions and execute them.
The ALU is typically used for the actual number crunching of the program.

**When is the ALU activated in the CPU?**
When the CPU passes inputs, called `operands` and the code indicating what operation is to be performed on thos `operands`, the ALU is activated.
It can be as simple as the `operands` A and B, with A being 2 and B being 3, and passing the operation `ADD` to the ALU, which should output `5`!
**Why are internal registers useful in assembly language?**
Internal registers are useful for assembly to store data that needs to be referenced very, very quickly. `RAM` is great, but its usually situated
outside of the core CPU unit, and so therefore takes a lot of time to traverse to and fro from to retrieve and store data. The registers are right
there in the chip itself, so storing and retrieving data from these registers is much easier. You can use these registers to store stack pointers,
process counters, and variables for storing `operands` that need to be used for work by the `ALU`.
**Convert the 8-bit hex number 0xB7 to binary.**
B 7
1011 0111
`BINARY 10110111`
**Convert the 8-bit binary number 0b10101011 to hex.**
1010 1011
10 11
A B
`Hex AB`
**Why is a CPU stack useful in assembly language?**
The CPU stack is incredibly useful, especially for temporary storing values that you need to use later (so you dont have to waste registers), and
for the purposes for our `LS-8`, to save registers so we can restore our `process counter` after doing a call routine or processing an interrupt
handler. For more mundane usage, we can use a stack to allocate space for local variables in our subroutine calls.
**Turn off the 5th bit from the right of 0b01111100.**
0b01111100
0b11101111 MASK
0b01101100 RESULT

or we can `NAND` or ~(A & B), where A is <<<<< 5 and B is 0.
**Why do people tend to gravitate towards base-10 number systems while computers do better with base-2?**
We have 10 fingers, and `base-10` is really handy in that it can be neatly divided by 1, 10, 5, and even 2. Computers are based on binary/boolean
logic, `on` or `off`, 0 or 1, so computers typically are handled with `base-2` computations.
**Create an AND mask to preserve the last 3 right-hand bits of any 8-bit number.**
0b00000111 MASK
**Describe which form of storage is better - RAM or internal registers.**
I am pretty sure this question is intentionally worded to prompt a rebuttal; there is no `better`, just what you want to do with your memory.
Typically the `RAM` will be the only storage available for any decently sized instruction, as you have a very very limited store of registers to work with.
They are incredibly fast to work with, as they are literally part of the `CPU`, allowing the CPU to access them within one clock cycle. But in general, you
need to store your data on `RAM`, as you only have 8, 32, or at best 64 `bits` of CPU register, as that is how many you physically have to work with. `RAM`,
of course, is much more plentiful.
**Describe the difference in what happens when a JMP command is executed versus a CALL command.**
In a `JMP` command, the cpu literally jumps to the given address stored in the register it calls, unconditionally, and keeps procedually working from there.
There is no paired `RTN` command, so there is no storing of the previous PC location on the stack, and no returning to the address right after the `JMP` command.

# SPRINT CHALLENGE IN MY WEEKLY PROJECT

https://github.com/tryingtokeepup/Computer-Architecture/
