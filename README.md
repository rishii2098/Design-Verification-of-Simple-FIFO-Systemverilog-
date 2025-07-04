# Design-Verification-of-Simple-FIFO-Systemverilog-

# FIFO Design and Verification using SystemVerilog

## 📝 Overview

This project demonstrates the design and verification of a **simple FIFO (First-In-First-Out)** memory using **SystemVerilog**. The FIFO supports `write`, `read`, `reset`, `full`, and `empty` operations. A testbench is developed to verify its basic functionality using randomized read/write transactions.

---

## 🎯 Goals

- Design a 16-depth, 8-bit wide FIFO memory module.
- Write a SystemVerilog testbench using:
  - Transactions
  - Mailboxes
  - Scoreboard
  - Generator, Driver, Monitor components
- Apply random read/write operations and check for correct data handling.
- Ensure correct behavior of `full` and `empty` signals.

---

## 📐 Testbench Components

- **Transaction**: Holds data and control info.
- **Generator**: Produces random read/write operations.
- **Driver**: Applies operations to the DUT.
- **Monitor**: Observes outputs and records activity.
- **Scoreboard**: Compares expected vs actual output using a queue.
- **Environment**: Connects all the above and runs the test.

---

## ▶️ Run It Online

You can run this design and testbench online using EDA Playground:

👉 [Open in EDA Playground](https://edaplayground.com/x/Gvss)

---

## 🧪 How the Test Works

- Randomly chooses to perform either a **read** or **write**.
- **Writes** insert data into the FIFO if it is not full.
- **Reads** retrieve data from the FIFO if it is not empty.
- The **scoreboard** tracks written values and verifies if read outputs match expectations.
- Tracks any mismatches and prints error count at the end.

---
