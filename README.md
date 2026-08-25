# 4-Bit ALU — Multisim

A **4-bit Arithmetic Logic Unit (ALU)** designed and simulated using **NI Multisim** as part of a Computer Architecture / Digital Logic project.

The ALU accepts two 4-bit inputs, **A[3:0]** and **B[3:0]**, and performs different arithmetic and logic operations based on the selected **Mode (M)** and operation-select inputs **S1** and **S0**.

## Project Overview

The ALU supports two main modes:

* **Logic Mode (M = 0)** — performs bitwise logic operations.
* **Arithmetic Mode (M = 1)** — performs arithmetic operations.

The circuit also provides status flags to indicate specific conditions after an operation.

## Inputs & Outputs

### Inputs

| Input    | Description                     |
| -------- | ------------------------------- |
| `A[3:0]` | 4-bit input A                   |
| `B[3:0]` | 4-bit input B                   |
| `S1, S0` | Operation select inputs         |
| `M`      | Mode select: Logic / Arithmetic |

### Outputs

| Output   | Description      |
| -------- | ---------------- |
| `F[3:0]` | 4-bit ALU result |
| `C`      | Carry flag       |
| `N`      | Negative flag    |
| `Z`      | Zero flag        |
| `V`      | Overflow flag    |

## Operations

### Logic Mode — M = 0

| S1 | S0 | Function    | Operation |
| -: | -: | ----------- | --------- |
|  0 |  0 | `A · B`     | AND       |
|  0 |  1 | `A + B`     | OR        |
|  1 |  0 | `A'B + AB'` | XOR       |
|  1 |  1 | `A'`        | NOT       |

### Arithmetic Mode — M = 1

| S1 | S0 | Function | Operation   |
| -: | -: | -------- | ----------- |
|  0 |  0 | `A + B`  | Addition    |
|  0 |  1 | `A - B`  | Subtraction |
|  1 |  0 | `A + 1`  | Increment   |
|  1 |  1 | `A - 1`  | Decrement   |

## Status Flags

The ALU generates status flags depending on the performed operation.

### Arithmetic Operations

The following flags are provided:

* **C — Carry:** Indicates a carry or borrow condition.
* **N — Negative:** Indicates that the result is negative.
* **Z — Zero:** Set when the result is zero.
* **V — Overflow:** Indicates an arithmetic overflow condition.

### Logic Operations

For logic operations, only the **Zero (Z)** flag is required.

## Circuit Design

The ALU is implemented using digital logic components and simulated in **NI Multisim**.

The design consists of:

* 4-bit input A
* 4-bit input B
* Mode selection (`M`)
* Operation selection (`S1`, `S0`)
* Arithmetic and logic circuitry
* 4-bit output `F[3:0]`
* Status flag generation
* Probes for monitoring status flags
* 7-segment display for displaying the result

## Simulation

The circuit can be tested by changing the values of:

* `A[3:0]`
* `B[3:0]`
* `M`
* `S1`
* `S0`

The resulting 4-bit output and status flags can then be observed using the probes and 7-segment display.

## Tools

* **NI Multisim**
* Digital Logic Gates
* 4-bit Digital Circuit Design
* Computer Architecture Concepts

## Project Objectives

* Design a functional **4-bit ALU**.
* Implement arithmetic and logical operations using digital circuits.
* Understand ALU operation selection and control signals.
* Generate and interpret arithmetic status flags.
* Simulate and verify the circuit using **NI Multisim**.

## Repository Contents

```text
4-bit-ALU-Multisim/
│
├── README.md
├── 4-bit-ALU.ms14

```
<img width="1090" height="809" alt="image" src="https://github.com/user-attachments/assets/730351ed-e874-4dc1-a8fa-672954bb30b8" />





Designed and simulated using **NI Multisim**.
