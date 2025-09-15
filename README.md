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
Build the kernel image:
```sh
make
```

Run in RISC-V QEMU:
```sh
make run
```

Clean build artifacts:
```sh
make clean
```

---

## 📂 Project Structure
```
os1000/
├── src/        # RISC-V assembly and C source code
├── build/      # Compiled binaries / OS image
├── docs/       # Notes and diagrams
├── Makefile    # Build script
└── README.md   # Project overview
```

---

## 🎯 Goals
- Learn how a CPU boots and transitions into supervisor mode.  
- Explore how exceptions, traps, and interrupts are handled.  
- Implement paging and isolated virtual address spaces.  
- Build a minimal shell and drivers to interact with hardware.  

---

## 📚 References
- [Operating System in 1000 Lines](https://operating-system-in-1000-lines.vercel.app/en/02-assembly)  
- [RISC-V Specifications](https://riscv.org/technical/specifications/)  
- [QEMU RISC-V Documentation](https://www.qemu.org/docs/master/system/target-riscv.html)  
- [OSDev Wiki](https://wiki.osdev.org)  

---

## ⚠️ Disclaimer
This project is for **educational purposes** only.  
It’s not secure, stable, or suitable for production use.
