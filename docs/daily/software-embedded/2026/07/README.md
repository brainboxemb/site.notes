# 2026-07

> This page was created with the assistance of ChatGPT. Information and links should be verified.

## 2026-07-29

### `printf` Is a Shared Resource

Embedded systems note by **Jacob Beningo / Beningo Embedded Group**.

Calling `printf` directly from multiple RTOS tasks can cause blocking, interleaved output and timing problems.

A cleaner architecture gives the logging interface a single owner:

* application tasks place log messages in a queue;
* a dedicated logging task reads the queue;
* only the logging task accesses the UART.

This keeps the output serialized and prevents application tasks from waiting unnecessarily for the UART transmission to finish.

Interrupt-driven or DMA-based transmission can improve the transport, but clear ownership and synchronization are still required.

[![printf is a shared resource](./_images/20260729-beningo-embedded-group-printf-shared-resource.jpg ':size=320')](https://www.beningo.com/)

* [Beningo Embedded Group](https://www.beningo.com/)
