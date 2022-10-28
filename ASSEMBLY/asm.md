# Системный вызов в Linux
[Содержание](../README.md)
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
[Содержание](../README.md)
