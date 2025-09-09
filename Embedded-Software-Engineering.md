# Embedded Software Engineering

---
#### **[⇐ Embedded Systems](./README.md)**
---

### Steps

#### Code Design and Architecture

- Flow Diagram: A flow diagram can depict, how a particular piece of software or algorithm should behave
    - Algorithm based
    - Shows functional behavior
    - Conditional decisions
    - High-level function calls

- Software blocks :  Depict how different blocks of code communicate and connect to one another. A Software Block Diagram can also depict a software system in layers.
    - C-files are "modules"
    - Many definitions
    - Functions interact with other modules
    - Eventually interact with Hardware

    ![Software Block Diagram](Images/Software-Block-Diagram.jpg)

### Software in Layers
* **Device Drivers** (Low level software)
    - Interface to hardware layers
    - HAL - Hardware Abstraction Layer
* **Bootloader**
    - Software that boots or starts the system
* **Operating System (OS)**
    - Abstracts High from Low levels
    - Scheduling
    - Resource management
* **Libraries** for shared code
* **User Application** (High level software)

    ![OS-Based Design](Images/OS-Based-Design.jpg)

### Hardware Abstraction

**Bare-metal Firmware (FW)**
- Software that directly interacts with hardware.
- Low level control

**Hardware Abstraction Layer (HAL)**
- Segmenting hardware interface
- Allows the application layer developer to write platform independent code.
- Portable interface


### Software Block design
* Component design
    - Defines small functional software blocks that have certain tasks, along with interface mechanism and the specs each modules must follow.
    - Helps building modulized software that is reusable  across different systems, architectures and platforms, allowing easy migration of certain software solutions without significant system changes.
    - Layers:
        - **Hardware Firmware Layer** - Controls peripheral hardware
            - **Extracted Interface** - Hardware independent
        - **High-level Communication Library Interfaces**
        - **Control Library** - Utilizes hardware interfaces

![Software Component Design](Images/Component-design.jpg)

### On-target Testing
On-target testing is installing code on to particular embedded system instead of another.

### Software Engineer Tools
[Embedded Software Engineering Tools](Tools/README.md#software-engineer-tools).

### Principles of High Quality Software

Build and design embedded software that is:

 - Maintainable
 - Testable
 - Portable
 - Robust
 - Efficient
 - Consistent
 
Keeping these in mind helps to write better code, speed up development by using all code and produce system bug free software.

### Programming Languages
[Programming languages used in embedded engineering](Tools/README.md#languages).


---


## Software Configuration Management | SCM

Software configuration management or SCM is a process used by software teams to develop software projects.

This process contains a diverse set of goals and guidelines that dictate the software processes for-

--- 
<sub>[Used directly by software engineers in development]<sub>

* **Software Requirements** - Software teams will use Version Control and Software Review along with specific coding standards, as the methodology for software code storage and change requirements.
* **Environment Information** (IDEs, toolchains, simulators, Docker)
* **Software Build and Release** (Tools: GNU Make/CMake/SCons, GCC)

* **Software Review** - usually combined with version control as a way to prevent poorly designed software contributions into a project.
* **Version control** (Git, SVN, Mercurial) - Allows to track all the changes made to a software project indefinitely

---
<sub>[Used to help organize and support software projects]<sub>
* **Testing**
* **Support**
* **Documentation**
* **Defect Tracking**
* **Task Management** (Jira)



---

![SCM](Images/SCM.jpg)

There are often more topics that were not listed, and sometimes these topics are even broken down into further granularity. 


### Software Requirements


### Environment Information
A development environment will be where an engineer can actually develop code by providing many integrations with things like testing, building and installation.

## Embedded Software Configuration Management

![Embedded System Development Platform](Images/Embedded-Dev-Platform.jpg)

![Software Tools](Images/Software-Tools.jpg)

## Software Support

![iOS Support Matrix](Images/iOS-Support-Matrix.jpg)

### Legacy Systems
Older systems that may or may not be supported anymore

Reasons:
- Software or hardware is outdated
- A loss of compatibility
- Parts not available
- Off-company roadmap

## Development Environment
[Development Environment](Tools/README.md#development-environment).

---

## Documentation

* **Features Specification**
    
    - The process of creating feature and operation requirements checklist is called a specification, or a features spec.

* **Investigation of Features & Specs**
 
    * **Platform Documents** - There are many documents that describe how to pick out a platform or evaluate a particular chip.
        
        1. **Selector Guide** - Helps a user slip down choices by interactively selecting feature sets for our design. It shows a full processor family.
        
            * A **chip family** will share the same chip architecture.
            * Each **sub-family** typically has more differences in supported hardware.
            * Each **device** in a sub-family only has a slightly variances from one sub-family part to another.

        ![Selector Guide](Images/Selector-Guide.jpg)

        2. **Product Brief**
            * Concise overview of a product
            * Talks about use cases
            * Gives more detailed feature specifications
            * Nice on the eyes

        3. **Datasheets**

            * An informative yet dense read

            * Contains detailed technical specifications

                * **Electrical** - Information on power specs of various conditions and operating modes.
                
                ![Electrical Spec](Images/Electrical-Spec.jpg)

                
                * **Timing** - You will find info on the limit of the processor's clock frequencies. There are timing diagrams that show expected time delays before certain digital signals are asserted. These quantities are usually measured in micro or nano seconds. Helps predict or calculate runtime requirements and performance.
                
                ![Timing Spec](Images/Timing-Spec.jpg)
                
                * **Environmental** - Environmental effects such as how temperature, can affect the device or the operation characteristics.
                
                ![Environmental Spec](Images/Environmental-Spec.jpg)

                * **Physical Package** - physical design constraints such as a CAD drawing with dimensions for the physical package and footprints of the chip, describes which pins match up to the general IO ports of the microcontroller, and subsequently, which pins can connect to certain peripheral devices.

                ![Physical Package](Images/Physical-Package-Spec.jpg)
        
        4. **Family Technical Reference Manual**
            
            A comprehensive document that provides detailed information about a specific family of microcontrollers or integrated circuits (ICs). It outlines:

            * Configuration details
            * Operation descriptions
            * Used to write Bare-Metal Firmware
            
            ![Family Technical Reference Manual](Images/Ref-Manual.jpg)
            
        5. **Chip Errata**
            
            A document that provides important information about issues or problems found in a specific chip or family of chips after they have been released.
        
            * Integrated Circuits are not perfect
            * Error descriptions
            * Provides corrective information or workaround to issue

            ![Chip Errata](Images/Chip-Errata.jpg)


    * **Prototyping & Proof of Concept**
        * **Prototyping** - The process of creating an early model or sample of a product to test and validate ideas before full-scale production.
        
        * **Proof of Concept (PoC)** - A demonstration to verify that certain concepts or theories have the potential to be developed into a viable product.

        - Manufacturers help with this process by providing resources to analyze their products. 


---
#### **[⇐ Embedded Systems](./README.md)**
---