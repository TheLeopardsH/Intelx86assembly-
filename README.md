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
General purpose registers:EAX,ABX,ACX,ABX,ESI,EDI
Special purpose registers:EIP,ESP,EBP
```

|32bits|                    |            |               |
| ---- | ------------------ | ---------- | ------------- |                              
|      |       16 bits      |   8bits    |    8bits      |
|EAX   |         AX         |    AH      |    AL         |
|EBX   |         BX         |    BH      |    BL         |
|ECX   |         CX         |    CH      |    CL         |
|EDX   |         DX         |    DH      |    DL         |
|ESI   |                    |            |               |
|EDI   |                    |            |               |
 


