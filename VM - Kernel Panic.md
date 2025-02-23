# Kernel Panic Overview

A kernel panic is an event that occurs when the operating system's kernel detects an error that it can't safely recover from, causing it to abruptly stop functioning and become unusable (*Similar to a Blue Screen of Death on Windows systems*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Kernel Panic Error Messages

Memory Corruption
```Bash
Kernel panic - not syncing: Attempted to kill the idle task!
Panic: Aiee, killing interrupt handler!
```

Driver or Hardware Issues
```Bash
Kernel panic - not syncing: Fatal exception in interrupt
Kernel panic - not syncing: VFS: Unable to mount root fs on unknown-block(0,0)
```

CPU or Hardware Issues
```Bash
Kernel panic - not syncing: CPU context corrupt
Kernel panic - not syncing: Machine check exception: 0000000000000004
```

Kernel Bugs or Null Pointer Dereferences
```Bash
Kernel panic - not syncing: null pointer dereference
BUG: unable to handle kernel paging request at ffffea0000000000
```

Stack Overflows or Bad System Calls
```Bash
Kernel panic - not syncing: stack-protector: Kernel stack is corrupted in: ffffffff81448b6a
Kernel panic - not syncing: Attempted to kill init! exitcode=0x00000100
```

```Bash
Kernel panic - not syncing: hung_task: blocked tasks
```

```Bash
Kernel Panic - not syncing: VFS: Unable to mount root fs on unknown-block(0,0)
```

```Bash
Kernel panic - not syncing: NMI: Not continuing
```

```Bash
Kernel panic - not syncing: out of memory. panic_on_oom is selected
```

```Bash
Kernel panic - not syncing: Fatal Machine check 
```

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Common Causes

## initramfs Issues

The `initramfs` (Initial RAM File System) is a temporary root file system loaded into memory during the early stages of the boot process that allows the kernel to perform necessary operations before the actual root filesystem can be mounted (Ex: *Loading required drivers*, *Handling complex disk setups*, *etc.*)

* The entry related to the `initramfs` file that corresponds to the kernel doesn't exist in the `grub.cfg` file (This is the main configuration file for the GRUB bootloader on Linux systems that contains information about the GRUB menu and a list of installed kernels
* The `initramfs` file doesn't get generated in the /boot directory during kernel installation
* The `initramfs` file gets only partially generated or is corrupted


