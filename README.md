# OS1000 – A Tiny RISC-V Operating System

This project follows [Operating System in 1000 Lines](https://operating-system-in-1000-lines.vercel.app/en/02-assembly), a tutorial for building a simple operating system from scratch on **RISC-V**.  
The goal is to understand how an OS boots, manages memory and processes, and exposes basic abstractions like system calls and a shell.

---

## 📖 Features (so far / planned)
- [x] Booting on RISC-V and entering supervisor mode  
- [ ] Basic multitasking (switching between processes)  
- [ ] Exception & interrupt handling  
- [ ] Paging and virtual memory  
- [ ] System calls (bridge between user programs and kernel)  
- [ ] Simple device drivers (UART, disk I/O)  
- [ ] File system support  
- [ ] Command-line shell  

---

## 🛠 Requirements
- **RISC-V toolchain** (compiler + assembler + linker)
  - On macOS (Homebrew):  
    ```sh
    brew tap riscv/riscv
    brew install riscv-tools
    ```
  - On Ubuntu/Debian:  
    ```sh
    sudo apt update
    sudo apt install gcc-riscv64-unknown-elf qemu-system-misc make
    ```
- **QEMU (RISC-V target)** – to emulate the OS  
- `make` – build automation  

---

## 🚀 Build & Run
To build the kernel image:
```sh
make