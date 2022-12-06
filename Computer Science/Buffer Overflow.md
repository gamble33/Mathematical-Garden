#CompSci 

[^1]: 
[Computerphile video on Buffer Overflows. Amazing source, their example was used. Watch this video.](https://www.youtube.com/watch?v=1S0aBV-Waeo)

# Buffer Overflow
---
## Performing a Buffer Overflow Attack Example
```c
#include <stdio.h>
#include <string.h>

int main(int argc, char** argv) 
{
	char buffer[500];
	strcpy(buffer, argv[1]);

	return 0;
}
```
C program that allocates 500 bytes of memory on the stack and copies the first command line parameter into the buffer[^1].
 
When the main function is [[Disassembler|disassembled]] (using [[gdb]]), it looks as such:
```nasm
Dump of assembler code for function main:
   0x0000000000001169 <+0>:     endbr64
   0x000000000000116d <+4>:     push   %rbp
   0x000000000000116e <+5>:     mov    %rsp,%rbp
   0x0000000000001171 <+8>:     sub    $0x210,%rsp
   0x0000000000001178 <+15>:    mov    %edi,-0x204(%rbp)
   0x000000000000117e <+21>:    mov    %rsi,-0x210(%rbp)
   0x0000000000001185 <+28>:    mov    %fs:0x28,%rax
   0x000000000000118e <+37>:    mov    %rax,-0x8(%rbp)
   0x0000000000001192 <+41>:    xor    %eax,%eax
   0x0000000000001194 <+43>:    mov    -0x210(%rbp),%rax
   0x000000000000119b <+50>:    add    $0x8,%rax
   0x000000000000119f <+54>:    mov    (%rax),%rdx
   0x00000000000011a2 <+57>:    lea    -0x200(%rbp),%rax
   0x00000000000011a9 <+64>:    mov    %rdx,%rsi
   0x00000000000011ac <+67>:    mov    %rax,%rdi
   0x00000000000011af <+70>:    callq  0x1060 <strcpy@plt>
   0x00000000000011b4 <+75>:    mov    $0x0,%eax
   0x00000000000011b9 <+80>:    mov    -0x8(%rbp),%rcx
   0x00000000000011bd <+84>:    xor    %fs:0x28,%rcx
   0x00000000000011c6 <+93>:    je     0x11cd <main+100>
   0x00000000000011c8 <+95>:    callq  0x1070 <__stack_chk_fail@plt>
   0x00000000000011cd <+100>:   leaveq
   0x00000000000011ce <+101>:   retq
End of assembler dump.
```

Line 5 in particular is 
```nasm
0x0000000000001171 <+8>:     sub    $0x210,%rsp
```