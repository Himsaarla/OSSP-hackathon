# CPU and Memory Stress Testing Tool

**Section:** 6  
**Team:** 1  
**Faculty:** Dr. Kotte Anusha

## Team Members

| Name | Roll Number |
|---|---|
| Navaneeth | 2520030058 |
| Himesh | 2520030317 |

> Note: The same roll number was provided for both members. Verify the numbers before submitting the project.

## Project Overview

The **CPU and Memory Stress Testing Tool** is a terminal-based Operating Systems project developed in C for a Linux environment. It is intended to demonstrate how a system behaves when CPU and memory resources are under load.

The project presentation describes these main capabilities:

- **CPU stress testing:** Generates continuous computational workloads, potentially using multiple threads.
- **Memory stress testing:** Allocates and accesses memory blocks to simulate high memory usage.
- **Combined testing:** Applies CPU and memory workloads together.
- **System monitoring:** Reads system information from `/proc/stat` and `/proc/meminfo`.
- **Terminal results:** Displays monitoring information and test completion details.

Actual features and results should be confirmed against the final source code and tested program.

## Operating System Concepts Demonstrated

- CPU scheduling and utilization
- Threads and concurrency
- Memory allocation and memory pressure
- Linux `/proc` system information
- Synchronization, where implemented
- Error handling and resource cleanup

## Requirements

- Ubuntu/Linux environment (or a compatible WSL environment)
- GCC compiler
- C source code for the project
- Terminal
- POSIX threads support if the source uses pthreads

## Compilation

If the main source file is named `stress.c`, compile it with:

```bash
gcc -Wall -Wextra -O2 stress.c -o stress -pthread
```

If your source file has a different name, replace `stress.c` with the actual filename. If the project contains multiple source files, include all required files in the command.

## Run

```bash
./stress
```

Follow the options shown by the program. Start with conservative test settings and do not assume options that are not implemented in the source code.

## Useful Monitoring Commands

These commands can help you observe system behaviour during a test:

```bash
top
free -h
ps -ef
cat /proc/stat
cat /proc/meminfo
```

`top` and other optional tools may need to be installed separately.

## Testing Checklist

- [ ] Run the CPU stress test and record actual observations.
- [ ] Run the memory stress test and record actual observations.
- [ ] Run the combined test and record actual observations.
- [ ] Check invalid-input handling, if supported.
- [ ] Confirm that threads/processes stop correctly.
- [ ] Confirm that allocated memory and other resources are released.
- [ ] Capture screenshots of real program output for the report.

Do not add estimated CPU percentages, memory values, or pass/fail results. Record results only after running the program.

## Safety Notes

Stress tests deliberately increase resource usage and may make a computer slow or unresponsive. Save important work before testing, use conservative workload settings, and avoid allocating more memory than the system can safely provide. Stop the test if the system becomes unstable.

## Project Structure

A simple project layout may look like this; adjust it to match your actual repository:

```text
project/
├── stress.c        # Main C source file (if this is its actual name)
├── README.md
└── screenshots/    # Optional real execution screenshots
```

## Future Enhancements

- Configurable test duration, thread count, and memory size
- Timestamped logs and exportable results
- Live CPU and memory charts
- Controlled disk I/O stress testing
- Automated tests and a Makefile
- Improved validation and graceful interruption

## References

- Linux man-pages
- GNU Compiler Collection (GCC) documentation
- POSIX specifications
- Linux `/proc` filesystem documentation
- Team project presentation: *CPU and Memory Stress Testing Tool*

