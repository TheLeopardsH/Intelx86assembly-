# Intelx86assembly-
Intel x86 assembly introductory tutorial for Reverse Engineering and Malware Analysis

For more in detail guide ,refer to following manuals

Reference Manuals

| Intel Developer’s Manuals                |
|  --------------------------------------  |
| Documentation Changes                    |
| Volume 1: Basic Architecture             |
| Volume 2A: Instruction Set Reference A-M |
| Volume 2B: Instruction Set Reference N-Z |
| Volume 3A: System Programming Guide      |
| Volume 3B: System Programming Guide      |
https://www.intel.com/products/processor/manuals/


There are two notations used in intel Assembly AT&T and Intel Syntax,I would use intel Syntax

Major difference is the source destination location  and $ sign.For example

In AT&T : 
* *mov $4, %eax // GP register assignment*
* *mov $4, %(eax) // Memory assignment*

But in Intel : 
* *mov eax, 4 // GP register assignment*
* *mov [eax],4 // Memory assignment*




### Regiters in x86
```
General purpose registers:EAX,ABX,ACX,ABX,ESI,EDI,EIP
Special purpose registers:ESP,EBP
```

|32bits|                    |            |               |
| ---- | ------------------ | ---------- | ------------- |                              
|      |       16 bits      |   8bits    |    8bits      |
|EAX   |         AX         |    AH      |    AL         |EAX used to be called the accumulator as used by arithmetic operations
|EBX   |         BX         |    BH      |    BL         |
|ECX   |         CX         |    CH      |    CL         |ECX is known as the counter since it is used to hold a loop index
|EDX   |         DX         |    DH      |    DL         |
|ESI   |                    |            |               |
|EDI   |                    |            |               |
|EIP   |                    |            |               |Instruction pointer
|ESP   |                    |            |               |Stack pointer
|EBP   |                    |            |               |Base pointer

AX = accumulator
DX = double word accumulator
CX = counter
BX = base register
SI = Source Index
DI = Destination Index
<!-- 
    calling convention
    call 0xAE436784(i.e push eip+5(address after the function in i think ; jmp 0xAE436784)
     ret (pop eip)
     f(a,b) (push b;push a,call f)  arguments in reverse order   
     hardware stack is based on push, pop, call, and ret instructions-->


