# **Complete 32-Hour Course Plan and Lecture Notes**

## **IEEE Std 7-4.3.2-2026: Programmable Digital Devices in Safety Systems of Nuclear Power Generating Stations**

# **32 hours**

**16 lectures · 2 hours per lecture · 4 training days**

Lectures

# **16**

Duration per lecture

# **120 min**

Practical exercises

# **8**

Final project

# **1**

Recommended professional training format

I recommend organizing the 16 lectures around the engineering lifecycle of a programmable digital device (PDD), rather than following the standard as a simple list of requirements.

The course will progress through:

1. Nuclear safety fundamentals and standards.
2. Safety requirements and system architecture.
3. Hardware, software, firmware, and programmable logic.
4. Verification, validation, and testing.
5. Reliability, qualification, and regulatory compliance.

The primary reference will be **IEEE Std 7-4.3.2-2026**, used together with IEEE Std 603. The 2026 edition is the main reference for programmable digital devices used in nuclear power plant safety systems.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://standards.ieee.org\&sz=32)

IEEE Standards Association+1



# **Part 1. Overall course structure**

## **1.1 Course syllabus**

| Unit | Lectures | Subject                                     | Hours  |
| ---- | -------- | ------------------------------------------- | ------ |
| I    | 1–3      | Introduction and standards framework        | 6      |
| II   | 4–6      | Safety requirements and system architecture | 6      |
| III  | 7–9      | Digital hardware engineering                | 6      |
| IV   | 10–12    | Software, firmware, and programmable logic  | 6      |
| V    | 13–14    | Verification, validation, and reliability   | 4      |
| VI   | 15–16    | Qualification and regulatory compliance     | 4      |
|      | **16**   | **Total**                                   | **32** |

## **1.2 Learning objectives**

After completing the course, students should be able to:

- Explain the role of programmable digital devices in nuclear safety systems.
- Understand the relationship between IEEE 603 and IEEE 7-4.3.2.
- Identify the engineering requirements for programmable digital devices.
- Understand digital hardware architectures and their safety implications.
- Explain software and firmware development assurance.
- Evaluate FPGA-based and processor-based implementations.
- Develop verification and validation plans.
- Identify systematic faults and common-cause failure mechanisms.
- Understand qualification and configuration management.
- Prepare a preliminary compliance assessment for a digital safety device.

## **1.3 Target audience**

- Nuclear instrumentation and control engineers.
- Electrical and electronics engineers.
- Computer and software engineers.
- Nuclear safety engineers.
- Digital systems designers.
- Nuclear regulatory personnel.
- Graduate students in nuclear engineering, electrical engineering, and computer science.

## **1.4 Recommended teaching methodology**

| Teaching method                         | Allocation |
| --------------------------------------- | ---------- |
| Technical lectures                      | 50%        |
| Engineering examples and demonstrations | 20%        |
| Practical exercises                     | 20%        |
| Discussions and knowledge checks        | 10%        |

Each two-hour lecture should contain:

**Standard lecture format**

Introduction and review

**10 min**

Main technical lecture

**55 min**

Engineering examples

**25 min**

Practical exercise or discussion

**25 min**

Summary and assessment

**5 min**

Total: 120 minutes

# **Part 2. Detailed lecture notes and teaching plan**

# **Unit I — Introduction and standards framework**

## **Lecture 1. Introduction to programmable digital devices in nuclear power plants**



2 hours

&#x20;FOUNDATION



**Lecture objective**

Understand programmable digital devices, their applications in nuclear power plants, and their importance to nuclear safety.

### **Lecture contents**

**1.1 Evolution of nuclear instrumentation and control systems — 20 min**

- Conventional analog I&C systems.
- Relay-based protection systems.
- Digital instrumentation and control.
- Microprocessor-based controllers.
- PLC-based control systems.
- FPGA-based safety systems.
- Digital modernization of existing nuclear power plants.

[File:Control room of Commonwealth Edison Company's Dresden nuclear power station.jpg - Wikimedia Commons](https://images.openai.com/static-rsc-4/OW--ThQ5vsNziHO-1AKNduZijltVo8MIv3_-4PKSiR2cIZkKsG-EUWNwKJqPectWY7klm7ICyi_jaeECt4wilVP1Z5IQWVlpOk3xi5XXukqeuFoO5qHpOOS-Zb9lTchltSB_CSqaiTKjHPQM9ZuCzfBUvSm0z8eI3j4IUhD07PA?purpose=inline)

[NUMAC Power Plant Monitors | GE Vernova Hitachi Nuclear Energy](https://images.openai.com/static-rsc-4/anojqgoEkQ32XnOZQ1nkKd-HIsyLNBmW9t1pcuwXmAM0CImhZIYurmdU4hgKJnDNffP7hCQz-I2FlUXRd4yVjI3T__EQzFDWC6VDLXckZ-_DuAG8voTRLsTse0tldh_aWsjHcknVj-AxH4Bai402c_02rFIJhdgsAAHMLeZSz1s?purpose=inline)

[广利核公司：科技自立自强推动高质量发展](https://images.openai.com/static-rsc-4/GeF7_Dvfg7lNG2O7hL-hw1DTW1eAE7ReiBf9xdVeJixOfhTgnH2giQUD6iyubcW6uufWcCgkf--ySz6PNR9Pn95VfVvKTJ8ZjxqodE3M055uNE-v4SX4SJe7oW8_q5R2skINzgHNCF7kLzWMB1Qxr_j3rELxe6LSx8h0G2ApIX4?purpose=inline)

12

**Instructor note:** Explain why nuclear facilities have progressively adopted digital technology. Discuss improved diagnostic capabilities, flexibility, maintainability, and the new assurance challenges associated with software and programmable logic.

**1.2 Definition and classification of programmable digital devices — 25 min**

Introduce the following categories:

| Category                   | Explanation                            | Example                       |
| -------------------------- | -------------------------------------- | ----------------------------- |
| Computer-based devices     | Execute instructions using a processor | Embedded safety computer      |
| Programmable logic devices | Implement configurable digital logic   | FPGA                          |
| PLC-based devices          | Execute industrial control programs    | Programmable controller       |
| Firmware-based devices     | Operate using embedded software        | Intelligent electronic device |

Explain the differences between:

- Hardware.
- Software.
- Firmware.
- Programmable logic.
- Configuration data.
- Development tools.

**1.3 Applications in nuclear power plants — 25 min**

Introduce:

- Reactor protection systems.
- Reactor trip systems.
- Engineered safety features actuation systems.
- Emergency core cooling system actuation.
- Safety-related monitoring.
- Safety-related interlocks.

[Full article: Proposal of quantification method of dynamic system reliability model of digital RPS using Markov state-transition model](https://images.openai.com/static-rsc-4/mjCqDf3_Ty1wTgWs-_JebdowQe5pIcCDzRj-dNBuXY6qBw8WlkXnAkjAZkJIY8IuvDrTWPE_5ZUWjvjZ2Xf0fkUQtJjO-K34CseCGqFC9m1yhZuo7DoqS2HGPtYuuVnFNmQQGmM5K0YCC_gtsTBji1wqlodJZbMapY3HYCcpUOU?purpose=inline)

[tandfonline.com](https://www.tandfonline.com/doi/full/10.1080/00223131.2023.2169379?utm_source=chatgpt.com)

**1.4 Safety implications of digital technology — 30 min**

Discuss:

- Hardware failures.
- Software defects.
- Incorrect system requirements.
- Common-cause failures.
- Configuration errors.
- Unexpected operating conditions.
- Dependence on software development tools.

**1.5 Exercise and discussion — 20 min**

Students classify five examples as hardware, software, firmware, programmable logic, or system-level functions.

**Expected learning output:** Students understand what constitutes a PDD and why its application in a nuclear safety system requires special engineering assurance.

## **Lecture 2. Nuclear safety principles and digital safety systems**



2 hours

&#x20;NUCLEAR SAFETY FOUNDATION



**Lecture objective**

Understand the fundamental nuclear safety principles that influence the design of programmable digital devices.

### **Lecture contents**

**2.1 Fundamental nuclear safety concepts — 20 min**

- Defense-in-depth.
- Safety functions.
- Safety classification.
- Single-failure considerations.
- Redundancy.
- Independence.
- Diversity.
- Fail-safe design concepts.

**2.2 Nuclear safety functions — 25 min**

Introduce the three fundamental safety functions:

1. Control of reactivity.
2. Removal of heat from the reactor and fuel.
3. Confinement of radioactive material.

Explain how I&C systems support these functions.

**2.3 Safety systems and non-safety systems — 25 min**

Compare:

| Safety-related systems                                  | Non-safety systems                                          |
| ------------------------------------------------------- | ----------------------------------------------------------- |
| Perform or support credited safety functions            | Support normal plant operation                              |
| Subject to safety classification and specific assurance | Subject to their applicable design and quality requirements |
| Require rigorous design verification and qualification  | Requirements depend on application and safety significance  |
| Interfaces require careful assessment                   | Must not adversely affect safety systems                    |

Clarify that a plant information system or historian is not automatically a safety system simply because it receives data from one.

**2.4 Digital safety-system architecture — 30 min**

[PPT - TKK automaatio -- Loviisan voimalaitos Loviisan uuden automaation arkkitehtuuri PowerPoint Presentation - ID:858632](https://images.openai.com/static-rsc-4/1qStIH7CjZcDGBV2FwoQUbAziBky7vM939WAWsTAecijZtvSnWpeD7BdwEQ79Toz-LUP9BX3Xvy0qmMNQFo0ALJC9YdN6SFL4xBnutGpPYIC1-hJGvqurZc1KtWdlMjOoqKtcYnFFsHydn-5Iol7aJjG7GJQj4bvmuXEJ5iK0wE?purpose=inline)

[slideserve.com](https://www.slideserve.com/melora/tkk-automaatio-loviisan-voimalaitos-loviisan-uuden-automaation-arkkitehtuuri?utm_source=chatgpt.com)

Explain:

- Redundant channels.
- Voting logic.
- Sensor interfaces.
- Processing units.
- Actuation interfaces.
- Separation and independence.
- Data communication between channels.

**2.5 Engineering discussion — 20 min**

Question:

Why might four identical digital channels still be vulnerable to a common software defect?

**Expected learning output:** Students understand the safety context in which IEEE 7-4.3.2 is applied.

## **Lecture 3. International standards and regulatory framework**



2 hours

&#x20;STANDARDS FRAMEWORK



**Lecture objective**

Understand the relationship between IEEE 7-4.3.2, IEEE 603, IEC standards, IAEA guidance, and national regulatory requirements.

### **Lecture contents**

**3.1 Structure of the international standards framework — 25 min**

- IAEA safety standards.
- IEEE standards.
- IEC standards.
- National regulatory requirements.
- Regulatory guidance.
- Industry practices.
- Plant-specific design specifications.

**3.2 IEEE 603 — 25 min**

*Criteria for Safety Systems for Nuclear Power Generating Stations.*

Teach:

- General safety-system design principles.
- Safety-system functional requirements.
- Independence and redundancy.
- Reliability.
- Testing and surveillance.
- Design verification.

**3.3 IEEE 7-4.3.2 — 30 min**

*Criteria for Programmable Digital Devices in Safety Systems of Nuclear Power Generating Stations.*

Teach:

- Why programmable devices need additional criteria.
- Scope of programmable digital devices.
- Relationship to the general safety-system criteria.
- Device-level digital engineering concerns.
- Development and assurance considerations.

**3.4 Supporting IEC and IAEA references — 20 min**

| Reference      | Main application                           |
| -------------- | ------------------------------------------ |
| IEC 61513      | Overall I&C systems important to safety    |
| IEC 61226      | Classification of I&C functions            |
| IEC/IEEE 60880 | Software for Category A functions          |
| IEC 62138      | Software for Category B and C functions    |
| IEC 60987      | Hardware aspects of computer-based systems |
| IEC 62566      | HDL-programmed devices                     |
| IAEA SSG-39    | I&C design guidance                        |

**3.5 Exercise: Standards applicability — 20 min**

Students are given a digital reactor protection controller and asked to identify the relevant standards.

**Expected learning output:** A preliminary standards applicability matrix.

# **Unit II — Safety requirements and system architecture**

## **Lecture 4. Safety classification and requirements engineering**



2 hours

&#x20;SYSTEM ENGINEERING



**Lecture objective**

Understand how nuclear safety requirements are translated into specific requirements for programmable digital devices.

### **Lecture contents**

**4.1 Safety classification — 20 min**

- Classification of safety functions.
- Safety categories.
- Safety classes.
- Relationship between function and equipment classification.
- Design implications of classification.

Introduce IEC 61226 and IAEA SSG-30.

**4.2 Functional requirements — 25 min**

- Safety function identification.
- Initiating conditions.
- Required response.
- Operating modes.
- Input and output definitions.
- Functional boundaries.

**4.3 Performance requirements — 25 min**

- Response time.
- Accuracy.
- Processing time.
- Signal ranges.
- Availability.
- Reliability.
- Data integrity.
- Environmental operating conditions.

**4.4 Requirements engineering lifecycle — 30 min**

[Live Traceability in Systems Engineering - Jama Software](https://images.openai.com/static-rsc-4/eGGnazln_0XKgyeL-3BDGM9E6mVi7cMrnG0DA5ZCsxCDX6iNg8jK0Os6Vuq9zI_MNu3RjCY_5Wtt1lMpUGo7YU8JgzLnzF-9EBYd29GI2cSl1vid4tTkom-blIotINhZD3UlDidyBo8zaothLlsARs04ntuai3NPSOUWPpuPjSA?purpose=inline)

[jamasoftware.com](https://www.jamasoftware.com/blog/how-to-use-requirements-management-as-an-anchor-to-establish-live-traceability-in-systems-engineering/?utm_source=chatgpt.com)

Teach:

1. Requirements identification.
2. Requirements analysis.
3. Requirements allocation.
4. Requirements specification.
5. Requirements verification.
6. Requirements traceability.
7. Requirements change management.

**4.5 Practical exercise — 20 min**

Develop a device requirements specification for a fictional reactor protection controller.

**Expected learning output:** A preliminary requirements specification and traceability matrix.

## **Lecture 5. Digital safety-system architecture and independence**



2 hours

&#x20;SYSTEM ARCHITECTURE



**Lecture objective**

Understand the architectural principles required to ensure that programmable digital devices support the intended safety functions without compromising system independence.

### **Lecture contents**

**5.1 Digital safety-system architecture — 25 min**

- Centralized versus distributed architecture.
- Processor-based systems.
- Distributed I&C systems.
- Modular architecture.
- Channel architecture.
- Interface architecture.

**5.2 Redundancy and voting logic — 25 min**

[Принцип работы архитектуры голосования в  СПАЗ: 2oo4D — Дмитрий  Косьянчик на TenChat.ru](https://images.openai.com/static-rsc-4/pWpCSC7gsppV-AWfei7VdU76UIGWgQZG-bK6zxPYh3l2PzDqyDICf8W9WkwD3k3ZP5dOeJnXgldUy0ecJb2gknKqtXu7xH2boutAQ7ChjZdAgBz3h46zbIj84Ywg1nOxUJdTKX3XDAMWiwuRtUtCJ2tc2N9f5OO6Y1o2GTuLNgA?purpose=inline)

[tenchat.ru](https://tenchat.ru/media/3960845-printsip-raboty-arkhitektury-golosovaniya-v--spaz-2oo4d?utm_source=chatgpt.com)

Explain:

- Single-channel logic.
- Dual-channel logic.
- Triple Modular Redundancy.
- Two-out-of-three voting.
- Two-out-of-four voting.
- Fault detection.
- Channel isolation.

Use voting logic examples to teach the underlying concepts, without implying that any particular voting arrangement is universally suitable.

**5.3 Independence and separation — 25 min**

- Physical separation.
- Electrical separation.
- Functional independence.
- Communication isolation.
- Power supply separation.
- Protection against adverse interactions.

**5.4 Diversity and defense-in-depth — 25 min**

- Identical versus diverse hardware.
- Software diversity.
- Functional diversity.
- Diverse actuation systems.
- Independent backup protection.
- Common-cause failure considerations.

**5.5 Practical exercise — 20 min**

Students evaluate a simplified four-channel architecture and identify potential common dependencies.

**Expected learning output:** A digital safety-system architecture assessment.

## **Lecture 6. Safety-system interfaces and communication architecture**



2 hours

&#x20;INTERFACES AND COMMUNICATION



**Lecture objective**

Understand the design and safety implications of interfaces between programmable devices and other nuclear plant systems.

### **Lecture contents**

**6.1 Input interfaces — 20 min**

- Analog sensor signals.
- Digital sensor signals.
- Signal conditioning.
- Electrical isolation.
- Input validation.
- Sensor diagnostics.

**6.2 Output interfaces — 20 min**

- Digital actuation signals.
- Relay interfaces.
- Output drivers.
- Output monitoring.
- Fail-safe output considerations.

**6.3 Digital communication — 25 min**

- Serial communication.
- Ethernet.
- Fieldbus technologies.
- Data protocols.
- Message integrity.
- Communication timing.
- Loss of communication.

**6.4 Safety and non-safety system interfaces — 25 min**

[Owl DualDiode│事例：原子力発電 - 日本ダイレックス](https://images.openai.com/static-rsc-4/KwhMQBE7-55bw6SRVVQ6KqfgglLGMa3kPLk-5yN9NEY15lgnMLbPS4jkDZcJ794MnHEa3gij-VrIE6ioxxFmkCeiNZeJpqWjTW-o-pYX4FPo8jNbdWmAPWh80ImcjucQd2MZgM_2FEy6ZL2Ny58VckbNdLLen4VpL5ocKeuB730?purpose=inline)

[direx.com](https://www.direx.com/product.dualdiode_uc_nuclear-power.html?utm_source=chatgpt.com)

Discuss:

- Safety-to-non-safety data exchange.
- Interface isolation.
- Communication direction.
- Data transfer mechanisms.
- Potential adverse interactions.
- Network segmentation.
- Cybersecurity implications.

**6.5 Practical exercise — 20 min**

Assess a proposed data interface between a safety system and a plant information system.

**Expected learning output:** An interface assessment checklist and architecture diagram.

# **Unit III — Digital hardware engineering**

## **Lecture 7. Processor-based digital device hardware**



2 hours

&#x20;HARDWARE ENGINEERING



**Lecture objective**

Understand the hardware architecture and design considerations of processor-based programmable digital devices.

### **Lecture contents**

**7.1 Computer architecture fundamentals — 25 min**

[임베디드 시스템 소개 초보자를 위한 빠른 가이드](https://images.openai.com/static-rsc-4/hOs0v3iH7rh5sf9x4FVWQwbraVyfLFgsKtERxlQ0ZLCf0CVx9BLLBoawsxu146U94FGtX7PVVbiDZWo8sY8-hhc_N8v1cBWMOJzvk_knyk3u-qRt03xpaHU7yYr2n0eq2KjnkFP7zuJcdOKy9ysGJFolpnkjSkPonK2hYB8dz5c?purpose=inline)

[ko.mfgrobots.com](https://ko.mfgrobots.com/mfg/it/1008029079.html?utm_source=chatgpt.com)

- CPU architecture.
- Instruction execution.
- Registers.
- Memory.
- Data buses.
- Interrupts.
- Clock systems.

**7.2 Memory and data integrity — 20 min**

- RAM.
- ROM.
- Flash memory.
- Memory corruption.
- Parity checking.
- Error-correcting codes.
- Memory protection.
- Program integrity.

**7.3 Processor diagnostics — 20 min**

- Watchdog timers.
- Built-in self-test.
- Processor monitoring.
- Clock monitoring.
- Fault detection.
- Diagnostic reporting.

**7.4 Hardware fault handling — 25 min**

- Fault detection.
- Fault isolation.
- Recovery.
- Safe-state considerations.
- Hardware failure propagation.
- Redundant hardware.

**7.5 Practical exercise — 30 min**

Students review a simplified embedded controller architecture and identify critical hardware components and potential failure points.

**Expected learning output:** Hardware design review checklist.

## **Lecture 8. FPGA and programmable logic devices**



2 hours

&#x20;PROGRAMMABLE HARDWARE



**Lecture objective**

Understand the architecture, design process, and assurance challenges of FPGA-based programmable digital devices.

### **Lecture contents**

**8.1 Introduction to programmable logic — 20 min**

- Programmable logic devices.
- CPLDs.
- FPGAs.
- Application-specific integrated circuits (ASICs).
- Processor versus FPGA architecture.

**8.2 FPGA internal architecture — 25 min**

[FPGA Architecture: A Comprehensive Guide for Digital Design Engineers](https://images.openai.com/static-rsc-4/rHnuZMnbB3K0DJZR6M5YDAbmaUe5Mm85lYtJxENODEZvZTIkHntfqfcMzG0pj4gVB1hFwvE4U-YrjUX4MFA1qVnffSj4UJLQVc5g_1vnroys_AbVlkyAMirN6kudp6edNU4cw0mQF91BGdQkyX1upP2QLY6M_qDNpIpYNPUBuWU?purpose=inline)

[wevolver.com](https://www.wevolver.com/article/fpga-architecture-a-comprehensive-guide-for-digital-design-engineers?utm_source=chatgpt.com)

- Configurable logic blocks.
- Lookup tables.
- Flip-flops.
- Routing resources.
- Input/output blocks.
- Clock management.

**8.3 Hardware description languages — 20 min**

- VHDL.
- Verilog.
- RTL design.
- Combinational logic.
- Sequential logic.
- State machines.

**8.4 FPGA development lifecycle — 25 min**

[PPT - Xilinx Design Flow PowerPoint Presentation, free download - ID:3894686](https://images.openai.com/static-rsc-4/BQALNADwf-ak691f5y-z-Hp423fa9RuNFkjEDejoRHJrwbTaEYlEmZKHT7NEdQE2-lmLxq0777IIUNgCT1OVPkORN-7XrguoLAQg26wF_NEi5FpqKn5wzfQ37jrzJ7KjKvKBmXdAcHTa7cBi3EyPIMuYfePxSqVfN8LY7bY8kmI?purpose=inline)

[slideserve.com](https://www.slideserve.com/chynna/xilinx-design-flow?utm_source=chatgpt.com)

- Requirements.
- RTL design.
- Simulation.
- Synthesis.
- Place and route.
- Timing analysis.
- Configuration generation.
- Verification.

**8.5 FPGA assurance considerations — 20 min**

- Design complexity.
- Toolchain dependence.
- Timing behavior.
- Logic verification.
- Configuration management.
- Design review.
- Testing and qualification.

**8.6 Practical exercise — 10 min**

Students compare a processor-based implementation with an FPGA-based implementation for a hypothetical protection function.

**Expected learning output:** FPGA design and assurance comparison.

## **Lecture 9. Hardware reliability, environmental conditions, and diagnostics**



2 hours

&#x20;HARDWARE ASSURANCE



**Lecture objective**

Understand how hardware design and operating conditions influence the reliability and qualification of programmable digital devices.

### **Lecture contents**

**9.1 Hardware reliability — 20 min**

- Random hardware failures.
- Component degradation.
- Reliability concepts.
- Failure rates.
- Hardware redundancy.
- Maintainability.

**9.2 Environmental conditions — 25 min**

- Temperature.
- Humidity.
- Vibration.
- Radiation.
- Seismic conditions.
- Electromagnetic interference.
- Electrical disturbances.

**9.3 Electromagnetic compatibility — 20 min**

- EMI and EMC fundamentals.
- Conducted interference.
- Radiated interference.
- Grounding and shielding.
- Power quality.
- Equipment susceptibility.

**9.4 Hardware diagnostics — 20 min**

- Continuous monitoring.
- Built-in self-test.
- Memory diagnostics.
- Power supply monitoring.
- Input/output monitoring.
- Fault annunciation.

**9.5 Failure analysis — 20 min**

- Failure Modes and Effects Analysis.
- Failure detection.
- Fault isolation.
- Failure propagation.
- Diagnostic coverage.

**9.6 Practical exercise — 15 min**

Students prepare a simplified hardware FMEA.

**Expected learning output:** Preliminary hardware reliability and environmental assessment.

# **Unit IV — Software, firmware, and programmable logic assurance**

## **Lecture 10. Software engineering lifecycle for nuclear safety systems**



2 hours

&#x20;SOFTWARE ENGINEERING



**Lecture objective**

Understand how software is developed and controlled for safety-related programmable digital devices.

### **Lecture contents**

**10.1 Software development lifecycle — 25 min**

[howcomputerprogrammerswork.com](https://howcomputerprogrammerswork.com/book/Safety-critical-programming.html?utm_source=chatgpt.com)

- Requirements definition.
- Architecture.
- Detailed design.
- Implementation.
- Verification.
- Integration.
- Validation.
- Maintenance.

**10.2 Software requirements specification — 20 min**

- Functional requirements.
- Timing requirements.
- Data requirements.
- Operating modes.
- Interfaces.
- Error handling.
- Requirements traceability.

**10.3 Software architecture and design — 20 min**

- Software decomposition.
- Modules.
- Interfaces.
- Data flow.
- Control flow.
- Design documentation.
- Complexity management.

**10.4 Software implementation — 20 min**

- Programming languages.
- Coding standards.
- Structured programming.
- Defensive programming.
- Code review.
- Static analysis.

**10.5 Software quality assurance — 20 min**

- Quality plans.
- Independent review.
- Development records.
- Defect management.
- Version control.
- Release approval.

**10.6 Exercise — 15 min**

Review a sample software lifecycle and identify missing assurance activities.

**Expected learning output:** Software lifecycle assurance checklist.

## **Lecture 11. Firmware, FPGA logic, and development tools**



2 hours

&#x20;DIGITAL IMPLEMENTATION



**Lecture objective**

Understand the development and assurance of embedded firmware and programmable logic, including the tools used to create them.

### **Lecture contents**

**11.1 Firmware architecture — 20 min**

- Embedded firmware.
- Bootloaders.
- Operating systems.
- Real-time operating systems.
- Device drivers.
- Firmware interfaces.

**11.2 Firmware development and control — 20 min**

- Firmware requirements.
- Implementation.
- Verification.
- Version control.
- Configuration management.
- Installation and updates.

**11.3 FPGA logic development — 25 min**

- HDL coding.
- Simulation.
- Synthesis.
- Timing analysis.
- Logic verification.
- Configuration files.

**11.4 Development tools and toolchain — 25 min**

[Introduction to the LLVM for a iOS Engineer | by Julie Yaunches | Medium](https://images.openai.com/static-rsc-4/LMYaMbed8B4VzRnBQh5w3TWVPZr7hFYxAe7pM3Mutehh7BnR4UyGZEkH_zHtk_yafIM1x9Ftsh-0hD3WdBk5stIbWughBuCBVMNc5K4i2W8HVFGvV-6e1RrC12BaRL063wenoZv9y3EMfRvZxRo9ryx8JbUiAUPRTVFPot-R7Yk?purpose=inline)

[medium.com](https://medium.com/%40jyaunches/introduction-to-the-llvm-for-a-ios-engineer-8c00ed0f9ff0?utm_source=chatgpt.com)

- Compilers.
- Linkers.
- Debuggers.
- FPGA synthesis tools.
- Simulation tools.
- Static analysis tools.
- Test automation tools.
- Configuration management tools.

**11.5 Tool assurance — 20 min**

Discuss:

- Tool failure.
- Incorrect tool output.
- Tool verification.
- Tool validation.
- Tool qualification or assurance approaches.
- Independent checks.
- Reproducible builds.

**11.6 Exercise — 10 min**

Students identify potential risks in an FPGA and firmware development toolchain.

**Expected learning output:** Toolchain assurance checklist.

## **Lecture 12. Software verification, systematic faults, and configuration management**



2 hours

&#x20;SOFTWARE ASSURANCE



**Lecture objective**

Understand how software-related systematic failures are identified, prevented, and controlled.

### **Lecture contents**

**12.1 Systematic failures — 25 min**

- Requirements errors.
- Design errors.
- Coding errors.
- Incorrect assumptions.
- Boundary-condition errors.
- Unexpected operating conditions.

**12.2 Software verification — 25 min**

- Requirements reviews.
- Design reviews.
- Code reviews.
- Static analysis.
- Unit testing.
- Integration testing.
- Regression testing.

**12.3 Software testing methods — 20 min**

- Functional testing.
- Boundary testing.
- Robustness testing.
- Stress testing.
- Timing testing.
- Fault-injection testing.
- Requirements-based testing.

**12.4 Configuration management — 25 min**

- Source code baselines.
- Firmware versions.
- FPGA configuration files.
- Compiler versions.
- Development environment.
- Change requests.
- Impact analysis.
- Release management.

**12.5 Practical exercise — 25 min**

Students review a fictional software change request for a digital protection controller.

They must identify:

- The reason for the change.
- Affected requirements.
- Affected components.
- Verification needed.
- Regression testing needed.
- Approval and release evidence.

**Expected learning output:** Software change-control assessment.

# **Unit V — Verification, validation, and reliability**

## **Lecture 13. Verification, validation, integration, and acceptance testing**



2 hours

&#x20;TESTING AND VALIDATION



**Lecture objective**

Develop an understanding of the testing and verification activities needed to demonstrate that a programmable digital device meets its requirements.

### **Lecture contents**

**13.1 Verification and validation concepts — 20 min**

- Verification.
- Validation.
- Independent verification.
- Requirements traceability.
- Acceptance criteria.

**13.2 Testing hierarchy — 25 min**

1. Unit testing.
2. Integration testing.
3. Hardware/software integration testing.
4. System testing.
5. Acceptance testing.

**13.3 Testing methods — 20 min**

- Functional testing.
- Performance testing.
- Timing testing.
- Boundary testing.
- Robustness testing.
- Fault-injection testing.
- Regression testing.

**13.4 Test coverage — 15 min**

- Requirements coverage.
- Test-case coverage.
- Code coverage.
- Logic coverage.
- Test completeness.

Explain why coverage metrics alone cannot prove the absence of systematic faults.

**13.5 FAT and SAT — 15 min**

- Factory acceptance testing.
- Site acceptance testing.
- Test equipment.
- Test procedures.
- Test configuration.
- Test reports.
- Defect resolution.

**13.6 Practical exercise — 25 min**

Students prepare a test matrix for a digital protection controller.

**Expected learning output:** Verification and validation plan.

## **Lecture 14. Digital reliability, common-cause failure, and diversity**



2 hours

&#x20;RELIABILITY ENGINEERING



**Lecture objective**

Understand the reliability challenges of programmable digital devices and the impact of systematic failures on redundant safety systems.

### **Lecture contents**

**14.1 Hardware and software reliability — 20 min**

- Random hardware failures.
- Systematic software faults.
- Hardware degradation.
- Fault detection.
- Diagnostic coverage.
- Reliability assessment limitations.

**14.2 Common-cause failure — 25 min**

[INSIDE THE BRAIN OF A NUCLEAR REACTOR: SAFETY BY DESIGN | by Gökhan Kurtkaya | Nuclear I&C Systems & Safety | Medium](https://images.openai.com/static-rsc-4/gXCW8pLVK8tnA77M6NXWW63fYgqAkMMet_13tycJBLqCPQdsipmURM90Ysl2KObe9stat60fRuo5Dvrj3p50CyoL6LXGzHWkX6MUwmU45u47IyFVUoIINFcpCZmsxm_Me5VhLYYZ233PeeHms3p6KrHaaQE0TUTzRg2TH9C9RPo?purpose=inline)

[medium.com](https://medium.com/nuclear-i-c-systems-safety/inside-the-brain-of-a-nuclear-reactor-safety-by-design-a40c6c4f5967?utm_source=chatgpt.com)

Explain how identical devices can be affected by the same underlying design defect.

Examples:

- Shared software.
- Common requirements.
- Identical development tools.
- Shared hardware design.
- Common power sources.
- Common interfaces.

**14.3 Diversity and defense-in-depth — 20 min**

- Hardware diversity.
- Software diversity.
- Functional diversity.
- Independent backup systems.
- Diverse actuation.
- Defense-in-depth.

**14.4 Failure analysis techniques — 25 min**

- FMEA.
- Fault Tree Analysis.
- Hazard analysis.
- Failure propagation analysis.
- Common-cause failure analysis.

**14.5 Reliability case study — 30 min**

Students examine a fictional four-channel protection system and identify how a single systematic defect could affect multiple channels.

**Expected learning output:** Preliminary reliability and common-cause failure assessment.

# **Unit VI — Qualification and regulatory compliance**

## **Lecture 15. Equipment qualification and lifecycle management**



2 hours

&#x20;QUALIFICATION



**Lecture objective**

Understand how programmable digital devices are assessed for suitability under their intended installation and operating conditions.

### **Lecture contents**

**15.1 Qualification fundamentals — 20 min**

- Equipment qualification.
- Qualification basis.
- Qualification evidence.
- Design verification.
- Functional validation.
- Qualification boundaries.

**15.2 Environmental qualification — 25 min**

- Temperature.
- Humidity.
- Radiation.
- Vibration.
- Seismic requirements.
- Aging.
- Service conditions.

**15.3 Electromagnetic compatibility and electrical qualification — 20 min**

- EMC testing.
- Electrical disturbances.
- Power supply variation.
- Grounding.
- Shielding.
- Immunity testing.

**15.4 Procurement and supplier qualification — 20 min**

- Supplier quality assurance.
- Procurement specifications.
- Supplier documentation.
- Commercial-grade equipment.
- Product traceability.
- Acceptance activities.

**15.5 Lifecycle management — 20 min**

- Installation.
- Commissioning.
- Operation.
- Maintenance.
- Periodic testing.
- Modification.
- Obsolescence management.

**15.6 Exercise — 15 min**

Students prepare a qualification evidence checklist for a hypothetical embedded digital controller.

**Expected learning output:** Equipment qualification and lifecycle management checklist.

## **Lecture 16. Regulatory compliance and integrated case study**



2 hours

&#x20;FINAL ENGINEERING ASSESSMENT



**Lecture objective**

Bring together all previous lectures to demonstrate how the engineering evidence for a programmable digital device can be assessed against applicable nuclear safety criteria.

### **Lecture contents**

**16.1 Compliance assessment methodology — 20 min**

- Identify applicable requirements.
- Establish compliance criteria.
- Identify required evidence.
- Review design documentation.
- Review verification and qualification records.
- Identify gaps.
- Record findings.

**16.2 Regulatory documentation — 20 min**

Introduce:

- System design descriptions.
- Safety analysis documentation.
- Device requirements specifications.
- Hardware design documents.
- Software lifecycle records.
- V&V reports.
- Qualification reports.
- Configuration management records.

**16.3 Case study: Digital reactor protection controller — 40 min**

[ПАО "Приборный завод "Сигнал" | Комплексная система контроля, управления и защиты (КСКУЗ)](https://images.openai.com/static-rsc-4/c4sXdp8UOZ3fS96mMZvRfQysWnxAB94DwR5siPeLS2yGSDmT6c0AdNR6UnA8To0hfcfk7pMiagrwD_mHUMBWCDxmYVqav1YVMCc3Hc8wSaToGxUnJu-CaiNRTicjE-QHGdbsTe3wvVrL7_BOVtdXrfYFBfobbX-uCKK03ngTSao?purpose=inline)

[pz-signal.ru](https://pz-signal.ru/products/detail/Kompleksnaya-sistema-kontrolya-upravleniya-i-zashchity?utm_source=chatgpt.com)

Scenario:

A nuclear power plant proposes replacing a conventional analog protection subsystem with a programmable digital controller.

Students receive a fictional project package containing:

- System functional requirements.
- Device architecture.
- Hardware description.
- Software description.
- FPGA or firmware information.
- Test records.
- Qualification information.

Students must evaluate:

1. Requirements completeness.
2. Architecture and independence.
3. Hardware design assurance.
4. Software and firmware lifecycle.
5. Verification and validation.
6. Reliability and common-cause failure.
7. Qualification evidence.
8. Configuration management.

**16.4 Group presentation — 20 min**

Each group presents its findings and outstanding issues.

**16.5 Final examination and course review — 20 min**

- Review key concepts.
- Individual knowledge examination.
- Course evaluation.
- Final discussion.

**Expected learning output:** A preliminary compliance assessment report.

# **Part 3. Four-day teaching schedule**

The following schedule allocates eight hours of instruction per day. Breaks are additional.

## **Day 1 — Nuclear safety and standards**

6 hours of lectures

| Session | Lecture                            | Duration |
| ------- | ---------------------------------- | -------- |
| 1       | Introduction to PDDs               | 2 h      |
| 2       | Nuclear safety principles          | 2 h      |
| 3       | Standards and regulatory framework | 2 h      |

Additional 2 hours: opening, breaks, discussion, and review.

## **Day 2 — Requirements and hardware architecture**

6 hours of lectures

| Session | Lecture                                | Duration |
| ------- | -------------------------------------- | -------- |
| 4       | Safety classification and requirements | 2 h      |
| 5       | Digital safety-system architecture     | 2 h      |
| 6       | Interfaces and communication           | 2 h      |

Additional 2 hours: practical workshop, breaks, and review.

## **Day 3 — Hardware and software engineering**

6 hours of lectures

| Session | Lecture                              | Duration |
| ------- | ------------------------------------ | -------- |
| 7       | Processor-based hardware             | 2 h      |
| 8       | FPGA and programmable logic          | 2 h      |
| 9       | Hardware reliability and diagnostics | 2 h      |

Additional 2 hours: hardware architecture workshop, breaks, and review.

## **Day 4 — Software assurance and qualification**

8 hours of lectures

| Session | Lecture                                 | Duration |
| ------- | --------------------------------------- | -------- |
| 10      | Software engineering lifecycle          | 2 h      |
| 11      | Firmware, FPGA tools, and toolchain     | 2 h      |
| 12      | Software verification and configuration | 2 h      |
| 13      | V&V and testing                         | 2 h      |

Lectures 14–16 are delivered on a fifth day in this arrangement.

**Correction to the four-day allocation:** The six-unit syllabus contains 16 lectures, so it needs a fifth teaching day if every lecture is delivered for two hours. The correct full schedule is:

| Day       | Lectures | Instruction hours |
| --------- | -------- | ----------------- |
| Day 1     | 1–3      | 6                 |
| Day 2     | 4–6      | 6                 |
| Day 3     | 7–9      | 6                 |
| Day 4     | 10–12    | 6                 |
| Day 5     | 13–16    | 8                 |
| **Total** | **16**   | **32**            |

I recommend the five-day arrangement for a professional course because it gives the students more time to absorb the technical content and complete the exercises.

# **Part 4. Practical exercise and project package**

I recommend using one continuing project across the course.

## **Main project: Design assurance of a digital reactor protection controller**

[PPT - A Safety-Critical Software Approach to Hard Real-Time Applications PowerPoint Presentation - ID:6985490](https://images.openai.com/static-rsc-4/bBjhv5xK2g8iJMy0WlHxSS1xaQ-q7X1BoFD39nSkOa0-UJr9rbC8hmFlRDCNg2srVHE16vVPphPWhWjU1WJ-n_A_gRRV5imMeAJo2Y8GtviMw0_yzGhL5RiFeNuNrTBaoAw9mBzGAWmrFKCPdCTdW_KWv3fr86b5t-zl_1y2N7g?purpose=inline)

[slideserve.com](https://www.slideserve.com/sterling-channing/a-safety-critical-software-approach-to-hard-real-time-applications?utm_source=chatgpt.com)

Students will work in groups of three or four.

### **Project tasks**

| Lecture | Practical task                 | Deliverable                    |
| ------- | ------------------------------ | ------------------------------ |
| 1       | Identify device types          | Device classification          |
| 2       | Identify safety functions      | Safety-function description    |
| 3       | Identify standards             | Standards applicability matrix |
| 4       | Define device requirements     | Requirements specification     |
| 5       | Review system architecture     | Architecture diagram           |
| 6       | Evaluate interfaces            | Interface assessment           |
| 7       | Review processor hardware      | Hardware checklist             |
| 8       | Compare FPGA and processor     | Technology comparison          |
| 9       | Conduct hardware FMEA          | Failure analysis               |
| 10      | Review software lifecycle      | Software assurance plan        |
| 11      | Review toolchain               | Tool assurance checklist       |
| 12      | Assess software changes        | Configuration plan             |
| 13      | Prepare testing plan           | V&V matrix                     |
| 14      | Analyze common-cause failure   | Reliability assessment         |
| 15      | Prepare qualification evidence | Qualification checklist        |
| 16      | Complete compliance assessment | Final engineering report       |

### **Final student submission**

Each group submits:

1. Safety-function description.
2. Standards applicability matrix.
3. Device requirements specification.
4. Hardware architecture diagram.
5. Software and firmware assurance plan.
6. Verification and validation plan.
7. Preliminary FMEA.
8. Qualification evidence checklist.
9. Compliance assessment report.

# **Part 5. Course assessment**

| Assessment component                      | Weight   |
| ----------------------------------------- | -------- |
| Individual examination                    | 20%      |
| Requirements and architecture exercises   | 20%      |
| Hardware and software assurance exercises | 20%      |
| V&V and reliability exercises             | 15%      |
| Final group project                       | 25%      |
| **Total**                                 | **100%** |

Suggested final examination: 20 questions, including multiple-choice, short-answer, and engineering scenario questions.

# **Part 6. Recommended reference materials**

These are the core references I would include in the official course reading list.

## **A. Primary IEEE standards**

| Standard          | Course application              |
| ----------------- | ------------------------------- |
| IEEE 7-4.3.2-2026 | Main reference for all lectures |
| IEEE 603-2018     | Lectures 2–6 and 14–16          |

Official references:

- [IEEE 7-4.3.2-2026](https://standards.ieee.org/ieee/7-4.3.2/7407/?utm_source=chatgpt.com)
- [IEEE 603-2018](https://standards.ieee.org/ieee/603/6086/?utm_source=chatgpt.com)

## **B. Supporting IEC standards**

| Standard            | Subject                                  |
| ------------------- | ---------------------------------------- |
| IEC 61513           | I&C systems important to safety          |
| IEC 61226           | Safety classification of I&C functions   |
| IEC/IEEE 60880-2026 | Software for Category A functions        |
| IEC 62138:2018      | Software for Category B and C functions  |
| IEC 60987:2021      | Hardware requirements                    |
| IEC 62566           | HDL-programmed devices                   |
| IEC 61500           | Data communication in Category A systems |

## **C. IAEA publications**

| Publication | Subject                              |
| ----------- | ------------------------------------ |
| SSG-39      | I&C system design                    |
| SSG-30      | Safety classification                |
| SSG-51      | Human factors engineering            |
| SSG-69      | Equipment qualification              |
| GSR Part 2  | Leadership and management for safety |

IAEA publications are particularly valuable for student reading because many are publicly accessible.

- [IAEA SSG-39](https://nucleus.iaea.org/sites/nss-oui/Published%20Collections/m_3df5a9eb-7e9b-4968-a0d6-4864db84d434/m_3df5a9eb-7e9b-4968-a0d6-4864db84d434__18_0.Html?utm_source=chatgpt.com)
- [IAEA NSS 17-T](https://nucleus.iaea.org/sites/nss-oui/Published%20Collections/m_e3cff0f5-af02-4237-a0b0-648f5d703c1e/m_e3cff0f5-af02-4237-a0b0-648f5d703c1e__3_0.Html?utm_source=chatgpt.com)
- [IAEA equipment qualification reference](https://nucleus.iaea.org/sites/committees/Shared%20Documents/status.pdf?utm_source=chatgpt.com)

# **Part 7. Preparation of the actual teaching package**

For your institute, I would produce the following documents as a consistent course package.

**Recommended course-material package**

**16 lecture slide decks**

Approximately 20–30 slides per lecture

**Instructor lecture notes**

Detailed explanations, examples, diagrams, and speaking notes

**Student handout**

Definitions, summaries, exercises, and reading assignments

**Practical exercise workbook**

Eight structured engineering exercises and answer guidance

**Assessment package**

Question bank, final examination, marking rubric, and project evaluation

## **Suggested production sequence**

I would prepare the material in this order:

1. Lectures 1–3: Establish the nuclear safety and standards foundation.
2. Lectures 4–6: Develop the safety requirements and system architecture.
3. Lectures 7–9: Explain hardware and programmable logic.
4. Lectures 10–12: Cover software and firmware assurance.
5. Lectures 13–16: Complete testing, reliability, qualification, and compliance.

**My recommendation for your institute:** Make the 32-hour course the core professional training course for digital nuclear safety systems. Then offer separate advanced courses on FPGA engineering for nuclear applications, safety-critical software assurance, and nuclear I&C cybersecurity. This creates a coherent training pathway rather than trying to cover every digital nuclear engineering topic in one course.