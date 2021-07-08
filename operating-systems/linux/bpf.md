---
description: >-
  BPF is a revolutionary technology that can run sandboxed programs in the Linux
  kernel without changing kernel source code or loading kernel modules.
---

# BPF

BPF \(formally known as eBPF\) is a revolutionary technology that can run sandboxed programs in the Linux kernel without changing kernel source code or loading kernel modules. By making the Linux kernel programmable, infrastructure software can leverage existing layers, making them more intelligent and feature-rich without continuing to add additional layers of complexity to the system.

eBPF was [described by](https://lkml.org/lkml/2015/4/14/232) Ingo Molnár as:

> One of the more interesting features in this cycle is the ability to attach eBPF programs \(user-defined, sandboxed bytecode executed by the kernel\) to kprobes. This allows user-defined instrumentation on a live kernel image that can never crash, hang or interfere with the kernel negatively.



#### BPF Compiler Collection \(BCC\)

BCC makes BPF programs easier to write, with kernel instrumentation in C \(and includes a C wrapper around LLVM\), and front-ends in Python and lua. It is suited for many tasks, including performance analysis and network traffic control.

#### Resources

* [What is eBPF?](https://ebpf.io/what-is-ebpf)
* [BPF Compiler Collection \(BCC\)](https://github.com/iovisor/bcc)

