
<style
  type="text/css">
h1 {color:red;}

p {color:blue;}
</style>

# Системный вызов в Linux
[Содержание](../README.md)

` sys_write 0(Input), 1(Output), 2(Error) `
| syscall | ID | RDI | RSI | RDX | R10 | R8 | R9 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| sys_read  | 0  |   |  |  |  |  |  |
| sys_write | 1  | 1 (Output)  | TEXT  | 14 |  |  |  |
| sys_open  | 2  |   |  |  |  |  |  |
| sys_close | 3  |   |  |  |  |  |  |
| sys_exit  | 60 | 0 (Код)  |  |  |  |  |  |
### Aссемблерная инструкция
```
intel x86 int $0x80
intel x86-64 syscall
```
### Номер вызова
```
intel x86 регистр EAX
intel x86-64 регистр RAX
```
### Передача параметров
```
intel x86 регистры EBX, ECX, EDX, ESI, EDI, EBP
intel x86-64 регистры RDI, RSI, RDX, R10, R8, R9
```
### Возврат результата
```
intel x86 регистр EAX
intel x86-64 регистр RAX
```
```asm
section .data
  text db "Hello, World!", 10
section .text
  global _start
_start:
  mov rax, 1
  mov rdi, 1,
  mov rsi, text
  mov rdx, 14
  syscall
  
  mov rax, 60
  mov rdi, 0
  syscall
```
[Содержание](../README.md)
