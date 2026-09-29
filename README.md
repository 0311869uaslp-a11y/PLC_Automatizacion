# PLC & Industrial Automation

Repository containing practical exercises, simulations, and control programs developed during my academic training in **Industrial Automation and Programmable Logic Controllers (PLC)** at the **Universidad Autónoma de San Luis Potosí (UASLP)**.

The repository includes PLC-based automation projects implemented and simulated using **RSLogix 500 and LogixPro**, covering Ladder Logic, timers, sequencers, bit-shift operations, subroutines, and industrial control sequences.

Additional exercises include electrical control simulations for **three-phase motors, reversing circuits, electric gates, traffic-light systems, and chemical mixing processes**.

---

## Repository Overview

The projects progress from basic industrial-control concepts to more structured PLC programs:

```text
Industrial Automation
        |
        v
Electrical Control
        |
        v
PLC Fundamentals
        |
        v
Ladder Logic
        |
   +----+----+
   |         |
   v         v
Timers    Control Logic
   |         |
   v         v
Traffic   Industrial
Lights    Processes
   |
   v
Sequencers
   |
   v
Bit-Shift Operations
   |
   v
Subroutines
   |
   v
Structured PLC Programs
```

---

# Technologies & Tools

The repository contains practical work with:

- PLC programming
- Ladder Logic
- RSLogix 500
- LogixPro
- CADe_SIMU
- Timers
- Sequencers
- Bit-shift registers
- PLC subroutines
- Industrial electrical control
- Motor-control circuits
- Sequential automation

---

# Repository Projects

## 1. Electric Gate Opening and Closing Control

**Directory:** `T1_APERTURA Y CIERRE DE PORTON`

PLC exercise for controlling the opening and closing sequence of an **electric gate**.

The project introduces the implementation of sequential industrial-control logic where the system must react to commands and control the movement of an actuator.

Conceptually:

```text
        User Command
             |
             v
        PLC Inputs
             |
             v
        Control Logic
          /       \
         v         v
      Opening    Closing
         |         |
         v         v
       Motor / Actuator
```

This exercise provides an introduction to translating a physical automation problem into PLC control logic.

---

## 2. Three-Phase Motor Start/Stop and Reversing Control

**Directory:** `T2_SIMULACIÓN DE CIRCUITO DE ARRANQUE Y PARO DE UN MOTOR TRIFASI`

Simulation of an industrial control circuit for a **three-phase motor**.

The exercise includes:

- Motor start
- Motor stop
- Forward/reverse operation
- Direction reversal
- Indicator lamps
- Electrical protection
- Power circuit
- Control circuit

The circuit was implemented and simulated using **CADe_SIMU**.

The basic architecture is:

```text
Control Commands
       |
       v
 Control Circuit
       |
   +---+---+
   |       |
   v       v
Forward   Reverse
   |       |
   +---+---+
       |
       v
 Contactors / Protection
       |
       v
 Three-Phase Motor
```

This exercise connects PLC/automation concepts with traditional industrial electrical-control systems.

---

# 3. Simple Traffic Light Using Timers

**Directories:**

```text
T3_SEMAFORO CON TIMERS
P2_(TIMERS) IMPLEMENTACIÓN DE UN SEMAFORO SIMPLE
```

Implementation of a simple traffic-light control system using **PLC timers**.

The project was developed using **RSLogix 500** and simulated with **LogixPro**.

The traffic-light sequence can be represented as:

```text
        START
          |
          v
        GREEN
          |
        Timer
          |
          v
        YELLOW
          |
        Timer
          |
          v
         RED
          |
        Timer
          |
          +------> Repeat
```

This exercise introduces timer-based sequential control.

---

## PLC Timers

Timers are fundamental instructions in industrial automation because many physical processes depend on time.

Conceptually:

```text
Condition
    |
    v
 Timer Enabled
    |
    v
 Accumulated Time
    |
    v
Preset Reached
    |
    v
Output / Next State
```

The traffic-light exercise demonstrates how timed events can be coordinated using Ladder Logic.

---

# 4. Complete Intersection Traffic Light Using Limits

**Directories:**

```text
T4_SEMAFORO COMPLETO CON LIMITES
P3_SEMAFORO COMPLETO CON LIMITES
```

Development of a more complete **intersection traffic-light control system** using limit-based PLC logic.

The project extends the simple timer exercise into a larger sequence representing a real traffic intersection.

Conceptually:

```text
             Intersection Controller
                      |
             +--------+--------+
             |                 |
             v                 v
        Direction A       Direction B
             |                 |
       +-----+-----+       +---+---+
       |     |     |       |   |   |
       v     v     v       v   v   v
     Green Yellow Red    Green Yellow Red
```

The project was programmed in **RSLogix 500** and tested through **LogixPro simulation**.

---

# 5. Traffic-Light Control Using Sequencers

**Directories:**

```text
T5_SEMAFORO COMPLETO CON SECUENCIADORES
P4_Semaforo de crucero real usando secuenciador
```

This exercise implements a complete intersection traffic-light system using a **PLC sequencer**.

Instead of controlling every transition independently, the traffic-light states are organized as a sequence.

```text
Step 1
  |
  v
Step 2
  |
  v
Step 3
  |
  v
Step 4
  |
  v
...
  |
  +----> Repeat
```

Each step represents a predefined combination of outputs.

For example:

```text
Sequence
   |
   +--> State 1: Direction A Green
   |
   +--> State 2: Direction A Yellow
   |
   +--> State 3: Direction A Red
   |
   +--> State 4: Direction B Green
   |
   +--> State 5: Direction B Yellow
   |
   `--> Repeat
```

This approach demonstrates how sequencers can simplify complex repetitive industrial-control processes.

---

# 6. Bit-Shift Register Applications

**Directory:**

```text
P5_APLICACION DE LOS REGISTROS DE CORRIMIENTO DE BIT
```

The repository also contains exercises related to **bit-shift registers** in PLC programming.

A shift register moves stored binary states through a sequence of memory positions.

Conceptually:

```text
Initial:

[1][0][0][0][0]

Shift:

[0][1][0][0][0]

Shift:

[0][0][1][0][0]

Shift:

[0][0][0][1][0]
```

This concept can be useful for sequential industrial processes where an event or state must progress through multiple stages.

Applications can include:

- Sequential processes
- Conveyor tracking
- Production-line states
- Step-based automation
- Output sequencing

---

# 7. PLC Subroutines

**Directory:**

```text
P6_APLICACIONES DE LAS SUBRUTINAS Semaforo de crucero real
```

This project implements a traffic-light system using **PLC subroutines (JSR)**.

The program contains a structured organization including:

```text
LAD2 - MAIN_PROGRAM
LAD3 - USER_FAULT
LAD4 - STI_INT
```

The use of subroutines allows a PLC program to be divided into smaller logical components.

Conceptually:

```text
             MAIN PROGRAM
                  |
        +---------+---------+
        |                   |
        v                   v
   Subroutine A        Subroutine B
        |                   |
        v                   v
 Control Logic        Control Logic
        |                   |
        +---------+---------+
                  |
                  v
               Outputs
```

This provides a more structured approach than implementing the complete automation sequence in a single program block.

---

## JSR — Jump to Subroutine

The exercise uses the **JSR (Jump to Subroutine)** concept.

```text
Main Program
     |
     v
JSR Instruction
     |
     v
Subroutine
     |
     v
Execute Logic
     |
     v
Return
     |
     v
Main Program
```

Subroutines improve:

- Program organization
- Modularity
- Maintainability
- Logical separation
- Reuse of control routines

---

# 8. Chemical Mixer Automation

**Directory:**

```text
T_MEZCLADORA DE QUIMICOS
```

PLC exercise involving the automation of a **chemical mixing process**.

Unlike the traffic-light exercises, this project represents a more explicitly industrial process-control application.

The general process can be represented as:

```text
        Process Start
             |
             v
       Input / Material
             |
             v
        Mixing Stage
             |
             v
       Control Sequence
             |
             v
       Process Output
```

The exercise demonstrates how sequential PLC logic can be applied to automate a process involving multiple states and control actions.

---

# Ladder Logic

A major component of the repository is **Ladder Logic**, one of the standard graphical programming approaches used for PLCs.

Its structure is inspired by relay-based electrical-control diagrams.

Conceptually:

```text
|----[ Input ]----------------( Output )----|

|----[ Start ]----[/ Stop ]----( Motor )----|
```

PLC programs evaluate the logical conditions in the ladder and update the corresponding outputs.

---

# Inputs, Logic, and Outputs

PLC automation can be represented through three main stages:

```text
Physical Inputs
      |
      v
     PLC
      |
      v
 Control Program
      |
      v
Physical Outputs
```

Examples include:

```text
INPUTS                 OUTPUTS

Push buttons   --->    Motors
Sensors        --->    Lamps
Switches       --->    Contactors
Limits         --->    Actuators
```

The PLC program defines how the outputs react to the current input conditions and internal states.

---

# Sequential Control

Several projects in this repository focus on **sequential automation**.

A sequential process progresses through predefined states:

```text
State 1
   |
   v
State 2
   |
   v
State 3
   |
   v
State 4
```

Transitions may depend on:

```text
Timers
  |
Sensors
  |
Limits
  |
Buttons
  |
Internal PLC States
```

Traffic lights, gates, mixers, and industrial machines can all be represented using this approach.

---

# Industrial Automation Workflow

The exercises collectively demonstrate the general process of developing an automation solution:

```text
Physical Process
       |
       v
Define Inputs & Outputs
       |
       v
Design Control Sequence
       |
       v
Develop Ladder Logic
       |
       v
Configure Timers /
Sequencers / Subroutines
       |
       v
Simulation
       |
       v
Validate Sequence
       |
       v
Industrial Control Logic
```

---

# Software Used

## RSLogix 500

**RSLogix 500** was used for PLC Ladder Logic programming in several exercises contained in this repository.

The projects include `.RSS` PLC program files.

```text
Control Problem
      |
      v
RSLogix 500
      |
      v
Ladder Logic
      |
      v
PLC Program (.RSS)
```

---

## LogixPro

**LogixPro** was used to simulate and validate several PLC control sequences.

The simulations include traffic-light systems and other industrial-control exercises.

```text
PLC Program
     |
     v
LogixPro
     |
     v
Simulation
     |
     v
Observe Inputs / Outputs
     |
     v
Validate Control Logic
```

---

## CADe_SIMU

**CADe_SIMU** was used in the three-phase motor exercise to implement and simulate the electrical **power and control circuits**.

The exercise included:

- Start/stop control
- Direction reversal
- Signaling lamps
- Electrical protection

This complements PLC programming with traditional industrial electrical-control concepts.

---

# Project Files

The repository contains several types of files:

```text
.pdf
```

Technical reports documenting the exercises, simulations, and results.

```text
.RSS
```

PLC program files associated with RSLogix 500.

```text
.rsl
```

Files associated with the simulation exercises.

Together, these files preserve both the **implementation and documentation** of the automation exercises.

---

# Skills Developed

The projects in this repository provide practical experience in:

- PLC programming
- Ladder Logic
- Industrial automation
- Sequential control
- RSLogix 500
- LogixPro
- CADe_SIMU
- PLC timers
- Sequencers
- Bit-shift registers
- Subroutines
- JSR instructions
- Motor-control circuits
- Three-phase motor control
- Forward/reverse motor operation
- Electrical protection
- Traffic-light automation
- Process-control logic
- Industrial electrical diagrams
- Control-system simulation
- Troubleshooting and validation

---

# Relationship with Industrial IoT

PLC-based automation also provides an important foundation for **Industrial IoT (IIoT)** systems.

Traditional automation:

```text
Sensors
   |
   v
  PLC
   |
   v
Actuators
```

Industrial IoT extends this architecture:

```text
Sensors
   |
   v
PLC / Controller
   |
   v
Communication Network
   |
   v
Data Acquisition
   |
   v
Database / Cloud
   |
   v
Dashboard / Analytics
```

This relationship is particularly relevant to my later work integrating **PLC/Modbus systems, Raspberry Pi, Telegraf, InfluxDB, and Grafana** for industrial monitoring.

---

# Academic Context

These projects were developed as part of my academic training in **Automation and Programmable Logic Controllers** at:

**Universidad Autónoma de San Luis Potosí (UASLP)**  
**Facultad de Ciencias**  
San Luis Potosí, Mexico

The exercises combine theoretical industrial-control concepts with practical PLC programming and simulation.

---

# Repository Purpose

The purpose of this repository is to preserve and document my practical training in PLC programming and industrial automation.

The projects demonstrate a progression from electrical control fundamentals to structured PLC programming:

```text
Electrical Control
       |
       v
Motor & Actuator Control
       |
       v
PLC Fundamentals
       |
       v
Ladder Logic
       |
       v
Timers
       |
       v
Sequential Control
       |
       v
Sequencers
       |
       v
Bit-Shift Registers
       |
       v
Subroutines
       |
       v
Structured Industrial Automation
```

Together, these exercises provide practical foundations in **PLC programming, industrial control, sequential automation, and control-system simulation**.

---

# Author

**José Luis Romero Vázquez**

Electronics Engineer and Data Scientist with international graduate education in Electronic Engineering, Telecommunications, and Computer Networks, with experience in industrial automation, PLC/Modbus integration, IoT systems, Machine Learning, data analytics, and software development.

**LinkedIn:**  
https://www.linkedin.com/in/jose-luis-romero-vazquez-486569209

**GitHub:**  
https://github.com/0311869uaslp-a11y
